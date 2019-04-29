---
title: MAPI アイドルエンジン
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
# <a name="mapi-idle-engine"></a><span data-ttu-id="60ec2-103">MAPI アイドルエンジン</span><span class="sxs-lookup"><span data-stu-id="60ec2-103">MAPI Idle Engine</span></span>

  
  
<span data-ttu-id="60ec2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60ec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60ec2-105">MAPI には、「idle engine」と総称されるいくつかの機能があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-105">MAPI provides several functions that are collectively known as the idle engine.</span></span> <span data-ttu-id="60ec2-106">これらの関数を使用すると、クライアント、アドレス帳プロバイダー、およびメッセージストアプロバイダーは、セッションの遅延時間にさまざまなタスクを実行したり、時間がかかりすぎたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-106">These functions allow clients, address book providers, and message store providers to perform various tasks during slow times in the session or in response to a slow time.</span></span> <span data-ttu-id="60ec2-107">たとえば、クライアントとサービスプロバイダーは低速な操作を延期したり、使用されなくなったファイルを長期間閉じたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-107">For example, clients and service providers can defer slow operations or close files that have remained unused for a lengthy period.</span></span> <span data-ttu-id="60ec2-108">通常、トランスポートプロバイダーは、 **IXPLogon:: idle**メソッドによって実行されるので、アイドルエンジンを使用しません。</span><span class="sxs-lookup"><span data-stu-id="60ec2-108">Transport providers typically do not use the idle engine because the **IXPLogon::Idle** method takes its place.</span></span> <span data-ttu-id="60ec2-109">詳細については、「 [IXPLogon:: Idle](ixplogon-idle.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60ec2-109">For more information, see [IXPLogon::Idle](ixplogon-idle.md).</span></span>
  
