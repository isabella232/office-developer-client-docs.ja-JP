---
title: オフライン状態アドインの切断
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '最終更新日: 2015 年 12 月 7 日'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564137"
---
# <a name="disconnecting-an-offline-state-add-in"></a>オフライン状態アドインの切断

**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン状態アドインが切断された場合は、アドインを適切に終了してクリーンアップするための関数を実装する必要があります。 接続状態変更の監視を行うためのオフライン状態アドインのセットアップとその使用の詳細については、[オフライン状態アドインのセットアップ](setting-up-an-offline-state-add-in.md)、[オフライン状態アドインを使用した接続状態変更の監視](monitoring-connection-state-changes-using-an-offline-state-add-in.md)を参照してください。
  
このトピックでは、サンプルのオフライン状態アドインのコード例を使って、これらの切断、終了、クリーンアップ関数を説明します。 サンプルのオフライン状態アドインは、オフライン状態 API を使用して Outlook に**オフライン状態**メニューを追加する COM アドインです。 オフライン状態メニューを使うと、状態の監視を有効または無効にしたり、現在の状態を確認、変更したりすることができます。 サンプルのオフライン状態アドインのダウンロードやインストールの詳細については、[サンプルのオフライン状態アドインのインストール](installing-the-sample-offline-state-add-in.md)を参照してください。 オフライン状態 API の詳細については、[オフライン状態 API について](about-the-offline-state-api.md)を参照してください。
  
## <a name="on-disconnection-routine"></a>切断ルーチンについて

オフライン状態アドインがアンロードされると、**IDTExtensibility2.OnDisconnection** メソッドが呼び出されます。 この関数にはクリーンアップ コードを実装する必要があります。 次の例では、**IDTExtensibility2.OnDisconnection** 関数が `HrTermAddin` 関数を呼び出します。 
  
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

## <a name="terminate-add-in-function"></a>アドイン関数の終了

`HrTermAddin` 関数が `inDeInitMonitor`、`HrRemoveMenuItems` および `UnloadLibraries` 関数を呼び出して、オフライン状態アドインのクリーンアップを完了します。 
  
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

## <a name="deinitialize-monitor-routine"></a>監視ルーチンの非初期化

`inDeInitMonitor` 関数が、[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) 関数を呼び出して、オフライン オブジェクトのコールバックをキャンセルします。 
  
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

## <a name="remove-menu-items-routine"></a>メニュー アイテム ルーチンの削除

`HrRemoveMenuItems` 関数が**オフライン状態**メニューにある各メニュー アイテムの `DispEventUnadvise` を呼び出した後、**オフライン状態**メニューを削除します。 
  
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

## <a name="unload-libraries-routine"></a>ライブラリ ルーチンのアンロード

Outlook からアドインがアンロードされると、`UnloadLibraries` 関数がそのアドインが必要とするダイナミック リンク ライブラリ (DLL) をアンロードします。 
  
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

- [オフライン状態 API について](about-the-offline-state-api.md)
- [サンプルのオフライン状態アドインのインストール](installing-the-sample-offline-state-add-in.md)
- [サンプルのオフライン状態アドインについて](about-the-sample-offline-state-add-in.md)
- [オフライン状態アドインのセットアップ](setting-up-an-offline-state-add-in.md)
- [オフライン状態アドインを使用した接続状態変更の監視](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

