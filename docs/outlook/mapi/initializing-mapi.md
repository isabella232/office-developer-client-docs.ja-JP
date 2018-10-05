---
title: MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399040"
---
# <a name="initializing-mapi"></a><span data-ttu-id="57efb-103">MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="57efb-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="57efb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57efb-105">MAPI ライブラリを使用するすべてのクライアント アプリケーションは**生じます**関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="57efb-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="57efb-106">詳細については、[生じます](mapiinitialize.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57efb-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="57efb-107">**生じます**では、セッションのグローバル データを初期化し、呼び出しを受け入れるため、MAPI ライブラリを準備します。</span><span class="sxs-lookup"><span data-stu-id="57efb-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="57efb-108">いくつかの状況で設定するのには重要ないくつかのフラグがあります。</span><span class="sxs-lookup"><span data-stu-id="57efb-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="57efb-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="57efb-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="57efb-110">クライアントが Windows サービスとして実装されている場合は、MAPI_NT_SERVICE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="57efb-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="57efb-111">クライアントは Windows サービスであり、このフラグを設定しないで場合、MAPI が認識されず、サービスとして。</span><span class="sxs-lookup"><span data-stu-id="57efb-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="57efb-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="57efb-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="57efb-113">MAPI_MULTITHREAD_NOTIFICATIONS フラグは、MAPI 通知の管理方法に関連しています。</span><span class="sxs-lookup"><span data-stu-id="57efb-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="57efb-114">MAPI では、通知を生成するオブジェクトへの変更が発生したときに、ウィンドウ メッセージを受信する非表示のウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="57efb-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="57efb-115">ウィンドウ メッセージは、ある時点で、通知を送信して、適切な[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出せる原因で処理されます。</span><span class="sxs-lookup"><span data-stu-id="57efb-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="57efb-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="57efb-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="57efb-117">[CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx)の呼び出しで COM を初期化するために**生じます**が試みないように、MAPI_NO_COINT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="57efb-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="57efb-118">**MAPIINIT_0**構造体が渡された場合に**生じます** _ulFlags_ MAPI_NO_COINIT に設定すると、MAPI は、COM が既に初期化されてし、 **CoInitialize**の呼び出しを使用しないと見なされます。</span><span class="sxs-lookup"><span data-stu-id="57efb-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="57efb-119">MAPI が使用されていたスレッドに通知ウィンドウを作成する MAPI_MULTITHREAD_NOTIFICATIONS のフラグが渡されない場合に**生じます**の最初の呼び出しをします。</span><span class="sxs-lookup"><span data-stu-id="57efb-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="57efb-120">MAPI_MULTITHREAD_NOTIFICATIONS が渡された場合、MAPI が別のスレッドに通知ウィンドウを作成、通知の処理に専用のスレッドです。</span><span class="sxs-lookup"><span data-stu-id="57efb-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="57efb-121">MAPI では、通知を非表示のウィンドウを作成するために使用されるスレッドを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="57efb-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="57efb-122">メッセージ ループがあります。</span><span class="sxs-lookup"><span data-stu-id="57efb-122">Have a message loop.</span></span>
    
- <span data-ttu-id="57efb-123">セッションの有効期間全体にわたってブロックを解除されたままになります。</span><span class="sxs-lookup"><span data-stu-id="57efb-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="57efb-124">クライアントによって作成された他のスレッドよりも長い有効期間があります。</span><span class="sxs-lookup"><span data-stu-id="57efb-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="57efb-125">**生じます**の最初の呼び出しにフラグを設定することでスレッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="57efb-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="57efb-126">通知を処理するために、スレッドの 1 つを許可する危険性は、スレッドが消える場合は、通知ウィンドウが破棄される、他のスレッドのいずれかに通知が送信される不要になったことです。</span><span class="sxs-lookup"><span data-stu-id="57efb-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="57efb-127">特別な処理は、非表示のウィンドウのメッセージ キューに投稿される通知メッセージのディスパッチを制御する必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="57efb-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="57efb-128">通知を処理する別のウィンドウを使用する場合は、適切なスレッドに適切な時に通知が表示されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="57efb-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="57efb-129">確認し、[通知] ウィンドウに転記される Windows メッセージを処理する特別なコードを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="57efb-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="57efb-130">MAPI は、次の種類のクライアント アプリケーションが通知をサポートするための非表示のウィンドウを作成する別のスレッドを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="57efb-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="57efb-131">マルチ スレッドのすべてのクライアントです。</span><span class="sxs-lookup"><span data-stu-id="57efb-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="57efb-132">シングル スレッドの Windows サービスと Win32 コンソール アプリケーションをします。</span><span class="sxs-lookup"><span data-stu-id="57efb-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="57efb-133">通知に、メイン スレッドを使用する必要のないシングル スレッドのクライアントです。</span><span class="sxs-lookup"><span data-stu-id="57efb-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="57efb-134">別のスレッドのアプローチを使用するには、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定するすべてのスレッドで**生じます**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57efb-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="57efb-135">のみクライアントの最初の呼び出しに**生じます**が、通知をサポートするために作成される非表示のウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="57efb-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="57efb-136">2 回目以降では、参照カウントをインクリメントする唯一の原因を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57efb-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