<span data-ttu-id="60ec2-110">アイドル状態のエンジンを使用するために、クライアントとサービスプロバイダーは、MAPI サブシステムがアイドル状態のときに実行する必要のあるタスクを含むコールバック関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-110">To use the idle engine, clients and service providers create a callback function that contains the tasks that should occur when the MAPI subsystem is idle.</span></span> <span data-ttu-id="60ec2-111">MAPI がアイドル時間を検出すると、このコールバック関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-111">When MAPI detects idle time, it invokes this callback function.</span></span> <span data-ttu-id="60ec2-112">callback 関数は、次のように定義された**FNIDLE**プロトタイプに従います。</span><span class="sxs-lookup"><span data-stu-id="60ec2-112">The callback function follows the **FNIDLE** prototype, defined as follows:</span></span> 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
<span data-ttu-id="60ec2-113">詳細については、「 [FNIDLE](fnidle.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60ec2-113">For more information, see [FNIDLE](fnidle.md).</span></span>
  
<span data-ttu-id="60ec2-114">アイドル状態のエンジンを構成する関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="60ec2-114">The functions that make up the idle engine are:</span></span>
  
[<span data-ttu-id="60ec2-115">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="60ec2-115">ChangeIdleRoutine</span></span>](changeidleroutine.md)
  
[<span data-ttu-id="60ec2-116">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="60ec2-116">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md)
  
[<span data-ttu-id="60ec2-117">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="60ec2-117">EnableIdleRoutine</span></span>](enableidleroutine.md)
  
[<span data-ttu-id="60ec2-118">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="60ec2-118">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md)
  
[<span data-ttu-id="60ec2-119">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="60ec2-119">MAPIDeInitIdle</span></span>](mapideinitidle.md)
  
[<span data-ttu-id="60ec2-120">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="60ec2-120">MAPIInitIdle</span></span>](mapiinitidle.md)
  
<span data-ttu-id="60ec2-121">コールバック関数を登録するには、クライアントとサービスプロバイダーが**FtgRegisterIdleRoutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-121">To register a callback function, clients and service providers call the **FtgRegisterIdleRoutine** function.</span></span> <span data-ttu-id="60ec2-122">入力パラメーターには、オプションの優先度、入力としてコールバック関数に渡されるメモリブロック、任意の方法で使用される時間、およびオプションフラグのセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-122">The input parameters include an optional priority, a block of memory that is passed to your callback function as input, an amount of time to be used in any way appropriate, and a set of option flags.</span></span> 
  
<span data-ttu-id="60ec2-123">クライアントおよびサービスプロバイダーは、アイドル_状態_の関数の実行方法を制御する優先度を指定するか、優先度が問題でない場合は0を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-123">Clients and service providers can specify a priority in the  _priIdle_ parameter that controls how the idle function runs or specify zero if priority is not an issue.</span></span> <span data-ttu-id="60ec2-124">負の数値は正の数または0より高い優先度を表しているため、圧縮と検索の操作には負の数を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-124">Because negative numbers represent higher priorities than positive numbers or zero, compression and search operations should be assigned negative numbers.</span></span> <span data-ttu-id="60ec2-125">1回発生するタスクには、正の数を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-125">Tasks that occur once should be assigned positive numbers.</span></span> 
  
<span data-ttu-id="60ec2-126">アクティブなコールバック関数を登録解除するために、クライアントとサービスプロバイダーは**DeregisterIdleRoutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-126">To deregister an active callback function, clients and service providers call the **DeregisterIdleRoutine** function.</span></span> <span data-ttu-id="60ec2-127">**DeregisterIdleRoutine**は非同期的に動作するため、登録解除の呼び出し中にコールバック関数を呼び出すことができます。 **DeregisterIdleRoutine**が返された後でも、いつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-127">Because **DeregisterIdleRoutine** operates asynchronously, it is possible for the callback function to be invoked at any time during the deregister call and possibly even after **DeregisterIdleRoutine** has returned.</span></span> 
  
<span data-ttu-id="60ec2-128">コールバック関数の一部またはすべての特性を変更するには、クライアントおよびサービスプロバイダーが**changeidleroutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-128">To modify some or all of the characteristics of a callback function, clients and service providers call the **ChangeIdleRoutine** function.</span></span> <span data-ttu-id="60ec2-129">**changeidleroutine**は、フラグパラメーターが_ircidle_に設定されている方法に従って変更を行います。**changeidleroutine**は、関数自体、その priority、time 設定、および入力パラメーターを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-129">**ChangeIdleRoutine** makes changes according to how the flags parameter  _ircIdle_ is set; **ChangeIdleRoutine** can change the function itself, its priority, time setting, and input parameter.</span></span> 
  
<span data-ttu-id="60ec2-130">オペレーティングシステムに定義がある場合、MAPI はオペレーティングシステムと同じアイドル状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-130">MAPI defines idle the same as the operating system, when the operating system has a definition.</span></span> <span data-ttu-id="60ec2-131">Win32 では、アイドル状態のタスクをスケジュールするために、MAPI がアイドルクラスの優先順位を持つスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-131">On Win32, MAPI creates a thread with idle-class priority to schedule idle tasks.</span></span> <span data-ttu-id="60ec2-132">このスレッドは、時間の追跡を行い、実行時間が到来したときにアイドルタスクを実行するために、スレッドにメッセージを投稿します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-132">This thread keeps track of the time and posts a message to the thread that is to execute the idle task when the time for its execution arrives.</span></span> <span data-ttu-id="60ec2-133">Win32 は、プロセスではなく、スレッドをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="60ec2-133">Win32 schedules threads, not processes.</span></span> <span data-ttu-id="60ec2-134">優先度の高いタスクがワークステーション上で実行されている場合は、タスクが完了するまで、アイドルタスクがスケジュールされないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-134">If tasks that have a priority higher than the idle priority are occurring on the workstation, the idle task should not get scheduled for execution until the tasks have completed.</span></span> 
  
<span data-ttu-id="60ec2-135">すべてのアイドルタスクは、 **MAPIInitIdle**を呼び出したスレッドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-135">All idle tasks run on the thread that called **MAPIInitIdle**.</span></span> <span data-ttu-id="60ec2-136">MAPI は、スケジュール設定に別のスレッドを持っていますが、アイドルタスクが対象となる場合は、初期化スレッドにメッセージをポストバックし、そこでアイドルタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="60ec2-136">MAPI has a separate thread for scheduling, but when an idle task becomes eligible, it posts a message back over to the initialization thread and the idle task is executed there.</span></span> <span data-ttu-id="60ec2-137">クライアントの種類によって、次のような影響があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-137">The implications for different types of clients are as follows.</span></span>
  
|<span data-ttu-id="60ec2-138">**スレッドモデル**</span><span class="sxs-lookup"><span data-stu-id="60ec2-138">**Threading model**</span></span>|<span data-ttu-id="60ec2-139">**暗黙**</span><span class="sxs-lookup"><span data-stu-id="60ec2-139">**Implication**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60ec2-140">シングルスレッド</span><span class="sxs-lookup"><span data-stu-id="60ec2-140">Single-threaded</span></span>  <br/> |<span data-ttu-id="60ec2-141">大丈夫。</span><span class="sxs-lookup"><span data-stu-id="60ec2-141">No problem.</span></span> <span data-ttu-id="60ec2-142">Idle 関数は、クライアントのメインスレッドで実行され、メッセージループを介してシリアル化されます。</span><span class="sxs-lookup"><span data-stu-id="60ec2-142">Idle functions execute on your client's main thread and are serialized through the message loop.</span></span>  <br/> |
|<span data-ttu-id="60ec2-143">フリースレッド</span><span class="sxs-lookup"><span data-stu-id="60ec2-143">Free-threaded</span></span>  <br/> |<span data-ttu-id="60ec2-144">アイドル関数はスレッドセーフである必要がありますが、クライアントには既に必要なインフラストラクチャがあります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-144">Idle functions must be thread-safe, but your client already has the necessary infrastructure.</span></span> <span data-ttu-id="60ec2-145">クライアントでは、MAPI アイドルエンジンがまったく必要ない場合があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-145">Your client might not need the MAPI idle engine at all.</span></span>  <br/> |
|<span data-ttu-id="60ec2-146">アパートメントスレッド</span><span class="sxs-lookup"><span data-stu-id="60ec2-146">Apartment-threaded</span></span>  <br/> |<span data-ttu-id="60ec2-147">アイドル関数は、MAPI、OLE、またはその他の COM インターフェイスを使用する場合に、それを登録したのと同じスレッドで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60ec2-147">Idle function has to execute on the same thread that registered it if it wants to use MAPI, OLE, or any other COM interfaces.</span></span> <span data-ttu-id="60ec2-148">最も簡単な方法は、メッセージを右のスレッドに投稿して、そのスレッドのメッセージループから直接 "real" idle 関数をディスパッチする、MAPI を使用して idle 関数を登録する方法です。</span><span class="sxs-lookup"><span data-stu-id="60ec2-148">The most straightforward way is to register an idle function with MAPI that posts a message to the right thread and dispatch the "real" idle function directly from that thread's message loop.</span></span>  <br/> |
   

