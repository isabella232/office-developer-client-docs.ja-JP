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
# <a name="changeidleroutine"></a><span data-ttu-id="3602d-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3602d-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="3602d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3602d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3602d-105">[FNIDLE](fnidle.md)ベースのアイドルルーチンの一部またはすべての特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="3602d-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3602d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3602d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3602d-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="3602d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3602d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="3602d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3602d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3602d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3602d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3602d-110">Called by:</span></span>  <br/> |<span data-ttu-id="3602d-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3602d-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="3602d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3602d-112">Parameters</span></span>

<span data-ttu-id="3602d-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="3602d-113">_ftg_</span></span>
  
> <span data-ttu-id="3602d-114">順番idle ルーチンを識別する Function タグ。</span><span class="sxs-lookup"><span data-stu-id="3602d-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="3602d-115">_pfnidle_</span><span class="sxs-lookup"><span data-stu-id="3602d-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="3602d-116">順番アイドルルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3602d-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="3602d-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="3602d-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="3602d-118">順番呼び出し側の実装によってアイドルルーチンに対して割り当てられる新しいメモリブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3602d-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="3602d-119">_アイドル状態_</span><span class="sxs-lookup"><span data-stu-id="3602d-119">_priIdle_</span></span>
  
> <span data-ttu-id="3602d-120">順番アイドルルーチンの新しい優先度を表す値。</span><span class="sxs-lookup"><span data-stu-id="3602d-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="3602d-121">実装で定義されているルーチンの優先度は、0より大きい、または0より小さいです。</span><span class="sxs-lookup"><span data-stu-id="3602d-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="3602d-122">0の値は、マウスのクリックや WM_PAINT メッセージなどのユーザーイベントに対して予約されています。</span><span class="sxs-lookup"><span data-stu-id="3602d-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="3602d-123">0より大きい値は、ユーザーイベントより高い優先度を持つバックグラウンドタスクの優先度を表し、標準の Windows メッセージポンプループの一部としてディスパッチされます。</span><span class="sxs-lookup"><span data-stu-id="3602d-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="3602d-124">0未満の値は、メッセージポンプアイドル時間中にのみ実行されるアイドルタスクの優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="3602d-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="3602d-125">優先度の例は、フォアグラウンド送信の場合は1、power edit 文字の挿入の場合は1、新しいメッセージをダウンロードする場合は3です。</span><span class="sxs-lookup"><span data-stu-id="3602d-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="3602d-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="3602d-126">_csecIdle_</span></span>
  
> <span data-ttu-id="3602d-127">順番アイドルルーチンに適用する新しい時間 (1/100 秒単位)。</span><span class="sxs-lookup"><span data-stu-id="3602d-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="3602d-128">最初の時刻の値の意味は、 _iroIdle_パラメーターで渡された内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="3602d-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="3602d-129">次のことが可能です。</span><span class="sxs-lookup"><span data-stu-id="3602d-129">It can be:</span></span> 
    
  - <span data-ttu-id="3602d-130">_iroIdle_で firowait フラグが設定されている場合に、MAPI idle engine が最初にアイドルルーチンを呼び出すまでに経過する必要がある、ユーザーの最小処理時間。</span><span class="sxs-lookup"><span data-stu-id="3602d-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="3602d-131">この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3602d-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="3602d-132">_iroIdle_で firointerval フラグが設定されている場合に、アイドルルーチンへの呼び出しの最小間隔。</span><span class="sxs-lookup"><span data-stu-id="3602d-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="3602d-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="3602d-133">_iroIdle_</span></span>
  
> <span data-ttu-id="3602d-134">順番アイドルルーチンを呼び出すための新しいオプションを示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3602d-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="3602d-135">次のフラグのいずれかを正確に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3602d-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="3602d-136">firointerval: _csecIdle_パラメーターで指定された時間は、アイドルルーチンへの連続する呼び出し間の最小間隔です。</span><span class="sxs-lookup"><span data-stu-id="3602d-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="3602d-137">firoonly: Obsolete。</span><span class="sxs-lookup"><span data-stu-id="3602d-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="3602d-138">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3602d-138">Do not use.</span></span> 
      
  - <span data-ttu-id="3602d-139">FIROPERBLOCK: 廃止。</span><span class="sxs-lookup"><span data-stu-id="3602d-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="3602d-140">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3602d-140">Do not use.</span></span> 
      
  - <span data-ttu-id="3602d-141">firowait: _csecIdle_パラメーターで指定された時間は、MAPI アイドルエンジンが最初にアイドルルーチンを呼び出す前に経過する必要がある、ユーザーの最小処理時間です。</span><span class="sxs-lookup"><span data-stu-id="3602d-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="3602d-142">この時間が経過すると、アイドル状態のエンジンは、必要に応じて頻度の高いルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3602d-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="3602d-143">_ircidle_</span><span class="sxs-lookup"><span data-stu-id="3602d-143">_ircIdle_</span></span>
  
> <span data-ttu-id="3602d-144">順番アイドルルーチンに加えられる変更を示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3602d-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="3602d-145">次のフラグは、任意の組み合わせで設定できます。</span><span class="sxs-lookup"><span data-stu-id="3602d-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="3602d-146">[ファイヤ ccsec]: idle ルーチンに関連付けられている時間、つまり、 _csecIdle_パラメーターで渡された値によって示される変更点に対する変更。</span><span class="sxs-lookup"><span data-stu-id="3602d-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="3602d-147">_iroIdle_パラメーターで渡された値によって示される変更である、アイドルルーチンのオプションに対する変更。</span><span class="sxs-lookup"><span data-stu-id="3602d-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="3602d-148">[ファイヤ cpfn]: idle ルーチンポインターへの変更 (つまり、 _pfnidle_パラメーターに渡された値によって示される変更)。</span><span class="sxs-lookup"><span data-stu-id="3602d-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="3602d-149">[ファイヤ cpri]: idle _idle_パラメーターで渡された値によって示される変更である、アイドルルーチンの優先度の変更。</span><span class="sxs-lookup"><span data-stu-id="3602d-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="3602d-150">[ファイヤ cpv]: idle ルーチンのメモリブロックに対する変更 (つまり、 _pvIdleParam_パラメータで渡された値によって示される変更)。</span><span class="sxs-lookup"><span data-stu-id="3602d-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3602d-151">Return value</span><span class="sxs-lookup"><span data-stu-id="3602d-151">Return value</span></span>

<span data-ttu-id="3602d-152">なし。</span><span class="sxs-lookup"><span data-stu-id="3602d-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3602d-153">注釈</span><span class="sxs-lookup"><span data-stu-id="3602d-153">Remarks</span></span>

<span data-ttu-id="3602d-154">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="3602d-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="3602d-155">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="3602d-155">**Idle routine function**</span></span>|<span data-ttu-id="3602d-156">**使用法**</span><span class="sxs-lookup"><span data-stu-id="3602d-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3602d-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="3602d-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="3602d-158">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="3602d-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="3602d-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3602d-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="3602d-160">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="3602d-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3602d-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3602d-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="3602d-162">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="3602d-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="3602d-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="3602d-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="3602d-164">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="3602d-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="3602d-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="3602d-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="3602d-166">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="3602d-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="3602d-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="3602d-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="3602d-168">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3602d-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="3602d-169">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3602d-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="3602d-170">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3602d-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="3602d-171">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="3602d-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

