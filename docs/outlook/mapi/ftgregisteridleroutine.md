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
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="d5608-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d5608-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="d5608-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5608-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5608-105">[FNIDLE](fnidle.md)関数ベースのアイドルルーチンを MAPI システムに追加します。</span><span class="sxs-lookup"><span data-stu-id="d5608-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5608-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d5608-106">Header file:</span></span>  <br/> |<span data-ttu-id="d5608-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="d5608-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d5608-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d5608-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5608-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d5608-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d5608-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d5608-110">Called by:</span></span>  <br/> |<span data-ttu-id="d5608-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d5608-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="d5608-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5608-112">Parameters</span></span>

<span data-ttu-id="d5608-113">_pfnidle_</span><span class="sxs-lookup"><span data-stu-id="d5608-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="d5608-114">順番アイドルルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5608-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="d5608-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="d5608-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="d5608-116">順番アイドル状態のエンジンが、その呼び出し時にアイドルルーチンにパラメーターとして渡す必要があるメモリブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5608-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="d5608-117">_アイドル状態_</span><span class="sxs-lookup"><span data-stu-id="d5608-117">_priIdle_</span></span>
  
> <span data-ttu-id="d5608-118">順番アイドルルーチンの初期優先度。</span><span class="sxs-lookup"><span data-stu-id="d5608-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="d5608-119">実装で定義されているルーチンの優先度は、0より大きい、または0より小さいです。</span><span class="sxs-lookup"><span data-stu-id="d5608-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="d5608-120">優先度0は、マウスクリックや WM_PAINT メッセージなどのユーザーイベント用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="d5608-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="d5608-121">0より大きい優先度は、ユーザーイベントより高い優先度を持つバックグラウンドタスクを表し、標準の Windows メッセージポンプループの一部としてディスパッチされます。</span><span class="sxs-lookup"><span data-stu-id="d5608-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="d5608-122">0未満の優先度は、メッセージポンプのアイドル時間にのみ実行されるアイドルタスクを表します。</span><span class="sxs-lookup"><span data-stu-id="d5608-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="d5608-123">優先度の例は、フォアグラウンド送信の場合は1、power edit 文字の挿入の場合は2、新しいメッセージをダウンロードする場合は3です。</span><span class="sxs-lookup"><span data-stu-id="d5608-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="d5608-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="d5608-124">_csecIdle_</span></span>
  
> <span data-ttu-id="d5608-125">順番アイドルルーチンパラメーターの指定に使用される初期時間値 (1/100 秒単位)。</span><span class="sxs-lookup"><span data-stu-id="d5608-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="d5608-126">最初の時刻の値の意味は、 _iroIdle_パラメーターで渡された内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d5608-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="d5608-127">この意味には、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d5608-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="d5608-128">_iroIdle_で firowait フラグが設定されている場合に、MAPI idle engine が最初にアイドルルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間。</span><span class="sxs-lookup"><span data-stu-id="d5608-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="d5608-129">この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d5608-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="d5608-130">_iroIdle_で firointerval フラグが設定されている場合に、アイドルルーチンへの呼び出しの最小間隔。</span><span class="sxs-lookup"><span data-stu-id="d5608-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="d5608-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="d5608-131">_iroIdle_</span></span>
  
