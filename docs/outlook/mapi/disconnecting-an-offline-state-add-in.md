---
title: オフライン状態の追加の接続を切断します。
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19799919"
---
# <a name="disconnecting-an-offline-state-add-in"></a>オフライン状態の追加の接続を切断します。

**適用されます**: Outlook 
  
オフライン状態のアドインが切断されたとき、正常に終了し、アドインをクリーンアップする機能を実装しなければなりません。 設定し、オフライン使用の詳細については、アドインの接続状態の変更を監視するには、[アドインの設定をオフライン状態](setting-up-an-offline-state-add-in.md)および[監視接続状態の変更を使用してオフライン状態アドインを](monitoring-connection-state-changes-using-an-offline-state-add-in.md)参照してください状態です。
  
このトピックでは、これらの切断を終了して、オフライン状態のサンプル アドイン内のコード例を使用してクリーンアップ関数の例を示します。 オフライン状態のサンプル アドインは、COM アドインを Outlook に、**オフライン状態**のメニューを追加し、オフライン状態 API を使用してします。 オフライン状態] メニューの [使用を有効にするまたは状態の監視を無効にする、現在の状態を確認して現在の状態を変更できます。 ダウンロードしてオフライン状態のサンプル アドインをインストールする方法の詳細については[、オフライン状態のサンプル アドインをインストールする](installing-the-sample-offline-state-add-in.md)」を参照してください。 オフライン状態 API の詳細については、[の「オフライン状態 API](about-the-offline-state-api.md)を参照してください。
  
## <a name="on-disconnection-routine"></a>切断ルーチン

**IDTExtensibility2.OnDisconnection**メソッドは、オフライン状態のアドインがアンロードされるときに呼び出されます。 クリーン アップ コードをこの関数を実装する必要があります。 **IDTExtensibility2.OnDisconnection**関数を呼び出す例を次に、`HrTermAddin`関数です。 
  
### <a name="cmyaddinondisconnection-example"></a>CMyAddin::OnDisconnection() の使用例

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>アドインの関数を終了します。

`HrTermAddin`関数呼び出し、 `inDeInitMonitor`、`HrRemoveMenuItems`と`UnloadLibraries`でオフライン状態の追加のクリーンアップを終了する関数です。 
  
### <a name="cmyaddinhrtermaddin-example"></a>CMyAddin::HrTermAddin() の使用例

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a>監視ルーチンを deinitialize します。

`inDeInitMonitor` 、オフラインのオブジェクトのコールバックをキャンセルする、 [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)関数を呼び出します。 
  
### <a name="deinitmonitor-example"></a>DeInitMonitor() の使用例

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a>メニュー項目のルーチンを削除します。

`HrRemoveMenuItems`関数呼び出しの`DispEventUnadvise`[**オフライン状態**] メニューのメニュー項目ごとにし、**オフライン状態**のメニューを削除します。 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>CMyAddin::HrRemoveMenuItems() の使用例

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a>ライブラリ ルーチンをアンロードします。

アドインがアンロードされるとき、Outlook から、`UnloadLibraries`関数は、アドインを必要とするダイナミック リンク ライブラリ (Dll) をアンロードします。 
  
### <a name="unloadlibraries-example"></a>UnloadLibraries() の使用例

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a>関連項目

- [オフラインの状態の API について](about-the-offline-state-api.md)
- [サンプル オフライン状態のアドインをインストールします。](installing-the-sample-offline-state-add-in.md)
- [アドインの状態をオフラインのサンプルについて](about-the-sample-offline-state-add-in.md)
- [オフライン状態のアドインを設定します。](setting-up-an-offline-state-add-in.md)
- [接続状態の監視は、アドインを使用して、オフライン状態を変更します。](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

