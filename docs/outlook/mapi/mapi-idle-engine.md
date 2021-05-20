---
title: MAPI アイドル エンジン
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d8d591c02bb621c16a1d1b46272b19573ea79785
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428453"
---
# <a name="mapi-idle-engine"></a><span data-ttu-id="d8285-103">MAPI アイドル エンジン</span><span class="sxs-lookup"><span data-stu-id="d8285-103">MAPI Idle Engine</span></span>

  
  
<span data-ttu-id="d8285-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8285-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8285-105">MAPI には、アイドル エンジンと総称される複数の機能があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-105">MAPI provides several functions that are collectively known as the idle engine.</span></span> <span data-ttu-id="d8285-106">これらの関数を使用すると、クライアント、アドレス帳プロバイダー、およびメッセージ ストア プロバイダーは、セッションの低速時または低速時にさまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d8285-106">These functions allow clients, address book providers, and message store providers to perform various tasks during slow times in the session or in response to a slow time.</span></span> <span data-ttu-id="d8285-107">たとえば、クライアントとサービス プロバイダーは、低速の操作を延期したり、長い期間使用されていないファイルを閉じることもできます。</span><span class="sxs-lookup"><span data-stu-id="d8285-107">For example, clients and service providers can defer slow operations or close files that have remained unused for a lengthy period.</span></span> <span data-ttu-id="d8285-108">**IXPLogon::Idle** メソッドが実行されるので、トランスポート プロバイダーは通常、アイドル エンジンを使用しない。</span><span class="sxs-lookup"><span data-stu-id="d8285-108">Transport providers typically do not use the idle engine because the **IXPLogon::Idle** method takes its place.</span></span> <span data-ttu-id="d8285-109">詳細については [、「IXPLogon::Idle」を参照してください](ixplogon-idle.md)。</span><span class="sxs-lookup"><span data-stu-id="d8285-109">For more information, see [IXPLogon::Idle](ixplogon-idle.md).</span></span>
  
<span data-ttu-id="d8285-110">アイドル 状態のエンジンを使用するために、クライアントとサービス プロバイダーは、MAPI サブシステムがアイドル状態のときに発生する必要があるタスクを含むコールバック関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="d8285-110">To use the idle engine, clients and service providers create a callback function that contains the tasks that should occur when the MAPI subsystem is idle.</span></span> <span data-ttu-id="d8285-111">MAPI はアイドル時間を検出すると、このコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d8285-111">When MAPI detects idle time, it invokes this callback function.</span></span> <span data-ttu-id="d8285-112">コールバック関数は、次のように定義された **FNIDLE** プロトタイプに従います。</span><span class="sxs-lookup"><span data-stu-id="d8285-112">The callback function follows the **FNIDLE** prototype, defined as follows:</span></span> 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
<span data-ttu-id="d8285-113">詳細については [、「FNIDLE」を参照してください](fnidle.md)。</span><span class="sxs-lookup"><span data-stu-id="d8285-113">For more information, see [FNIDLE](fnidle.md).</span></span>
  
<span data-ttu-id="d8285-114">アイドル エンジンを構成する関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d8285-114">The functions that make up the idle engine are:</span></span>
  
