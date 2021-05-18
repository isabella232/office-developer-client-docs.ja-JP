---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412381"
---
# <a name="fnidle"></a><span data-ttu-id="0ce7b-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="0ce7b-103">FNIDLE</span></span>
 
<span data-ttu-id="0ce7b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ce7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ce7b-105">MAPI アイドル エンジンが優先度に応じて定期的に呼び出すアイドル ルーチンを定義します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ce7b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0ce7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ce7b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0ce7b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0ce7b-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="0ce7b-109">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0ce7b-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="0ce7b-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="0ce7b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="0ce7b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ce7b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ce7b-112">対応するポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="0ce7b-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="0ce7b-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="0ce7b-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="0ce7b-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0ce7b-114">Parameters</span></span>

 <span data-ttu-id="0ce7b-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="0ce7b-115">_lpvContext_</span></span>
  
> <span data-ttu-id="0ce7b-116">[in]MAPI が呼び出すごとにアイドル ルーチンに渡すメモリ ブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="0ce7b-117">このポインターは [、FtgRegisterIdleRoutine](ftgregisteridleroutine.md)_によって pvIdleParam_ パラメーターの MAPI アイドル エンジンに渡されます。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="0ce7b-118">メモリ ブロック内のデータは、どのオブジェクトを操作するか、長い操作の現在の状態など、アイドル 状態ルーチンへの呼び出しのコンテキストを提供できます。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ce7b-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="0ce7b-119">Return value</span></span>

<span data-ttu-id="0ce7b-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ce7b-120">FALSE</span></span> 
  
> <span data-ttu-id="0ce7b-121">FNIDLE プロトタイプを持つアイドル **状態のルーチン** は、常に FALSE を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0ce7b-122">注釈</span><span class="sxs-lookup"><span data-stu-id="0ce7b-122">Remarks</span></span>

<span data-ttu-id="0ce7b-123">アイドル ルーチンの特定の機能は、実装しているクライアント アプリケーションまたはサービス プロバイダーによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="0ce7b-124">クライアントまたはプロバイダーは、アイドル 状態の各状態の実行時間を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="0ce7b-125">すべての状態は、最小限の処理を実行し  _、lpvContext_ が指すコンテキスト データの現在の状態を更新し、MAPI アイドル エンジンに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="0ce7b-126">クライアントまたはプロバイダーは、独自のアイドル ルーチンを[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数への呼び出しで登録する前に、MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="0ce7b-127">次の関数は、MAPI アイドル エンジンと、FNIDLE 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="0ce7b-128">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="0ce7b-128">**Idle routine function**</span></span>|<span data-ttu-id="0ce7b-129">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="0ce7b-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ce7b-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ce7b-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="0ce7b-131">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="0ce7b-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ce7b-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="0ce7b-133">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ce7b-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ce7b-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="0ce7b-135">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ce7b-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ce7b-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="0ce7b-137">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="0ce7b-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ce7b-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="0ce7b-139">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="0ce7b-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ce7b-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="0ce7b-141">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="0ce7b-142">**ChangeIdleRoutine** **、DeregisterIdleRoutine、\*\*\*\*および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="0ce7b-143">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="0ce7b-144">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="0ce7b-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

