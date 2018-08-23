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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800093"
---
# <a name="fnidle"></a><span data-ttu-id="0433a-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="0433a-103">FNIDLE</span></span>
 
<span data-ttu-id="0433a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0433a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0433a-105">MAPI アイドル エンジンを呼び出すの優先順位に従って定期的にアイドル状態のルーチンを定義します。</span><span class="sxs-lookup"><span data-stu-id="0433a-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0433a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0433a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0433a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0433a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0433a-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="0433a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="0433a-109">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0433a-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="0433a-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="0433a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="0433a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0433a-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0433a-112">対応するポインターの型。</span><span class="sxs-lookup"><span data-stu-id="0433a-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="0433a-113">PFNIDLE</span><span class="sxs-lookup"><span data-stu-id="0433a-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="0433a-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0433a-114">Parameters</span></span>

 <span data-ttu-id="0433a-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="0433a-115">_lpvContext_</span></span>
  
> <span data-ttu-id="0433a-116">[in]アイドル ルーチンへの MAPI のパスは時間、メモリ ブロックへのポインターは、それを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0433a-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="0433a-117">このポインターは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)で、 _pvIdleParam_パラメーターでは、MAPI アイドル エンジンに渡されます。</span><span class="sxs-lookup"><span data-stu-id="0433a-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="0433a-118">メモリ ブロック内のデータは、操作対象のオブジェクトなど、アイドル状態のルーチンまたは時間のかかる操作の現在の状態への呼び出しのコンテキストを提供できます。</span><span class="sxs-lookup"><span data-stu-id="0433a-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0433a-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="0433a-119">Return value</span></span>

<span data-ttu-id="0433a-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="0433a-120">FALSE</span></span> 
  
> <span data-ttu-id="0433a-121">**FNIDLE**プロトタイプでアイドル状態のルーチンは、FALSE を返す常にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0433a-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0433a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="0433a-122">Remarks</span></span>

<span data-ttu-id="0433a-123">アイドル ルーチンの特定の機能は、実装することによって決定されますクライアント アプリケーションまたはサービス プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="0433a-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="0433a-124">クライアントまたはプロバイダーは、実行時間、アイドル状態のルーチンの各状態を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0433a-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="0433a-125">すべての状態では、最小限の処理を実行、 _lpvContext_で示されるコンテキスト データの現在の状態を更新、および MAPI アイドル エンジンに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="0433a-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="0433a-126">クライアントまたはプロバイダーは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数を呼び出して、独自のアイドル状態のルーチンを登録する前に MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0433a-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="0433a-127">次の関数では、MAPI アイドル エンジンと FNIDLE 関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="0433a-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="0433a-128">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="0433a-128">**Idle routine function**</span></span>|<span data-ttu-id="0433a-129">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="0433a-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0433a-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0433a-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="0433a-131">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="0433a-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="0433a-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0433a-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="0433a-133">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="0433a-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0433a-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0433a-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="0433a-135">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="0433a-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0433a-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0433a-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="0433a-137">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="0433a-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="0433a-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="0433a-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="0433a-139">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="0433a-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="0433a-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="0433a-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="0433a-141">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0433a-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="0433a-142">**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。</span><span class="sxs-lookup"><span data-stu-id="0433a-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="0433a-143">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0433a-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="0433a-144">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="0433a-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

