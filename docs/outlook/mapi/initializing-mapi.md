---
title: MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309731"
---
# <a name="initializing-mapi"></a><span data-ttu-id="89697-103">MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="89697-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="89697-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89697-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89697-105">MAPI ライブラリを使用するすべてのクライアントアプリケーションは、 **MAPIInitialize**関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="89697-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="89697-106">詳細については、「 [MAPIInitialize](mapiinitialize.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89697-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="89697-107">**MAPIInitialize**は、セッションのグローバルデータを初期化し、呼び出しを受け入れるように MAPI ライブラリを準備します。</span><span class="sxs-lookup"><span data-stu-id="89697-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="89697-108">状況によっては、次のようないくつかのフラグが設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="89697-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="89697-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="89697-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="89697-110">クライアントが Windows サービスとして実装されている場合は、MAPI_NT_SERVICE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="89697-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="89697-111">クライアントが Windows サービスで、このフラグが設定されていない場合、MAPI はサービスとして認識しません。</span><span class="sxs-lookup"><span data-stu-id="89697-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="89697-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="89697-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="89697-113">MAPI_MULTITHREAD_NOTIFICATIONS フラグは、MAPI が通知を管理する方法に関連しています。</span><span class="sxs-lookup"><span data-stu-id="89697-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="89697-114">MAPI は、通知を生成するオブジェクトに変更が発生したときにウィンドウメッセージを受信する非表示のウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="89697-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="89697-115">ウィンドウメッセージは何らかの時点で処理され、通知が送信され、適切な[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="89697-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="89697-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="89697-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="89697-117">MAPI_NO_COINT フラグを設定して、 **MAPIInitialize**が[CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx)の呼び出しで COM を初期化しないようにします。</span><span class="sxs-lookup"><span data-stu-id="89697-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="89697-118">_ulflags_が MAPI_NO_COINIT に設定されている場合、 **MAPIINIT_0**構造体が**MAPIInitialize**に渡されると、MAPI は COM が既に初期化されていると見なし、 **CoInitialize**への呼び出しをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="89697-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="89697-119">MAPI_MULTITHREAD_NOTIFICATIONS フラグが渡されない場合、MAPI は最初の**MAPIInitialize**呼び出しで使用されたスレッドに通知ウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="89697-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="89697-120">MAPI_MULTITHREAD_NOTIFICATIONS が渡されると、通知の処理専用のスレッドが生成されると、MAPI は別のスレッドで通知ウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="89697-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="89697-121">MAPI では、非表示の通知ウィンドウを作成するために使用されているスレッドが次のことを前提としています。</span><span class="sxs-lookup"><span data-stu-id="89697-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="89697-122">メッセージループがあります。</span><span class="sxs-lookup"><span data-stu-id="89697-122">Have a message loop.</span></span>
    
- <span data-ttu-id="89697-123">セッションが終了するまで、ブロックされないままになります。</span><span class="sxs-lookup"><span data-stu-id="89697-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="89697-124">クライアントによって作成された他のスレッドよりも長い有効期間がある。</span><span class="sxs-lookup"><span data-stu-id="89697-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="89697-125">最初の**MAPIInitialize**呼び出しでフラグを設定することによって、どのスレッドを使用するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="89697-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="89697-126">スレッドの1つが通知を処理できるようにする危険性は、スレッドが表示されなくなると、通知ウィンドウが破棄され、他のスレッドに通知を送信できなくなることです。</span><span class="sxs-lookup"><span data-stu-id="89697-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="89697-127">また、非表示のウィンドウのメッセージキューにポストされる通知メッセージのディスパッチを制御するために、特別な処理が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="89697-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="89697-128">別のウィンドウを使用して通知を処理する場合は、適切なスレッドの適切なタイミングで通知が表示されることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="89697-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="89697-129">通知ウィンドウにポストされた Windows メッセージを確認して処理するための特別なコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="89697-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="89697-130">MAPI では、次の種類のクライアントアプリケーションが別のスレッドを使用して通知をサポートする非表示のウィンドウを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="89697-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="89697-131">すべてのマルチスレッドクライアント。</span><span class="sxs-lookup"><span data-stu-id="89697-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="89697-132">シングルスレッド Windows サービスおよび Win32 コンソールアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="89697-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="89697-133">通知にメインスレッドを使用する必要がない、シングルスレッドクライアント。</span><span class="sxs-lookup"><span data-stu-id="89697-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="89697-134">個別のスレッドアプローチを使用するには、すべてのスレッドで**MAPIInitialize**を呼び出し、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="89697-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="89697-135">クライアントの最初の**MAPIInitialize**への呼び出しでは、通知をサポートする非表示のウィンドウが作成されます。</span><span class="sxs-lookup"><span data-stu-id="89697-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="89697-136">以降の呼び出しでは、参照カウントがインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="89697-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

