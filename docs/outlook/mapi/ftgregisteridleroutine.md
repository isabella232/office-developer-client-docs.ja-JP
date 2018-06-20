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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800139"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="3b1c2-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b1c2-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="3b1c2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b1c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b1c2-105">MAPI システムには、 [FNIDLE](fnidle.md)関数に基づくアイドル ルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b1c2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3b1c2-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b1c2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3b1c2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3b1c2-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b1c2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b1c2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b1c2-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-110">Called by:</span></span>  <br/> |<span data-ttu-id="3b1c2-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3b1c2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="3b1c2-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="3b1c2-112">Parameters</span></span>

<span data-ttu-id="3b1c2-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="3b1c2-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="3b1c2-114">[in]アイドル ルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="3b1c2-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="3b1c2-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="3b1c2-116">[in]アイドル状態のエンジンは、アイドル ルーチンにそれを呼び出すときで、パラメーターとして渡す必要があるメモリ ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="3b1c2-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="3b1c2-117">_priIdle_</span></span>
  
> <span data-ttu-id="3b1c2-118">[in]アイドル ルーチンの最初の優先順位です。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="3b1c2-119">ルーチンの実装で定義可能な優先度よりも大きいか小さいは、0 が 0 ではありません。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="3b1c2-120">0 の優先順位は、マウスのクリックや、WM_PAINT メッセージなどのユーザー イベントに予約されています。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="3b1c2-121">優先度が 0 より大きい値は、ユーザー イベントよりも優先順位が高いと、Windows メッセージ ポンプの標準的なループの一部としてディスパッチをバック グラウンド タスクを表します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="3b1c2-122">0 より小さい値の優先順位は、メッセージ ポンプのアイドル時間中にのみ実行しているアイドル状態のタスクを表します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="3b1c2-123">優先順位の例としては次のとおり: フォア グラウンドの提出書類の 1、2 電源編集文字の挿入、および 3 の新しいメッセージをダウンロードするためです。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="3b1c2-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="3b1c2-124">_csecIdle_</span></span>
  
> <span data-ttu-id="3b1c2-125">[in]初期の時間の値を 100 分の 1 秒間、アイドル状態の日常的なパラメーターを指定するときに使用します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="3b1c2-126">初期時刻の値の意味は、 _iroIdle_パラメーターに渡される内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="3b1c2-127">意味には、次のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="3b1c2-128">ユーザー何もしなかったため、MAPI の前に、までに必要な最小期間アイドル状態のエンジン ルーチンを呼び出すとアイドルを最初に、 _iroIdle_に FIROWAIT フラグが設定されている場合。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="3b1c2-129">この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="3b1c2-130">_IroIdle_に FIROINTERVAL フラグが設定されている場合、アイドル状態のルーチンへの呼び出しの間の最小間隔。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="3b1c2-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="3b1c2-131">_iroIdle_</span></span>
  
> <span data-ttu-id="3b1c2-132">[in]アイドル ルーチンの最初のオプションを設定するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="3b1c2-133">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="3b1c2-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="3b1c2-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="3b1c2-135">スリープのアイドル状態の定期的なタイマーを調整しないことを指定するのにはこのフラグを使用して停止または再開します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="3b1c2-136">このフラグを設定しないデフォルトの動作では、経過時間を計算するときに、スリープ時間を除外します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="3b1c2-137">FIRONOADJUSTMENT が渡された場合、スリープ時間は含まれている経過時間を計算する場合です。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="3b1c2-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="3b1c2-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="3b1c2-139">登録されている場合は、アイドル状態のルーチンを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="3b1c2-140">既定のアクションは、 **FtgRegisterIdleRoutine**がそれを登録すると、アイドル状態のルーチンを有効にするのには。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="3b1c2-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="3b1c2-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="3b1c2-142">_CsecIdle_パラメーターによって指定される時間は、アイドル状態のルーチンへの連続呼び出しの間の最小の間隔です。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="3b1c2-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="3b1c2-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="3b1c2-p107">現在使用されていません。使用しないでください。 </span><span class="sxs-lookup"><span data-stu-id="3b1c2-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="3b1c2-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="3b1c2-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="3b1c2-p108">現在使用されていません。使用しないでください。 </span><span class="sxs-lookup"><span data-stu-id="3b1c2-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="3b1c2-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="3b1c2-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="3b1c2-150">_CsecIdle_パラメーターによって指定される時間は、ユーザー何もしなかったため、MAPI アイドル エンジンは、最初にアイドル ルーチンを呼び出す前に必要な経過時間の最小期間です。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="3b1c2-151">この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b1c2-152">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3b1c2-152">Return value</span></span>

<span data-ttu-id="3b1c2-153">**FtgRegisterIdleRoutine**関数では、MAPI システムに追加されたアイドル ルーチンを識別する関数のタグを取得します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="3b1c2-154">**FtgRegisterIdleRoutine**は、クライアント アプリケーションまたはサービス プロバイダーのアイドル状態のルーチンを登録できません、する場合は、メモリの問題のため NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b1c2-155">備考</span><span class="sxs-lookup"><span data-stu-id="3b1c2-155">Remarks</span></span>

<span data-ttu-id="3b1c2-156">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを扱います。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="3b1c2-157">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="3b1c2-157">**Idle routine function**</span></span>|<span data-ttu-id="3b1c2-158">**使用例**</span><span class="sxs-lookup"><span data-stu-id="3b1c2-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b1c2-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b1c2-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="3b1c2-160">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="3b1c2-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b1c2-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="3b1c2-162">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3b1c2-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3b1c2-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="3b1c2-164">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="3b1c2-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="3b1c2-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="3b1c2-166">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="3b1c2-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="3b1c2-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="3b1c2-168">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="3b1c2-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="3b1c2-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="3b1c2-170">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="3b1c2-171">**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="3b1c2-172">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="3b1c2-173">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="3b1c2-174">次は、 _iroIdle_パラメーターに FIRONOADJUSTMENT フラグを使用する場合の例です。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="3b1c2-175">5 分遅れで、アイドル状態のルーチンを登録します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="3b1c2-176">休止状態やスリープ、コンピューター後 1 分 (4 分のタイマーのまま)。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="3b1c2-177">10 分後、コンピューターを再開します。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="3b1c2-178">FIRONOADJUSTMENT、せず、既定の動作では、4 分のルーチンを実行するを待機する必要がまだします。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="3b1c2-179">タイマーは、コンピューターがスリープする時間をできるように調整されました。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="3b1c2-180">ただし、FIRONOADJUSTMENT に合格した場合、アイドル ルーチンが実行直後にリアルタイムの 5 分以上が経過したためです。</span><span class="sxs-lookup"><span data-stu-id="3b1c2-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

