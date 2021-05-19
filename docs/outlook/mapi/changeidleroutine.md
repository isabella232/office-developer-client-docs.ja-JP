---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418268"
---
# <a name="changeidleroutine"></a><span data-ttu-id="f006b-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f006b-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="f006b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f006b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f006b-105">[FNIDLE](fnidle.md)ベースのアイドル ルーチンの特性の一部またはすべてが変更されます。</span><span class="sxs-lookup"><span data-stu-id="f006b-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f006b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f006b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f006b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f006b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f006b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f006b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f006b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f006b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f006b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f006b-110">Called by:</span></span>  <br/> |<span data-ttu-id="f006b-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f006b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="f006b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f006b-112">Parameters</span></span>

<span data-ttu-id="f006b-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="f006b-113">_ftg_</span></span>
  
> <span data-ttu-id="f006b-114">[in]アイドル ルーチンを識別する関数タグ。</span><span class="sxs-lookup"><span data-stu-id="f006b-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="f006b-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="f006b-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="f006b-116">[in]アイドル 状態のルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f006b-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="f006b-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="f006b-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="f006b-118">[in]呼び出し元の実装がアイドル ルーチンに割り当てる新しいメモリ ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f006b-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="f006b-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="f006b-119">_priIdle_</span></span>
  
> <span data-ttu-id="f006b-120">[in]アイドル ルーチンの新しい優先度を表す値。</span><span class="sxs-lookup"><span data-stu-id="f006b-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="f006b-121">実装定義ルーチンで考えられる優先順位は、0 より大きいか、0 未満です。</span><span class="sxs-lookup"><span data-stu-id="f006b-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="f006b-122">値 0 は、マウスクリックやメッセージメッセージなどのユーザー イベントWM_PAINTされます。</span><span class="sxs-lookup"><span data-stu-id="f006b-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="f006b-123">0 より大きい値は、ユーザー イベントよりも優先度が高く、メッセージ ポンプ の標準ループの一部としてディスパッチされるバックグラウンド タスクWindows表します。</span><span class="sxs-lookup"><span data-stu-id="f006b-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="f006b-124">0 未満の値は、メッセージ ポンプアイドル時間中にのみ実行されるアイドル タスクの優先順位を表します。</span><span class="sxs-lookup"><span data-stu-id="f006b-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="f006b-125">優先順位の例としては、フォアグラウンド申請の場合は 1、電源編集文字の挿入には 1、新しいメッセージをダウンロードする場合は 3 です。</span><span class="sxs-lookup"><span data-stu-id="f006b-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="f006b-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="f006b-126">_csecIdle_</span></span>
  
> <span data-ttu-id="f006b-127">[in]アイドル 状態のルーチンに適用する新しい時刻 (100 分の 1 秒)。</span><span class="sxs-lookup"><span data-stu-id="f006b-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="f006b-128">初期時間の値の意味は  _、iroIdle_ パラメーターで渡される内容に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="f006b-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="f006b-129">次の場合があります。</span><span class="sxs-lookup"><span data-stu-id="f006b-129">It can be:</span></span> 
    
  - <span data-ttu-id="f006b-130">FIROWAIT フラグが  _iroIdle_ に設定されている場合、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間。</span><span class="sxs-lookup"><span data-stu-id="f006b-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="f006b-131">この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f006b-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="f006b-132">FIROINTERVAL フラグが  _iroIdle_ で設定されている場合、アイドル 状態のルーチンへの呼び出しの最小間隔。</span><span class="sxs-lookup"><span data-stu-id="f006b-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="f006b-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="f006b-133">_iroIdle_</span></span>
  
> <span data-ttu-id="f006b-134">[in]アイドル ルーチンを呼び出す新しいオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f006b-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="f006b-135">次のいずれかのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f006b-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="f006b-136">FIROINTERVAL:  _csecIdle_ パラメーターで指定される時間は、アイドル ルーチンへの連続する呼び出しの最小間隔です。</span><span class="sxs-lookup"><span data-stu-id="f006b-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="f006b-137">FIROONCEONLY: 廃止。</span><span class="sxs-lookup"><span data-stu-id="f006b-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="f006b-138">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f006b-138">Do not use.</span></span> 
      
  - <span data-ttu-id="f006b-139">FIROPERBLOCK: 廃止。</span><span class="sxs-lookup"><span data-stu-id="f006b-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="f006b-140">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f006b-140">Do not use.</span></span> 
      
  - <span data-ttu-id="f006b-141">FIROWAIT:  _csecIdle_ パラメーターで指定された時間は、MAPI アイドル エンジンがアイドル ルーチンを初めて呼び出す前に経過する必要があるユーザーの不作為の最小期間です。</span><span class="sxs-lookup"><span data-stu-id="f006b-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="f006b-142">この時間が経過すると、アイドル エンジンは必要な頻度でアイドル ルーチンを呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f006b-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="f006b-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="f006b-143">_ircIdle_</span></span>
  
> <span data-ttu-id="f006b-144">[in]アイドル ルーチンに加える変更を示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f006b-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="f006b-145">次のフラグは、任意の組み合わせで設定できます。</span><span class="sxs-lookup"><span data-stu-id="f006b-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="f006b-146">FIRCCSEC: アイドル ルーチンに関連付けられた時刻の変更、つまり  _、csecIdle_ パラメーターで渡された値によって示される変更。</span><span class="sxs-lookup"><span data-stu-id="f006b-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="f006b-147">FIRCIRO: アイドル ルーチンのオプション (  _つまり、iroIdle_ パラメーターで渡された値によって示される変更) の変更。</span><span class="sxs-lookup"><span data-stu-id="f006b-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="f006b-148">FIRCPFN: アイドル 状態のルーチン ポインター 、つまり  _pfnIdle_ パラメーターで渡された値によって示される変更を変更します。</span><span class="sxs-lookup"><span data-stu-id="f006b-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="f006b-149">FIRCPRI: アイドル ルーチンの優先度に対する変更、つまり  _、priIdle_ パラメーターで渡された値によって示される変更。</span><span class="sxs-lookup"><span data-stu-id="f006b-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="f006b-150">FIRCPV: アイドル ルーチンのメモリ ブロックへの変更、つまり  _、pvIdleParam_ パラメーターで渡された値によって示される変更。</span><span class="sxs-lookup"><span data-stu-id="f006b-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f006b-151">Return value</span><span class="sxs-lookup"><span data-stu-id="f006b-151">Return value</span></span>

<span data-ttu-id="f006b-152">なし。</span><span class="sxs-lookup"><span data-stu-id="f006b-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f006b-153">注釈</span><span class="sxs-lookup"><span data-stu-id="f006b-153">Remarks</span></span>

<span data-ttu-id="f006b-154">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="f006b-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="f006b-155">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="f006b-155">**Idle routine function**</span></span>|<span data-ttu-id="f006b-156">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="f006b-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f006b-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="f006b-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="f006b-158">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="f006b-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="f006b-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f006b-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="f006b-160">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="f006b-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f006b-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f006b-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="f006b-162">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="f006b-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="f006b-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="f006b-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="f006b-164">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="f006b-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="f006b-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="f006b-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="f006b-166">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="f006b-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="f006b-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="f006b-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="f006b-168">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f006b-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="f006b-169">**ChangeIdleRoutine** **、DeregisterIdleRoutine、\*\*\*\*および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="f006b-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="f006b-170">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f006b-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="f006b-171">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="f006b-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

