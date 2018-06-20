---
title: MAPI アイドル エンジン
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c535da245be09f930a70c5fae2a892f33087ebf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801384"
---
# <a name="mapi-idle-engine"></a><span data-ttu-id="9f455-103">MAPI アイドル エンジン</span><span class="sxs-lookup"><span data-stu-id="9f455-103">MAPI Idle Engine</span></span>

  
  
<span data-ttu-id="9f455-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f455-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f455-105">MAPI には、アイドル状態のエンジンと総称されますいくつかの関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="9f455-105">MAPI provides several functions that are collectively known as the idle engine.</span></span> <span data-ttu-id="9f455-106">これらの関数は、セッション、または低速に応答のピーク時にさまざまなタスクを実行するには、クライアント、アドレス帳プロバイダー、およびメッセージ ストア プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f455-106">These functions allow clients, address book providers, and message store providers to perform various tasks during slow times in the session or in response to a slow time.</span></span> <span data-ttu-id="9f455-107">クライアントとサービス ・ プロバイダーが遅い操作を延期など、長期間使用されていないままのファイルを閉じる。</span><span class="sxs-lookup"><span data-stu-id="9f455-107">For example, clients and service providers can defer slow operations or close files that have remained unused for a lengthy period.</span></span> <span data-ttu-id="9f455-108">トランスポート プロバイダー通常ために使用しないでアイドル状態のエンジン、 **IXPLogon::Idle**メソッドを引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="9f455-108">Transport providers typically do not use the idle engine because the **IXPLogon::Idle** method takes its place.</span></span> <span data-ttu-id="9f455-109">詳細については、 [IXPLogon::Idle](ixplogon-idle.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f455-109">For more information, see [IXPLogon::Idle](ixplogon-idle.md).</span></span>
  
