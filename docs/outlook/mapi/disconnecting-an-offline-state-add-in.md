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
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="20fbd-103">オフライン状態の追加の接続を切断します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="20fbd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20fbd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20fbd-105">オフライン状態のアドインが切断されたとき、正常に終了し、アドインをクリーンアップする機能を実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20fbd-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="20fbd-106">設定し、オフライン使用の詳細については、アドインの接続状態の変更を監視するには、[アドインの設定をオフライン状態](setting-up-an-offline-state-add-in.md)および[監視接続状態の変更を使用してオフライン状態アドインを](monitoring-connection-state-changes-using-an-offline-state-add-in.md)参照してください状態です。</span><span class="sxs-lookup"><span data-stu-id="20fbd-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="20fbd-107">このトピックでは、これらの切断を終了して、オフライン状態のサンプル アドイン内のコード例を使用してクリーンアップ関数の例を示します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="20fbd-108">オフライン状態のサンプル アドインは、COM アドインを Outlook に、**オフライン状態**のメニューを追加し、オフライン状態 API を使用してします。</span><span class="sxs-lookup"><span data-stu-id="20fbd-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="20fbd-109">オフライン状態] メニューの [使用を有効にするまたは状態の監視を無効にする、現在の状態を確認して現在の状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="20fbd-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="20fbd-110">ダウンロードしてオフライン状態のサンプル アドインをインストールする方法の詳細については[、オフライン状態のサンプル アドインをインストールする](installing-the-sample-offline-state-add-in.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20fbd-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="20fbd-111">オフライン状態 API の詳細については、[の「オフライン状態 API](about-the-offline-state-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20fbd-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="20fbd-112">切断ルーチン</span><span class="sxs-lookup"><span data-stu-id="20fbd-112">On Disconnection Routine</span></span>

<span data-ttu-id="20fbd-113">**IDTExtensibility2.OnDisconnection**メソッドは、オフライン状態のアドインがアンロードされるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="20fbd-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="20fbd-114">クリーン アップ コードをこの関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20fbd-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="20fbd-115">**IDTExtensibility2.OnDisconnection**関数を呼び出す例を次に、`HrTermAddin`関数です。</span><span class="sxs-lookup"><span data-stu-id="20fbd-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="20fbd-116">CMyAddin::OnDisconnection() の使用例</span><span class="sxs-lookup"><span data-stu-id="20fbd-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="20fbd-117">アドインの関数を終了します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-117">Terminate Add-in Function</span></span>

<span data-ttu-id="20fbd-118">`HrTermAddin`関数呼び出し、 `inDeInitMonitor`、`HrRemoveMenuItems`と`UnloadLibraries`でオフライン状態の追加のクリーンアップを終了する関数です。</span><span class="sxs-lookup"><span data-stu-id="20fbd-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="20fbd-119">CMyAddin::HrTermAddin() の使用例</span><span class="sxs-lookup"><span data-stu-id="20fbd-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="20fbd-120">監視ルーチンを deinitialize します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="20fbd-121">`inDeInitMonitor` 、オフラインのオブジェクトのコールバックをキャンセルする、 [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="20fbd-122">DeInitMonitor() の使用例</span><span class="sxs-lookup"><span data-stu-id="20fbd-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="20fbd-123">メニュー項目のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="20fbd-124">`HrRemoveMenuItems`関数呼び出しの`DispEventUnadvise`[**オフライン状態**] メニューのメニュー項目ごとにし、**オフライン状態**のメニューを削除します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="20fbd-125">CMyAddin::HrRemoveMenuItems() の使用例</span><span class="sxs-lookup"><span data-stu-id="20fbd-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="20fbd-126">ライブラリ ルーチンをアンロードします。</span><span class="sxs-lookup"><span data-stu-id="20fbd-126">Unload Libraries Routine</span></span>

<span data-ttu-id="20fbd-127">アドインがアンロードされるとき、Outlook から、`UnloadLibraries`関数は、アドインを必要とするダイナミック リンク ライブラリ (Dll) をアンロードします。</span><span class="sxs-lookup"><span data-stu-id="20fbd-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="20fbd-128">UnloadLibraries() の使用例</span><span class="sxs-lookup"><span data-stu-id="20fbd-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="20fbd-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="20fbd-129">See also</span></span>

- [<span data-ttu-id="20fbd-130">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="20fbd-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="20fbd-131">サンプル オフライン状態のアドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="20fbd-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="20fbd-132">アドインの状態をオフラインのサンプルについて</span><span class="sxs-lookup"><span data-stu-id="20fbd-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="20fbd-133">オフライン状態のアドインを設定します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="20fbd-134">接続状態の監視は、アドインを使用して、オフライン状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="20fbd-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

