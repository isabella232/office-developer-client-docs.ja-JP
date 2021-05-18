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
# <a name="deregisteridleroutine"></a><span data-ttu-id="01f23-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01f23-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="01f23-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f23-105">MAPI システムから [FNIDLE ベース](fnidle.md) のアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f23-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f23-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="01f23-106">Header file:</span></span>  <br/> |<span data-ttu-id="01f23-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01f23-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01f23-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="01f23-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01f23-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01f23-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01f23-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="01f23-110">Called by:</span></span>  <br/> |<span data-ttu-id="01f23-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="01f23-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="01f23-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01f23-112">Parameters</span></span>

 <span data-ttu-id="01f23-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="01f23-113">_ftg_</span></span>
  
> <span data-ttu-id="01f23-114">[in]削除するアイドル ルーチンを識別する関数タグ。</span><span class="sxs-lookup"><span data-stu-id="01f23-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01f23-115">Return value</span><span class="sxs-lookup"><span data-stu-id="01f23-115">Return value</span></span>

<span data-ttu-id="01f23-116">なし。</span><span class="sxs-lookup"><span data-stu-id="01f23-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01f23-117">注釈</span><span class="sxs-lookup"><span data-stu-id="01f23-117">Remarks</span></span>

<span data-ttu-id="01f23-118">クライアント アプリケーションまたはサービス プロバイダー内のタスクは、有効な ftg パラメーターを持つアイドル ルーチンを  _登録解除_ できます。</span><span class="sxs-lookup"><span data-stu-id="01f23-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="01f23-119">特に、アイドル 状態のルーチンは、それ自体を登録解除できます。</span><span class="sxs-lookup"><span data-stu-id="01f23-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="01f23-120">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="01f23-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="01f23-121">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="01f23-121">**Idle routine function**</span></span>|<span data-ttu-id="01f23-122">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="01f23-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01f23-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01f23-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="01f23-124">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="01f23-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="01f23-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="01f23-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="01f23-126">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="01f23-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="01f23-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01f23-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="01f23-128">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="01f23-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="01f23-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="01f23-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="01f23-130">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="01f23-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="01f23-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="01f23-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="01f23-132">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="01f23-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="01f23-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="01f23-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="01f23-134">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="01f23-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="01f23-135">**ChangeIdleRoutine** **、DeregisterIdleRoutine、\*\*\*\*および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="01f23-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="01f23-136">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01f23-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="01f23-137">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="01f23-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="01f23-138">アイドル ルーチンの登録が解除された後、アイドル 状態のエンジンは再び呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="01f23-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="01f23-139">**DeregisterIdleRoutine** を呼び出す実装では、アイドル エンジンが **FtgRegisterIdleRoutine** 関数への元の呼び出しで使用するポインターを渡したメモリ ブロックを割り当て解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f23-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

