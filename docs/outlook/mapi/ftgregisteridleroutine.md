---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418522"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="59b6a-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="59b6a-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="59b6a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59b6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59b6a-105">MAPI システム [に FNIDLE](fnidle.md) 関数ベースのアイドル ルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59b6a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="59b6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="59b6a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="59b6a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="59b6a-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="59b6a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="59b6a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="59b6a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="59b6a-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="59b6a-110">Called by:</span></span>  <br/> |<span data-ttu-id="59b6a-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="59b6a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="59b6a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59b6a-112">Parameters</span></span>

<span data-ttu-id="59b6a-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="59b6a-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="59b6a-114">[in]アイドル 状態のルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="59b6a-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="59b6a-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="59b6a-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="59b6a-116">[in]アイドル エンジンが呼び出し時に、アイドル 状態のルーチンにパラメーターとして渡す必要があるメモリ ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="59b6a-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="59b6a-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="59b6a-117">_priIdle_</span></span>
  
> <span data-ttu-id="59b6a-118">[in]アイドル 状態のルーチンの最初の優先度。</span><span class="sxs-lookup"><span data-stu-id="59b6a-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="59b6a-119">実装定義ルーチンで考えられる優先順位は、0 より大きいか、0 未満です。</span><span class="sxs-lookup"><span data-stu-id="59b6a-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="59b6a-120">0 の優先度は、マウスクリックやメッセージメッセージなどのユーザー イベントWM_PAINTされます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="59b6a-121">優先度が 0 より大きい場合は、ユーザー イベントよりも優先度が高く、メッセージ ポンプ の標準ループの一部Windowsバックグラウンド タスクを表します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="59b6a-122">優先度が 0 未満の場合は、メッセージ ポンプのアイドル時間中にのみ実行されるアイドル タスクを表します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="59b6a-123">優先順位の例は、フォアグラウンド申請の場合は 1、電源編集文字の挿入には 2、新しいメッセージをダウンロードする場合は 3 です。</span><span class="sxs-lookup"><span data-stu-id="59b6a-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="59b6a-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="59b6a-124">_csecIdle_</span></span>
  
> <span data-ttu-id="59b6a-125">[in]アイドル 状態のルーチン パラメーターを指定する場合に使用する初期時間値 (100 分の 1 秒)。</span><span class="sxs-lookup"><span data-stu-id="59b6a-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="59b6a-126">初期時間の値の意味は  _、iroIdle_ パラメーターで渡される内容に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="59b6a-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="59b6a-127">意味は、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="59b6a-128">FIROWAIT フラグが  _iroIdle_ に設定されている場合、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間。</span><span class="sxs-lookup"><span data-stu-id="59b6a-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="59b6a-129">この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59b6a-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="59b6a-130">FIROINTERVAL フラグが  _iroIdle_ で設定されている場合、アイドル 状態のルーチンへの呼び出しの最小間隔。</span><span class="sxs-lookup"><span data-stu-id="59b6a-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="59b6a-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="59b6a-131">_iroIdle_</span></span>
  
> <span data-ttu-id="59b6a-132">[in]アイドル ルーチンの初期オプションを設定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="59b6a-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="59b6a-133">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="59b6a-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="59b6a-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="59b6a-135">このフラグを使用して、アイドル 状態のルーチン タイマーをスリープまたは再開に合わせて調整しなけれと指定します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="59b6a-136">このフラグのない既定の動作は、経過時間の計算時にスリープ時間が除外されます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="59b6a-137">FIRONOADJUSTMENT が渡された場合、経過時間の計算時にスリープ時間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="59b6a-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="59b6a-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="59b6a-139">登録時にアイドル ルーチンを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="59b6a-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="59b6a-140">既定のアクションは **、FtgRegisterIdleRoutine** が登録するときにアイドル ルーチンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="59b6a-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="59b6a-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="59b6a-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="59b6a-142">_csecIdle_ パラメーターで指定される時間は、アイドル ルーチンへの連続する呼び出しの最小間隔です。</span><span class="sxs-lookup"><span data-stu-id="59b6a-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="59b6a-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="59b6a-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="59b6a-p107">現在使用されていません。使用しないでください。 </span><span class="sxs-lookup"><span data-stu-id="59b6a-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="59b6a-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="59b6a-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="59b6a-p108">現在使用されていません。使用しないでください。 </span><span class="sxs-lookup"><span data-stu-id="59b6a-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="59b6a-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="59b6a-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="59b6a-150">_csecIdle_ パラメーターで指定される時間は、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間です。</span><span class="sxs-lookup"><span data-stu-id="59b6a-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="59b6a-151">この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59b6a-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="59b6a-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="59b6a-152">Return value</span></span>

<span data-ttu-id="59b6a-153">**FtgRegisterIdleRoutine** 関数は、MAPI システムに追加されたアイドル ルーチンを識別する関数タグを返します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="59b6a-154">**FtgRegisterIdleRoutine** が、メモリの問題などのためにクライアント アプリケーションまたはサービス プロバイダーのアイドル ルーチンを登録できない場合は、NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="59b6a-155">注釈</span><span class="sxs-lookup"><span data-stu-id="59b6a-155">Remarks</span></span>

<span data-ttu-id="59b6a-156">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="59b6a-157">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="59b6a-157">**Idle routine function**</span></span>|<span data-ttu-id="59b6a-158">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="59b6a-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59b6a-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="59b6a-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="59b6a-160">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="59b6a-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="59b6a-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="59b6a-162">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="59b6a-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="59b6a-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="59b6a-164">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="59b6a-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="59b6a-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="59b6a-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="59b6a-166">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="59b6a-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="59b6a-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="59b6a-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="59b6a-168">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="59b6a-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="59b6a-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="59b6a-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="59b6a-170">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="59b6a-171">**ChangeIdleRoutine** **、DeregisterIdleRoutine、\*\*\*\*および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="59b6a-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="59b6a-172">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="59b6a-173">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="59b6a-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="59b6a-174">iroIdle パラメーターで FIRONOADJUSTMENT フラグを使用する例  _を次に示_ します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="59b6a-175">5 分の遅延でアイドル 状態のルーチンを登録します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="59b6a-176">休止状態/1 分後にコンピューターをスリープ状態 (タイマーの残り 4 分)。</span><span class="sxs-lookup"><span data-stu-id="59b6a-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="59b6a-177">10 分後にコンピューターを再開します。</span><span class="sxs-lookup"><span data-stu-id="59b6a-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="59b6a-178">FIRONOADJUSTMENT を使用しない既定の動作は、ルーチンが実行するまでにさらに 4 分待機する必要があるという点です。</span><span class="sxs-lookup"><span data-stu-id="59b6a-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="59b6a-179">つまり、タイマーが調整され、コンピューターがスリープ状態にされた時間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="59b6a-180">ただし、FIRONOADJUSTMENT に合格すると、5 分以上のリアルタイムが経過したため、アイドル ルーチンはすぐに実行されます。</span><span class="sxs-lookup"><span data-stu-id="59b6a-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

