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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 49682007946a4c5dda3800751deaebcc0e1e5740
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579453"
---
# <a name="changeidleroutine"></a><span data-ttu-id="395f1-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="395f1-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="395f1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="395f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="395f1-105">[FNIDLE](fnidle.md)ベース アイドル ルーチンの特性の一部またはすべてを変更します。</span><span class="sxs-lookup"><span data-stu-id="395f1-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="395f1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="395f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="395f1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="395f1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="395f1-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="395f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="395f1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="395f1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="395f1-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="395f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="395f1-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="395f1-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="395f1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="395f1-112">Parameters</span></span>

<span data-ttu-id="395f1-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="395f1-113">_ftg_</span></span>
  
> <span data-ttu-id="395f1-114">[in]アイドル ルーチンを識別するタグを機能します。</span><span class="sxs-lookup"><span data-stu-id="395f1-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="395f1-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="395f1-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="395f1-116">[in]アイドル ルーチンへのポインター。</span><span class="sxs-lookup"><span data-stu-id="395f1-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="395f1-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="395f1-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="395f1-118">[in]新しいアイドル ルーチンの実装を呼び出し元が割り当てたメモリ ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="395f1-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="395f1-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="395f1-119">_priIdle_</span></span>
  
> <span data-ttu-id="395f1-120">[in]アイドル ルーチンの新しい優先度を表す値。</span><span class="sxs-lookup"><span data-stu-id="395f1-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="395f1-121">ルーチンの実装で定義可能な優先度よりも大きいか小さいは、0 が 0 ではありません。</span><span class="sxs-lookup"><span data-stu-id="395f1-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="395f1-122">0 の値は、マウスのクリックや、WM_PAINT メッセージなどのユーザー イベントに予約されています。</span><span class="sxs-lookup"><span data-stu-id="395f1-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="395f1-123">ゼロより大きい値は、ユーザー イベントよりも優先順位が高いと、Windows メッセージ ポンプの標準的なループの一部としてディスパッチをバック グラウンド タスクの優先順位を表します。</span><span class="sxs-lookup"><span data-stu-id="395f1-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="395f1-124">メッセージ ポンプのアイドル時間中にのみ実行しているアイドル状態のタスクの優先順位を表す 0 より小さい値です。</span><span class="sxs-lookup"><span data-stu-id="395f1-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="395f1-125">優先順位の例としては: 前景の提出書類の 1、1 電源編集文字の挿入、および新着メッセージをダウンロードするための 3。</span><span class="sxs-lookup"><span data-stu-id="395f1-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="395f1-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="395f1-126">_csecIdle_</span></span>
  
> <span data-ttu-id="395f1-127">[in]時間を 100 分の 1 秒間、アイドル状態のルーチンに適用します。</span><span class="sxs-lookup"><span data-stu-id="395f1-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="395f1-128">初期時刻の値の意味は、 _iroIdle_パラメーターに渡される内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="395f1-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="395f1-129">できます。</span><span class="sxs-lookup"><span data-stu-id="395f1-129">It can be:</span></span> 
    
  - <span data-ttu-id="395f1-130">ユーザー何もしなかったため、MAPI の前に、までに必要な最小期間アイドル状態のエンジン ルーチンを呼び出すとアイドルを最初に、 _iroIdle_に FIROWAIT フラグが設定されている場合。</span><span class="sxs-lookup"><span data-stu-id="395f1-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="395f1-131">この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="395f1-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="395f1-132">_IroIdle_に FIROINTERVAL フラグが設定されている場合、アイドル状態のルーチンへの呼び出しの間の最小間隔。</span><span class="sxs-lookup"><span data-stu-id="395f1-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="395f1-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="395f1-133">_iroIdle_</span></span>
  
> <span data-ttu-id="395f1-134">[in]アイドル ルーチンを呼び出すための新しいオプションを示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="395f1-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="395f1-135">次のフラグの 1 つだけを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="395f1-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="395f1-136">FIROINTERVAL: _csecIdle_パラメーターによって指定される時間は、アイドル状態のルーチンへの連続呼び出しの間の最小の間隔です。</span><span class="sxs-lookup"><span data-stu-id="395f1-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="395f1-137">FIROONCEONLY: 古い形式です。</span><span class="sxs-lookup"><span data-stu-id="395f1-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="395f1-138">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="395f1-138">Do not use.</span></span> 
      
  - <span data-ttu-id="395f1-139">FIROPERBLOCK: 古い形式です。</span><span class="sxs-lookup"><span data-stu-id="395f1-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="395f1-140">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="395f1-140">Do not use.</span></span> 
      
  - <span data-ttu-id="395f1-141">FIROWAIT: _csecIdle_パラメーターによって指定される時間は、ユーザー何もしなかったため、MAPI アイドル エンジンは、最初にアイドル ルーチンを呼び出す前に必要な経過時間の最小期間です。</span><span class="sxs-lookup"><span data-stu-id="395f1-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="395f1-142">この時間が経過した後、アイドル状態のエンジンでは必要に応じてアイドル ルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="395f1-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="395f1-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="395f1-143">_ircIdle_</span></span>
  
> <span data-ttu-id="395f1-144">[in]アイドル ルーチンに変更を示すために使用されるフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="395f1-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="395f1-145">任意の組み合わせでは、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="395f1-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="395f1-146">FIRCCSEC: アイドル状態のルーチンでは、 _csecIdle_パラメーターで渡された値で示される変更に関連付けられている時間を変更します。</span><span class="sxs-lookup"><span data-stu-id="395f1-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="395f1-147">FIRCIRO: アイドル状態のルーチンでは、オプションの変更は、値で示される変更パラメーターで渡された、 _iroIdle_です。</span><span class="sxs-lookup"><span data-stu-id="395f1-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="395f1-148">FIRCPFN: アイドル状態の日常的なポインターの変更は、値で示される変更パラメーターで渡された、 _pfnIdle_です。</span><span class="sxs-lookup"><span data-stu-id="395f1-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="395f1-149">FIRCPRI: アイドル状態のルーチンでは、優先順位の変更は、値で示される変更パラメーターで渡された、 _priIdle_です。</span><span class="sxs-lookup"><span data-stu-id="395f1-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="395f1-150">FIRCPV: アイドル状態のルーチンでは、メモリ ブロックへの変更は、値で示される変更パラメーターで渡された、 _pvIdleParam_です。</span><span class="sxs-lookup"><span data-stu-id="395f1-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="395f1-151">Return value</span><span class="sxs-lookup"><span data-stu-id="395f1-151">Return value</span></span>

<span data-ttu-id="395f1-152">なし。</span><span class="sxs-lookup"><span data-stu-id="395f1-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="395f1-153">注釈</span><span class="sxs-lookup"><span data-stu-id="395f1-153">Remarks</span></span>

<span data-ttu-id="395f1-154">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="395f1-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="395f1-155">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="395f1-155">**Idle routine function**</span></span>|<span data-ttu-id="395f1-156">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="395f1-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="395f1-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="395f1-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="395f1-158">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="395f1-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="395f1-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="395f1-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="395f1-160">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="395f1-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="395f1-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="395f1-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="395f1-162">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="395f1-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="395f1-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="395f1-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="395f1-164">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="395f1-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="395f1-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="395f1-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="395f1-166">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="395f1-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="395f1-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="395f1-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="395f1-168">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="395f1-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="395f1-169">**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。</span><span class="sxs-lookup"><span data-stu-id="395f1-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="395f1-170">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="395f1-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="395f1-171">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="395f1-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