[<span data-ttu-id="d8285-115">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d8285-115">ChangeIdleRoutine</span></span>](changeidleroutine.md)
  
[<span data-ttu-id="d8285-116">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d8285-116">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md)
  
[<span data-ttu-id="d8285-117">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d8285-117">EnableIdleRoutine</span></span>](enableidleroutine.md)
  
[<span data-ttu-id="d8285-118">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d8285-118">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md)
  
[<span data-ttu-id="d8285-119">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d8285-119">MAPIDeInitIdle</span></span>](mapideinitidle.md)
  
[<span data-ttu-id="d8285-120">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d8285-120">MAPIInitIdle</span></span>](mapiinitidle.md)
  
<span data-ttu-id="d8285-121">コールバック関数を登録するために、クライアントとサービス プロバイダーは **FtgRegisterIdleRoutine 関数を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="d8285-121">To register a callback function, clients and service providers call the **FtgRegisterIdleRoutine** function.</span></span> <span data-ttu-id="d8285-122">入力パラメーターには、オプションの優先度、入力としてコールバック関数に渡されるメモリブロック、適切な方法で使用する時間、およびオプション フラグのセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d8285-122">The input parameters include an optional priority, a block of memory that is passed to your callback function as input, an amount of time to be used in any way appropriate, and a set of option flags.</span></span> 
  
<span data-ttu-id="d8285-123">クライアントとサービス プロバイダーは、アイドル関数の実行方法を制御する  _priIdle_ パラメーターで優先度を指定するか、優先度が問題ではない場合は 0 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d8285-123">Clients and service providers can specify a priority in the  _priIdle_ parameter that controls how the idle function runs or specify zero if priority is not an issue.</span></span> <span data-ttu-id="d8285-124">負の数値は正の数値またはゼロよりも優先度が高いので、圧縮および検索操作には負の数値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-124">Because negative numbers represent higher priorities than positive numbers or zero, compression and search operations should be assigned negative numbers.</span></span> <span data-ttu-id="d8285-125">一度発生するタスクには正の数値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-125">Tasks that occur once should be assigned positive numbers.</span></span> 
  
<span data-ttu-id="d8285-126">アクティブなコールバック関数の登録を解除するために、クライアントとサービス プロバイダーは **DeregisterIdleRoutine 関数を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="d8285-126">To deregister an active callback function, clients and service providers call the **DeregisterIdleRoutine** function.</span></span> <span data-ttu-id="d8285-127">**DeregisterIdleRoutine** は非同期的に動作しますので、登録解除呼び出し中、および **DeregisterIdleRoutine** が返された後でも、コールバック関数をいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d8285-127">Because **DeregisterIdleRoutine** operates asynchronously, it is possible for the callback function to be invoked at any time during the deregister call and possibly even after **DeregisterIdleRoutine** has returned.</span></span> 
  
<span data-ttu-id="d8285-128">コールバック関数の一部またはすべての特性を変更するために、クライアントとサービス プロバイダーは **ChangeIdleRoutine 関数を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="d8285-128">To modify some or all of the characteristics of a callback function, clients and service providers call the **ChangeIdleRoutine** function.</span></span> <span data-ttu-id="d8285-129">**ChangeIdleRoutine は、flags** パラメーター  _ircIdle の設定方法に従って_ 変更を行います。 **ChangeIdleRoutine は** 、関数自体、優先度、時間設定、および入力パラメーターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d8285-129">**ChangeIdleRoutine** makes changes according to how the flags parameter  _ircIdle_ is set; **ChangeIdleRoutine** can change the function itself, its priority, time setting, and input parameter.</span></span> 
  
<span data-ttu-id="d8285-130">MAPI は、オペレーティング システムに定義がある場合、オペレーティング システムと同じアイドル状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="d8285-130">MAPI defines idle the same as the operating system, when the operating system has a definition.</span></span> <span data-ttu-id="d8285-131">Win32 では、MAPI はアイドル 状態のタスクをスケジュールするアイドル クラスの優先度を持つスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8285-131">On Win32, MAPI creates a thread with idle-class priority to schedule idle tasks.</span></span> <span data-ttu-id="d8285-132">このスレッドは時間を追跡し、スレッドにメッセージを投稿し、実行の時間が到着するとアイドル タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="d8285-132">This thread keeps track of the time and posts a message to the thread that is to execute the idle task when the time for its execution arrives.</span></span> <span data-ttu-id="d8285-133">Win32 は、プロセスではなくスレッドをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="d8285-133">Win32 schedules threads, not processes.</span></span> <span data-ttu-id="d8285-134">優先度がアイドル優先度より高いタスクがワークステーションで発生している場合は、タスクが完了するまで、アイドル状態のタスクは実行のスケジュールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-134">If tasks that have a priority higher than the idle priority are occurring on the workstation, the idle task should not get scheduled for execution until the tasks have completed.</span></span> 
  
<span data-ttu-id="d8285-135">すべてのアイドル タスクは **、MAPIInitIdle** を呼び出したスレッドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d8285-135">All idle tasks run on the thread that called **MAPIInitIdle**.</span></span> <span data-ttu-id="d8285-136">MAPI にはスケジュール用の別のスレッドがありますが、アイドル 状態のタスクが適格になると、メッセージが初期化スレッドにポストバックされ、アイドル タスクがそこで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d8285-136">MAPI has a separate thread for scheduling, but when an idle task becomes eligible, it posts a message back over to the initialization thread and the idle task is executed there.</span></span> <span data-ttu-id="d8285-137">さまざまな種類のクライアントに対する影響は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d8285-137">The implications for different types of clients are as follows.</span></span>
  
|<span data-ttu-id="d8285-138">**スレッド モデル**</span><span class="sxs-lookup"><span data-stu-id="d8285-138">**Threading model**</span></span>|<span data-ttu-id="d8285-139">**意味**</span><span class="sxs-lookup"><span data-stu-id="d8285-139">**Implication**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d8285-140">シングル スレッド</span><span class="sxs-lookup"><span data-stu-id="d8285-140">Single-threaded</span></span>  <br/> |<span data-ttu-id="d8285-141">問題ありません。</span><span class="sxs-lookup"><span data-stu-id="d8285-141">No problem.</span></span> <span data-ttu-id="d8285-142">アイドル関数はクライアントのメイン スレッドで実行され、メッセージ ループを介してシリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="d8285-142">Idle functions execute on your client's main thread and are serialized through the message loop.</span></span>  <br/> |
|<span data-ttu-id="d8285-143">フリー スレッド</span><span class="sxs-lookup"><span data-stu-id="d8285-143">Free-threaded</span></span>  <br/> |<span data-ttu-id="d8285-144">アイドル状態の関数はスレッド セーフである必要がありますが、クライアントには必要なインフラストラクチャが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="d8285-144">Idle functions must be thread-safe, but your client already has the necessary infrastructure.</span></span> <span data-ttu-id="d8285-145">クライアントで MAPI アイドル エンジンが必要ない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-145">Your client might not need the MAPI idle engine at all.</span></span>  <br/> |
|<span data-ttu-id="d8285-146">アパートメント スレッド</span><span class="sxs-lookup"><span data-stu-id="d8285-146">Apartment-threaded</span></span>  <br/> |<span data-ttu-id="d8285-147">アイドル関数は、MAPI、OLE、または他の COM インターフェイスを使用する場合は、登録したスレッドと同じスレッドで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8285-147">Idle function has to execute on the same thread that registered it if it wants to use MAPI, OLE, or any other COM interfaces.</span></span> <span data-ttu-id="d8285-148">最も簡単な方法は、適切なスレッドにメッセージを投稿するアイドル関数を MAPI に登録し、そのスレッドのメッセージ ループから "実際の" アイドル関数を直接ディスパッチする方法です。</span><span class="sxs-lookup"><span data-stu-id="d8285-148">The most straightforward way is to register an idle function with MAPI that posts a message to the right thread and dispatch the "real" idle function directly from that thread's message loop.</span></span>  <br/> |
   

