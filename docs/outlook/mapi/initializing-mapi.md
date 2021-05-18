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
# <a name="initializing-mapi"></a><span data-ttu-id="fff72-103">MAPI の初期化</span><span class="sxs-lookup"><span data-stu-id="fff72-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="fff72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fff72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fff72-105">MAPI ライブラリを使用するクライアント アプリケーションはすべて **、MAPIInitialize 関数を呼び出す必要** があります。</span><span class="sxs-lookup"><span data-stu-id="fff72-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="fff72-106">詳細については [、「MAPIInitialize」を参照してください](mapiinitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="fff72-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="fff72-107">**MAPIInitialize は** 、セッションのグローバル データを初期化し、呼び出しを受け入れる MAPI ライブラリを準備します。</span><span class="sxs-lookup"><span data-stu-id="fff72-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="fff72-108">いくつかの状況で設定することが重要なフラグがいくつかある。</span><span class="sxs-lookup"><span data-stu-id="fff72-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="fff72-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="fff72-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="fff72-110">クライアントが windows MAPI_NT_SERVICE実装されている場合は、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="fff72-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="fff72-111">クライアントが Windows サービスであり、このフラグを設定しない場合、MAPI はサービスとして認識できません。</span><span class="sxs-lookup"><span data-stu-id="fff72-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="fff72-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="fff72-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="fff72-113">[MAPI_MULTITHREAD_NOTIFICATIONS] フラグは、MAPI が通知を管理する方法に関連します。</span><span class="sxs-lookup"><span data-stu-id="fff72-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="fff72-114">MAPI は、通知を生成するオブジェクトに対する変更が発生すると、ウィンドウ メッセージを受信する非表示のウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="fff72-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="fff72-115">ウィンドウ メッセージは、ある時点で処理され、通知が送信され、適切な [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fff72-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="fff72-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="fff72-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="fff72-117">**MAPIInitialize** MAPI_NO_COINT呼び出しで COM を初期化しようとしないので、このフラグを [設定します](https://msdn.microsoft.com/library/ms886303.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fff72-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="fff72-118">MAPIINIT_0構造体が **mapiInitialize** に渡され _、ulFlags_ が MAPI_NO_COINIT に設定されている場合、MAPI は COM が既に初期化済みと見なされ **、CoInitialize** への呼び出しをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fff72-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="fff72-119">このMAPI_MULTITHREAD_NOTIFICATIONSが渡されない場合、MAPI は最初の **MAPIInitialize** 呼び出しに使用されたスレッドに通知ウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="fff72-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="fff72-120">MAPI は、通知を処理するために専用のスレッドMAPI_MULTITHREAD_NOTIFICATIONS場合は、別のスレッドに通知ウィンドウを作成します。</span><span class="sxs-lookup"><span data-stu-id="fff72-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="fff72-121">MAPI では、非表示の通知ウィンドウの作成に使用されるスレッドが次の処理を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fff72-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="fff72-122">メッセージ ループを設定します。</span><span class="sxs-lookup"><span data-stu-id="fff72-122">Have a message loop.</span></span>
    
- <span data-ttu-id="fff72-123">セッションの一生を通してブロック解除されたままにします。</span><span class="sxs-lookup"><span data-stu-id="fff72-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="fff72-124">クライアントによって作成された他のスレッドよりも長い有効期間を持つ。</span><span class="sxs-lookup"><span data-stu-id="fff72-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="fff72-125">最初の **MAPIInitialize** 呼び出しでフラグを設定することで、使用するスレッドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fff72-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="fff72-126">スレッドの 1 つで通知を処理できる危険性は、スレッドが消えると、通知ウィンドウが破棄され、通知を他のスレッドに送信できなくなるという危険があります。</span><span class="sxs-lookup"><span data-stu-id="fff72-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="fff72-127">また、非表示ウィンドウのメッセージ キューに投稿される通知メッセージのディスパッチを制御するために、特別な処理が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fff72-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="fff72-128">別のウィンドウを使用して通知を処理する場合は、通知が適切なスレッドに適切な時刻に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fff72-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="fff72-129">通知ウィンドウに投稿された Windows メッセージをチェックして処理する特別なコードは必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fff72-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="fff72-130">MAPI では、次の種類のクライアント アプリケーションが別のスレッドを使用して、通知サポート用の非表示ウィンドウを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fff72-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="fff72-131">すべてのマルチスレッド クライアント。</span><span class="sxs-lookup"><span data-stu-id="fff72-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="fff72-132">シングル スレッド Windows サービスと Win32 コンソール アプリケーション。</span><span class="sxs-lookup"><span data-stu-id="fff72-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="fff72-133">通知にメイン スレッドを使用する必要ないシングル スレッド クライアント。</span><span class="sxs-lookup"><span data-stu-id="fff72-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="fff72-134">個別のスレッド アプローチを使用するには、すべてのスレッドで **MAPIInitialize** を呼び出し、MAPI_MULTITHREAD_NOTIFICATIONSします。</span><span class="sxs-lookup"><span data-stu-id="fff72-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fff72-135">**MAPIInitialize** へのクライアントの最初の呼び出しのみ、通知をサポートするために非表示ウィンドウが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fff72-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="fff72-136">それ以降の呼び出しでは、参照カウントが増分されるのみです。</span><span class="sxs-lookup"><span data-stu-id="fff72-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

