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
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="e4b0c-103">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="e4b0c-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="e4b0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4b0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4b0c-105">オフライン状態アドインが切断された場合は、アドインを適切に終了してクリーンアップするための関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="e4b0c-106">接続状態変更の監視を行うためのオフライン状態アドインのセットアップとその使用の詳細については、[オフライン状態アドインのセットアップ](setting-up-an-offline-state-add-in.md)、[オフライン状態アドインを使用した接続状態変更の監視](monitoring-connection-state-changes-using-an-offline-state-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="e4b0c-107">このトピックでは、サンプルのオフライン状態アドインのコード例を使って、これらの切断、終了、クリーンアップ関数を説明します。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="e4b0c-108">サンプルのオフライン状態アドインは、オフライン状態 API を使用して Outlook に**オフライン状態**メニューを追加する COM アドインです。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="e4b0c-109">オフライン状態メニューを使うと、状態の監視を有効または無効にしたり、現在の状態を確認、変更したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="e4b0c-110">サンプルのオフライン状態アドインのダウンロードやインストールの詳細については、[サンプルのオフライン状態アドインのインストール](installing-the-sample-offline-state-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="e4b0c-111">オフライン状態 API の詳細については、[オフライン状態 API について](about-the-offline-state-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="e4b0c-112">切断ルーチンについて</span><span class="sxs-lookup"><span data-stu-id="e4b0c-112">On Disconnection Routine</span></span>

<span data-ttu-id="e4b0c-113">オフライン状態アドインがアンロードされると、**IDTExtensibility2.OnDisconnection** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="e4b0c-114">この関数にはクリーンアップ コードを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="e4b0c-115">次の例では、**IDTExtensibility2.OnDisconnection** 関数が `HrTermAddin` 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="e4b0c-116">CMyAddin::OnDisconnection() の使用例</span><span class="sxs-lookup"><span data-stu-id="e4b0c-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="e4b0c-117">アドイン関数の終了</span><span class="sxs-lookup"><span data-stu-id="e4b0c-117">Terminate Add-in Function</span></span>

<span data-ttu-id="e4b0c-118">`HrTermAddin` 関数が `inDeInitMonitor`、`HrRemoveMenuItems` および `UnloadLibraries` 関数を呼び出して、オフライン状態アドインのクリーンアップを完了します。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="e4b0c-119">CMyAddin::HrTermAddin() の使用例</span><span class="sxs-lookup"><span data-stu-id="e4b0c-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="e4b0c-120">監視ルーチンの非初期化</span><span class="sxs-lookup"><span data-stu-id="e4b0c-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="e4b0c-121">`inDeInitMonitor` 関数が、[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) 関数を呼び出して、オフライン オブジェクトのコールバックをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="e4b0c-122">DeInitMonitor() の使用例</span><span class="sxs-lookup"><span data-stu-id="e4b0c-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="e4b0c-123">メニュー アイテム ルーチンの削除</span><span class="sxs-lookup"><span data-stu-id="e4b0c-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="e4b0c-124">`HrRemoveMenuItems` 関数が**オフライン状態**メニューにある各メニュー アイテムの `DispEventUnadvise` を呼び出した後、**オフライン状態**メニューを削除します。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="e4b0c-125">CMyAddin::HrRemoveMenuItems() の使用例</span><span class="sxs-lookup"><span data-stu-id="e4b0c-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="e4b0c-126">ライブラリ ルーチンのアンロード</span><span class="sxs-lookup"><span data-stu-id="e4b0c-126">Unload Libraries Routine</span></span>

<span data-ttu-id="e4b0c-127">Outlook からアドインがアンロードされると、`UnloadLibraries` 関数がそのアドインが必要とするダイナミック リンク ライブラリ (DLL) をアンロードします。</span><span class="sxs-lookup"><span data-stu-id="e4b0c-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="e4b0c-128">UnloadLibraries() の使用例</span><span class="sxs-lookup"><span data-stu-id="e4b0c-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e4b0c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4b0c-129">See also</span></span>

- [<span data-ttu-id="e4b0c-130">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="e4b0c-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="e4b0c-131">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="e4b0c-131">Installing the sample Offline State add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="e4b0c-132">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="e4b0c-132">About the sample Offline State add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="e4b0c-133">オフライン状態アドインのセットアップ</span><span class="sxs-lookup"><span data-stu-id="e4b0c-133">Setting up an Offline State add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="e4b0c-134">オフライン状態アドインを使用した接続状態変更の監視</span><span class="sxs-lookup"><span data-stu-id="e4b0c-134">Monitoring connection state changes using an Offline State add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

