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
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342246"
---
# <a name="fnidle"></a><span data-ttu-id="e08a3-103">FNIDLE</span><span class="sxs-lookup"><span data-stu-id="e08a3-103">FNIDLE</span></span>
 
<span data-ttu-id="e08a3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e08a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e08a3-105">MAPI アイドルエンジンが優先度に従って定期的に呼び出すアイドルルーチンを定義します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-105">Defines an idle routine that the MAPI idle engine calls periodically according to priority.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e08a3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e08a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="e08a3-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="e08a3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e08a3-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="e08a3-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e08a3-109">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e08a3-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="e08a3-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="e08a3-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e08a3-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e08a3-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="e08a3-112">対応するポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e08a3-112">Corresponding pointer type:</span></span>  <br/> |<span data-ttu-id="e08a3-113">pfnidle</span><span class="sxs-lookup"><span data-stu-id="e08a3-113">PFNIDLE</span></span>  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="e08a3-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e08a3-114">Parameters</span></span>

 <span data-ttu-id="e08a3-115">_lpvcontext_</span><span class="sxs-lookup"><span data-stu-id="e08a3-115">_lpvContext_</span></span>
  
> <span data-ttu-id="e08a3-116">順番MAPI が呼び出しを行うたびにアイドルルーチンに渡されるメモリブロックへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e08a3-116">[in] Pointer to a block of memory that MAPI passes to the idle routine each time it calls it.</span></span> <span data-ttu-id="e08a3-117">このポインターは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)によって_pvIdleParam_パラメーターの MAPI アイドルエンジンに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e08a3-117">This pointer is passed to the MAPI idle engine in the  _pvIdleParam_ parameter by [FtgRegisterIdleRoutine](ftgregisteridleroutine.md).</span></span> <span data-ttu-id="e08a3-118">メモリブロック内のデータは、操作対象のオブジェクトや、時間のかかる操作の現在の状態など、アイドルルーチンの呼び出しのコンテキストを提供できます。</span><span class="sxs-lookup"><span data-stu-id="e08a3-118">The data in the memory block can provide context for the call to the idle routine, such as which object to operate on, or the current state of a lengthy operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e08a3-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="e08a3-119">Return value</span></span>

<span data-ttu-id="e08a3-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="e08a3-120">FALSE</span></span> 
  
> <span data-ttu-id="e08a3-121">**FNIDLE**プロトタイプが指定されたアイドルルーチンは、常に FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-121">An idle routine with the **FNIDLE** prototype should always return FALSE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e08a3-122">解説</span><span class="sxs-lookup"><span data-stu-id="e08a3-122">Remarks</span></span>

<span data-ttu-id="e08a3-123">アイドルルーチンの特定の機能は、クライアントアプリケーションまたはサービスプロバイダーを実装することによって決まります。</span><span class="sxs-lookup"><span data-stu-id="e08a3-123">The specific functionality of the idle routine is determined by the implementing client application or service provider.</span></span> 
  
<span data-ttu-id="e08a3-124">クライアントまたはプロバイダーは、アイドルルーチンの各状態の実行時間を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08a3-124">The client or provider must limit the execution time of each state of an idle routine.</span></span> <span data-ttu-id="e08a3-125">すべての状態は、最小限の処理を実行し、 _lpvcontext_が指すコンテキストデータ内の現在の状態を更新して、MAPI アイドルエンジンに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08a3-125">Every state should perform a minimum amount of processing, update the current state in the context data pointed to by  _lpvContext_, and return to the MAPI idle engine.</span></span> 
  
<span data-ttu-id="e08a3-126">クライアントまたはプロバイダーは、 [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)関数への呼び出しを使用して独自のアイドルルーチンを登録する前に、MAPI 関数[MAPIInitIdle](mapiinitidle.md)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08a3-126">The client or provider must call the MAPI function [MAPIInitIdle](mapiinitidle.md) before it can register its own idle routine with a call to the [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) function.</span></span> 
  
<span data-ttu-id="e08a3-127">次の関数は、MAPI アイドルエンジンと、FNIDLE 関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-127">The following functions deal with the MAPI idle engine and with idle routines based on the FNIDLE function prototype:</span></span> 
  
|<span data-ttu-id="e08a3-128">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="e08a3-128">**Idle routine function**</span></span>|<span data-ttu-id="e08a3-129">**使用法**</span><span class="sxs-lookup"><span data-stu-id="e08a3-129">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e08a3-130">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e08a3-130">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e08a3-131">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-131">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="e08a3-132">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e08a3-132">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="e08a3-133">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-133">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e08a3-134">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e08a3-134">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="e08a3-135">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="e08a3-135">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e08a3-136">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e08a3-136">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e08a3-137">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="e08a3-137">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e08a3-138">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e08a3-138">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e08a3-139">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="e08a3-139">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="e08a3-140">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e08a3-140">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="e08a3-141">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-141">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="e08a3-142">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="e08a3-142">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="e08a3-143">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e08a3-143">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e08a3-144">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="e08a3-144">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