<span data-ttu-id="9f455-110">アイドル状態のエンジンを使用するには、クライアントとサービス ・ プロバイダーは、MAPI サブシステムがアイドル状態のときに実行するタスクが含まれているコールバック関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="9f455-110">To use the idle engine, clients and service providers create a callback function that contains the tasks that should occur when the MAPI subsystem is idle.</span></span> <span data-ttu-id="9f455-111">MAPI では、アイドル時間を検出すると、このコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f455-111">When MAPI detects idle time, it invokes this callback function.</span></span> <span data-ttu-id="9f455-112">コールバック関数は、次のように定義されている、 **FNIDLE**のプロトタイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="9f455-112">The callback function follows the **FNIDLE** prototype, defined as follows:</span></span> 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
<span data-ttu-id="9f455-113">詳細については、 [FNIDLE](fnidle.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f455-113">For more information, see [FNIDLE](fnidle.md).</span></span>
  
<span data-ttu-id="9f455-114">アイドル状態のエンジンを構成する関数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9f455-114">The functions that make up the idle engine are:</span></span>
  
[<span data-ttu-id="9f455-115">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9f455-115">ChangeIdleRoutine</span></span>](changeidleroutine.md)
  
[<span data-ttu-id="9f455-116">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9f455-116">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md)
  
[<span data-ttu-id="9f455-117">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9f455-117">EnableIdleRoutine</span></span>](enableidleroutine.md)
  
[<span data-ttu-id="9f455-118">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9f455-118">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md)
  
[<span data-ttu-id="9f455-119">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9f455-119">MAPIDeInitIdle</span></span>](mapideinitidle.md)
  
[<span data-ttu-id="9f455-120">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9f455-120">MAPIInitIdle</span></span>](mapiinitidle.md)
  
<span data-ttu-id="9f455-121">コールバック関数を登録するには、クライアントとサービス ・ プロバイダーは、 **FtgRegisterIdleRoutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f455-121">To register a callback function, clients and service providers call the **FtgRegisterIdleRoutine** function.</span></span> <span data-ttu-id="9f455-122">入力パラメーターには、オプションの優先順位、適切な場合は、何らかの方法で使用する時間数の入力値として、コールバック関数に渡されるメモリのブロックが含まれ、オプションのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9f455-122">The input parameters include an optional priority, a block of memory that is passed to your callback function as input, an amount of time to be used in any way appropriate, and a set of option flags.</span></span> 
  
<span data-ttu-id="9f455-123">クライアントとサービス ・ プロバイダー、アイドル状態の関数の実行方法を制御する_priIdle_パラメーターの優先順位を指定したり、優先順位に問題がない場合に 0 を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9f455-123">Clients and service providers can specify a priority in the  _priIdle_ parameter that controls how the idle function runs or specify zero if priority is not an issue.</span></span> <span data-ttu-id="9f455-124">負の数は、正の数または 0 よりも高い優先順位を表す、ため圧縮検索や検索割り当てる必要があります負の数です。</span><span class="sxs-lookup"><span data-stu-id="9f455-124">Because negative numbers represent higher priorities than positive numbers or zero, compression and search operations should be assigned negative numbers.</span></span> <span data-ttu-id="9f455-125">1 回発生する可能性のあるタスクには、正の値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f455-125">Tasks that occur once should be assigned positive numbers.</span></span> 
  
<span data-ttu-id="9f455-126">作業中のコールバック関数の登録を解除するのには、クライアントとサービス ・ プロバイダーは、 **DeregisterIdleRoutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f455-126">To deregister an active callback function, clients and service providers call the **DeregisterIdleRoutine** function.</span></span> <span data-ttu-id="9f455-127">**DeregisterIdleRoutine**は、非同期的に動作するためが登録抹消] の呼び出し中に呼び出されるコールバック関数の可能性があっても**DeregisterIdleRoutine**が返された後できます。</span><span class="sxs-lookup"><span data-stu-id="9f455-127">Because **DeregisterIdleRoutine** operates asynchronously, it is possible for the callback function to be invoked at any time during the deregister call and possibly even after **DeregisterIdleRoutine** has returned.</span></span> 
  
<span data-ttu-id="9f455-128">コールバック関数の特性の一部またはすべてを変更するには、クライアントとサービス ・ プロバイダーは、 **ChangeIdleRoutine**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f455-128">To modify some or all of the characteristics of a callback function, clients and service providers call the **ChangeIdleRoutine** function.</span></span> <span data-ttu-id="9f455-129">**ChangeIdleRoutine**は、変更に応じてフラグ パラメーター _ircIdle_を設定する方法です。**ChangeIdleRoutine**には、関数自体、その優先順位、時間の設定、および入力パラメーターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="9f455-129">**ChangeIdleRoutine** makes changes according to how the flags parameter  _ircIdle_ is set; **ChangeIdleRoutine** can change the function itself, its priority, time setting, and input parameter.</span></span> 
  
<span data-ttu-id="9f455-130">MAPI がアイドル状態を定義、オペレーティング ・ システム、オペレーティング システムには、定義するときと同じです。</span><span class="sxs-lookup"><span data-stu-id="9f455-130">MAPI defines idle the same as the operating system, when the operating system has a definition.</span></span> <span data-ttu-id="9f455-131">Win32 では、MAPI は、アイドル状態のタスクをスケジュールするのには優先順位がアイドル クラスのスレッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f455-131">On Win32, MAPI creates a thread with idle-class priority to schedule idle tasks.</span></span> <span data-ttu-id="9f455-132">このスレッドは、時間の追跡し、到着すると、その実行時間、アイドル状態のタスクを実行するスレッドにメッセージを投稿します。</span><span class="sxs-lookup"><span data-stu-id="9f455-132">This thread keeps track of the time and posts a message to the thread that is to execute the idle task when the time for its execution arrives.</span></span> <span data-ttu-id="9f455-133">Win32 では、スレッドをスケジュール、処理されません。</span><span class="sxs-lookup"><span data-stu-id="9f455-133">Win32 schedules threads, not processes.</span></span> <span data-ttu-id="9f455-134">場合はワークステーションでは、アイドル状態の優先順位よりも高い優先順位のタスクが発生している、アイドル状態のタスク必要がありますいない取得の実行スケジュール タスクが完了するまで。</span><span class="sxs-lookup"><span data-stu-id="9f455-134">If tasks that have a priority higher than the idle priority are occurring on the workstation, the idle task should not get scheduled for execution until the tasks have completed.</span></span> 
  
<span data-ttu-id="9f455-135">**MAPIInitIdle**を呼び出したスレッドのすべてのアイドル タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9f455-135">All idle tasks run on the thread that called **MAPIInitIdle**.</span></span> <span data-ttu-id="9f455-136">MAPI のスケジュールを設定すると、別のスレッドがアイドル状態のタスクは、対象となり、を介して初期化スレッドにメッセージをポストして、アイドル状態のタスクの実行があります。</span><span class="sxs-lookup"><span data-stu-id="9f455-136">MAPI has a separate thread for scheduling, but when an idle task becomes eligible, it posts a message back over to the initialization thread and the idle task is executed there.</span></span> <span data-ttu-id="9f455-137">異なる種類のクライアントに対する影響は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9f455-137">The implications for different types of clients are as follows.</span></span>
  
|<span data-ttu-id="9f455-138">**スレッド モデル**</span><span class="sxs-lookup"><span data-stu-id="9f455-138">**Threading model**</span></span>|<span data-ttu-id="9f455-139">**意味**</span><span class="sxs-lookup"><span data-stu-id="9f455-139">**Implication**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f455-140">シングル スレッド</span><span class="sxs-lookup"><span data-stu-id="9f455-140">Single-threaded</span></span>  <br/> |<span data-ttu-id="9f455-141">大丈夫。</span><span class="sxs-lookup"><span data-stu-id="9f455-141">No problem.</span></span> <span data-ttu-id="9f455-142">アイドル関数では、クライアントのメイン スレッド上で実行し、メッセージ ループをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="9f455-142">Idle functions execute on your client's main thread and are serialized through the message loop.</span></span>  <br/> |
|<span data-ttu-id="9f455-143">フリー スレッド</span><span class="sxs-lookup"><span data-stu-id="9f455-143">Free-threaded</span></span>  <br/> |<span data-ttu-id="9f455-144">アイドル状態の関数はスレッド セーフである必要がありますが、クライアントが既に必要なインフラストラクチャです。</span><span class="sxs-lookup"><span data-stu-id="9f455-144">Idle functions must be thread-safe, but your client already has the necessary infrastructure.</span></span> <span data-ttu-id="9f455-145">クライアントは可能性があります MAPI アイドル エンジンをまったく必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9f455-145">Your client might not need the MAPI idle engine at all.</span></span>  <br/> |
|<span data-ttu-id="9f455-146">アパートメント スレッド</span><span class="sxs-lookup"><span data-stu-id="9f455-146">Apartment-threaded</span></span>  <br/> |<span data-ttu-id="9f455-147">アイドル状態の関数は、MAPI、OLE、またはその他の任意の COM インターフェイスを使用する必要がある場合は、登録されている同じスレッドで実行すること。</span><span class="sxs-lookup"><span data-stu-id="9f455-147">Idle function has to execute on the same thread that registered it if it wants to use MAPI, OLE, or any other COM interfaces.</span></span> <span data-ttu-id="9f455-148">最も簡単な方法は、MAPI スレッドを適切にメッセージを投稿すると、アイドル状態の関数を登録し、そのスレッドのメッセージ ループから直接「実際の」アイドル状態の関数にディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="9f455-148">The most straightforward way is to register an idle function with MAPI that posts a message to the right thread and dispatch the "real" idle function directly from that thread's message loop.</span></span>  <br/> |
   

