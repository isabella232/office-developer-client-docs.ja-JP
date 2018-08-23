---
title: オフライン状態のアドインを使用して、監視のための接続状態の変更
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9f7f3bc0e305fb5aa7d6ae1e1909b573b3376ef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801643"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="a671d-103">オフライン状態のアドインを使用して、監視のための接続状態の変更</span><span class="sxs-lookup"><span data-stu-id="a671d-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="a671d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a671d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a671d-105">オフライン状態アドインを使用するには接続状態の変更を監視するのには、前に設定し、アドインを初期化する関数を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a671d-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="a671d-106">詳細については、[アドインの設定をオフラインの状態](setting-up-an-offline-state-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a671d-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="a671d-107">オフラインの状態を追加で設定した後は、オフラインのオブジェクトを取得するのに**[HrOpenOfflineObj](hropenofflineobj.md)** 関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a671d-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="a671d-108">このオフラインのオブジェクトを使用すると、状態モニターを初期化および取得し、現在の状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="a671d-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="a671d-109">このトピックでは、これらの状態の監視機能は、オフライン状態のサンプル アドイン内のコード例を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="a671d-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="a671d-110">オフライン状態のサンプル アドインは、COM アドインを Outlook に、**オフライン状態**のメニューを追加し、オフライン状態 API を利用してします。</span><span class="sxs-lookup"><span data-stu-id="a671d-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="a671d-111">**オフライン状態**] メニューの [使用を有効にするまたは状態の監視を無効にする、現在の状態を確認して現在の状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="a671d-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="a671d-112">ダウンロードしてオフライン状態のサンプル アドインをインストールする方法の詳細については[、オフライン状態のサンプル アドインをインストールする](installing-the-sample-offline-state-add-in.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a671d-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="a671d-113">オフライン状態 API の詳細については、[の「オフライン状態 API](about-the-offline-state-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a671d-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="a671d-114">オフライン状態のアドインが切断されたとき、正常に終了し、アドインをクリーンアップする機能を実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a671d-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="a671d-115">詳細については、[オフライン状態追加の接続を切断する](disconnecting-an-offline-state-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a671d-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="a671d-116">オフラインのオブジェクトの開いているルーチン</span><span class="sxs-lookup"><span data-stu-id="a671d-116">Open Offline Object routine</span></span>

<span data-ttu-id="a671d-117">接続状態の変更が発生したときに通知を受け取るクライアントは、 **[HrOpenOfflineObj](hropenofflineobj.md)** 関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a671d-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="a671d-118">この関数は、 **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)** をサポートしているオフラインのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a671d-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="a671d-119">**HrOpenOfflineObj**関数は、ConnectionState.h ヘッダー ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="a671d-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a671d-120">**HrOpenOfflineObj**関数が ImportProcs.h ヘッダー ファイルで次のように宣言されている: `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`。</span><span class="sxs-lookup"><span data-stu-id="a671d-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="a671d-121">HrOpenOfflineObj の使用例</span><span class="sxs-lookup"><span data-stu-id="a671d-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="a671d-122">モニターのルーチンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a671d-122">Initialize Monitor routine</span></span>

<span data-ttu-id="a671d-123">`InitMonitor` 、 **HrOpenOfflineObj**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a671d-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="a671d-124">`InitMonitor`関数は、Outlook では、クライアントにコールバック通知を送信することができますので、 **CMyOfflineNotify**を呼び出すし、 **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** 変数をコールバックを登録する`AdviseInfo`。</span><span class="sxs-lookup"><span data-stu-id="a671d-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="a671d-125">InitMonitor() の使用例</span><span class="sxs-lookup"><span data-stu-id="a671d-125">InitMonitor() example</span></span>

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a><span data-ttu-id="a671d-126">ルーチンの現在の状態の取得</span><span class="sxs-lookup"><span data-stu-id="a671d-126">Get Current State routine</span></span>

<span data-ttu-id="a671d-127">`GetCurrentState`関数は、 **HrOpenOfflineObj**関数を呼び出すし、オフラインのオブジェクトを使用して、現在の接続状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="a671d-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="a671d-128">現在の状態が返されます、`ulCurState`で使用されている変数、`CButtonEventHandler::Click`ユーザーに現在の状態を表示する関数です。</span><span class="sxs-lookup"><span data-stu-id="a671d-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="a671d-129">GetCurrentState() の使用例</span><span class="sxs-lookup"><span data-stu-id="a671d-129">GetCurrentState() example</span></span>

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a><span data-ttu-id="a671d-130">ルーチンの現在の状態を設定</span><span class="sxs-lookup"><span data-stu-id="a671d-130">Set Current State routine</span></span>

<span data-ttu-id="a671d-131">`SetCurrentState`関数は、 **HrOpenOfflineObj**関数を呼び出すし、オフラインのオブジェクトを使用して、現在の接続状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="a671d-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="a671d-132">`CButtonEventHandler::Click`関数呼び出し、`SetCurrentState`関数、および新しい状態で渡されるから、`ulState`変数です。</span><span class="sxs-lookup"><span data-stu-id="a671d-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="a671d-133">SetCurrentState() の使用例</span><span class="sxs-lookup"><span data-stu-id="a671d-133">SetCurrentState() example</span></span>

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a><span data-ttu-id="a671d-134">通知先ルーチン</span><span class="sxs-lookup"><span data-stu-id="a671d-134">Notification routine</span></span>

<span data-ttu-id="a671d-135">**[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** 関数は、クライアントの接続状態が変更されたときに通知を送信する Outlook で使用します。</span><span class="sxs-lookup"><span data-stu-id="a671d-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="a671d-136">CMyOfflineNotify::Notify() の使用例</span><span class="sxs-lookup"><span data-stu-id="a671d-136">CMyOfflineNotify::Notify() example</span></span>

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a><span data-ttu-id="a671d-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="a671d-137">See also</span></span>

- [<span data-ttu-id="a671d-138">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="a671d-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="a671d-139">サンプルのオフライン状態アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="a671d-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="a671d-140">サンプルのオフライン状態アドインについて</span><span class="sxs-lookup"><span data-stu-id="a671d-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="a671d-141">オフライン状態アドインの設定</span><span class="sxs-lookup"><span data-stu-id="a671d-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="a671d-142">オフライン状態アドインの切断</span><span class="sxs-lookup"><span data-stu-id="a671d-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