> <span data-ttu-id="d5608-132">順番アイドルルーチンの初期オプションを設定するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d5608-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="d5608-133">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d5608-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="d5608-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="d5608-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="d5608-135">このフラグを使用して、アイドルルーチンタイマーをスリープまたは再開に調整しないように指定します。</span><span class="sxs-lookup"><span data-stu-id="d5608-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="d5608-136">このフラグを使用しない既定の動作では、経過時間の計算時にスリープ時間が除外されます。</span><span class="sxs-lookup"><span data-stu-id="d5608-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="d5608-137">FIRONOADJUSTMENT が渡された場合、経過時間を計算するときにスリープ時間が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5608-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="d5608-138">firodisabled</span><span class="sxs-lookup"><span data-stu-id="d5608-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="d5608-139">登録時にアイドルルーチンを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5608-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="d5608-140">既定のアクションは、 **FtgRegisterIdleRoutine**が登録時に idle ルーチンを有効にすることです。</span><span class="sxs-lookup"><span data-stu-id="d5608-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="d5608-141">firointerval</span><span class="sxs-lookup"><span data-stu-id="d5608-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="d5608-142">_csecIdle_パラメーターによって指定された時間は、アイドルルーチンへの連続する呼び出し間の最小間隔です。</span><span class="sxs-lookup"><span data-stu-id="d5608-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="d5608-143">firoonly のみ</span><span class="sxs-lookup"><span data-stu-id="d5608-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="d5608-144">使用されていません。</span><span class="sxs-lookup"><span data-stu-id="d5608-144">Obsolete.</span></span> <span data-ttu-id="d5608-145">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d5608-145">Do not use.</span></span> 
      
  <span data-ttu-id="d5608-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="d5608-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="d5608-147">使用されていません。</span><span class="sxs-lookup"><span data-stu-id="d5608-147">Obsolete.</span></span> <span data-ttu-id="d5608-148">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d5608-148">Do not use.</span></span> 
      
  <span data-ttu-id="d5608-149">firowait</span><span class="sxs-lookup"><span data-stu-id="d5608-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="d5608-150">_csecIdle_パラメーターによって指定された時間は、ユーザーが最初にアイドル状態のルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間です。</span><span class="sxs-lookup"><span data-stu-id="d5608-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="d5608-151">この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d5608-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d5608-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5608-152">Return value</span></span>

<span data-ttu-id="d5608-153">**FtgRegisterIdleRoutine**関数は、MAPI システムに追加された idle ルーチンを識別する関数タグを返します。</span><span class="sxs-lookup"><span data-stu-id="d5608-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="d5608-154">**FtgRegisterIdleRoutine**が、メモリの問題などのために、クライアントアプリケーションまたはサービスプロバイダーの idle ルーチンを登録できない場合は、NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="d5608-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d5608-155">注釈</span><span class="sxs-lookup"><span data-stu-id="d5608-155">Remarks</span></span>

<span data-ttu-id="d5608-156">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドル状態のルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="d5608-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="d5608-157">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="d5608-157">**Idle routine function**</span></span>|<span data-ttu-id="d5608-158">**使用法**</span><span class="sxs-lookup"><span data-stu-id="d5608-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5608-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d5608-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d5608-160">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="d5608-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d5608-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d5608-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d5608-162">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="d5608-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d5608-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d5608-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d5608-164">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="d5608-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="d5608-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="d5608-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="d5608-166">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="d5608-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d5608-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d5608-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d5608-168">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="d5608-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d5608-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d5608-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d5608-170">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5608-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d5608-171">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d5608-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="d5608-172">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5608-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d5608-173">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="d5608-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="d5608-174">_iroIdle_パラメーターで FIRONOADJUSTMENT フラグを使用する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d5608-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="d5608-175">アイドルルーチンに5分の遅延を登録します。</span><span class="sxs-lookup"><span data-stu-id="d5608-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="d5608-176">休止/コンピューターを1分後 (タイマーの左から4分) にします。</span><span class="sxs-lookup"><span data-stu-id="d5608-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="d5608-177">コンピューターを10分後に再開します。</span><span class="sxs-lookup"><span data-stu-id="d5608-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="d5608-178">FIRONOADJUSTMENT を使用しない既定の動作では、ルーチンが実行されるまでに4分間待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5608-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="d5608-179">つまり、タイマーは、コンピューターがスリープ状態になっていた時間を確保するように調整されています。</span><span class="sxs-lookup"><span data-stu-id="d5608-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="d5608-180">ただし、FIRONOADJUSTMENT を渡した場合、アイドルルーチンは、リアルタイムが5分以上経過したため、直ちに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d5608-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

