---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404562"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="2226c-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2226c-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="2226c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2226c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2226c-105">MAPI システムから[FNIDLE](fnidle.md)ベースのアイドルルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="2226c-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2226c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2226c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2226c-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="2226c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2226c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="2226c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2226c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2226c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2226c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2226c-110">Called by:</span></span>  <br/> |<span data-ttu-id="2226c-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2226c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="2226c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2226c-112">Parameters</span></span>

 <span data-ttu-id="2226c-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="2226c-113">_ftg_</span></span>
  
> <span data-ttu-id="2226c-114">順番削除する idle ルーチンを識別する Function タグです。</span><span class="sxs-lookup"><span data-stu-id="2226c-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2226c-115">Return value</span><span class="sxs-lookup"><span data-stu-id="2226c-115">Return value</span></span>

<span data-ttu-id="2226c-116">なし。</span><span class="sxs-lookup"><span data-stu-id="2226c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2226c-117">注釈</span><span class="sxs-lookup"><span data-stu-id="2226c-117">Remarks</span></span>

<span data-ttu-id="2226c-118">クライアントアプリケーションまたはサービスプロバイダーのすべてのタスクは、有効な_ftg_パラメーターを持つ idle ルーチンを登録解除できます。</span><span class="sxs-lookup"><span data-stu-id="2226c-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="2226c-119">特に、アイドル状態のルーチンで自分自身を登録解除することができます。</span><span class="sxs-lookup"><span data-stu-id="2226c-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="2226c-120">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="2226c-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="2226c-121">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="2226c-121">**Idle routine function**</span></span>|<span data-ttu-id="2226c-122">**使用法**</span><span class="sxs-lookup"><span data-stu-id="2226c-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2226c-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2226c-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="2226c-124">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="2226c-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="2226c-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="2226c-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="2226c-126">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="2226c-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2226c-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2226c-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="2226c-128">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="2226c-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="2226c-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="2226c-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="2226c-130">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="2226c-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="2226c-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="2226c-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="2226c-132">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="2226c-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="2226c-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="2226c-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="2226c-134">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2226c-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="2226c-135">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="2226c-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="2226c-136">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2226c-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="2226c-137">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="2226c-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="2226c-138">アイドル状態のルーチンが登録解除された後は、アイドル状態のエンジンはそれを再度呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="2226c-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="2226c-139">**DeregisterIdleRoutine**を呼び出す実装では、 **FtgRegisterIdleRoutine**関数への元の呼び出しで使用するために、アイドルエンジンがポインターを渡したメモリブロックを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2226c-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

