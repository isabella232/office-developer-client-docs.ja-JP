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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78d499dabe60a8051c6a2a77abad4b7d6f2ed159
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591955"
---
# <a name="deregisteridleroutine"></a><span data-ttu-id="d17af-103">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d17af-103">DeregisterIdleRoutine</span></span>

  
  
<span data-ttu-id="d17af-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d17af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d17af-105">MAPI システムからのアイドル状態のルーチンを削除する[FNIDLE](fnidle.md)に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d17af-105">Removes a [FNIDLE](fnidle.md) based idle routine from the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d17af-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d17af-106">Header file:</span></span>  <br/> |<span data-ttu-id="d17af-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d17af-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d17af-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d17af-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d17af-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d17af-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d17af-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d17af-110">Called by:</span></span>  <br/> |<span data-ttu-id="d17af-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d17af-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a><span data-ttu-id="d17af-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d17af-112">Parameters</span></span>

 <span data-ttu-id="d17af-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="d17af-113">_ftg_</span></span>
  
> <span data-ttu-id="d17af-114">[in]関数を削除するのにはアイドル状態のルーチンを識別するタグです。</span><span class="sxs-lookup"><span data-stu-id="d17af-114">[in] Function tag that identifies the idle routine to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d17af-115">Return value</span><span class="sxs-lookup"><span data-stu-id="d17af-115">Return value</span></span>

<span data-ttu-id="d17af-116">なし。</span><span class="sxs-lookup"><span data-stu-id="d17af-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d17af-117">注釈</span><span class="sxs-lookup"><span data-stu-id="d17af-117">Remarks</span></span>

<span data-ttu-id="d17af-118">_Ftg_の有効なパラメーターを持っている、アイドル状態のルーチンはクライアント アプリケーションまたはサービス プロバイダーの任意のタスクの登録を解除できます。</span><span class="sxs-lookup"><span data-stu-id="d17af-118">Any task in a client application or service provider can deregister any idle routine for which it has a valid  _ftg_ parameter.</span></span> <span data-ttu-id="d17af-119">具体的には、アイドル、ルーチンが登録を解除自体。</span><span class="sxs-lookup"><span data-stu-id="d17af-119">In particular, an idle routine can deregister itself.</span></span> 
  
<span data-ttu-id="d17af-120">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="d17af-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="d17af-121">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="d17af-121">**Idle routine function**</span></span>|<span data-ttu-id="d17af-122">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="d17af-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d17af-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d17af-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d17af-124">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="d17af-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|<span data-ttu-id="d17af-125">**DeregisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="d17af-125">**DeregisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="d17af-126">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="d17af-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d17af-127">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d17af-127">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d17af-128">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="d17af-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d17af-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d17af-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="d17af-130">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="d17af-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d17af-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d17af-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d17af-132">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="d17af-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d17af-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d17af-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d17af-134">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d17af-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="d17af-135">**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。</span><span class="sxs-lookup"><span data-stu-id="d17af-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="d17af-136">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d17af-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d17af-137">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="d17af-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="d17af-138">アイドル ルーチンの登録を解除した後、アイドル状態のエンジンが呼び出されません、もう一度。</span><span class="sxs-lookup"><span data-stu-id="d17af-138">After the idle routine is deregistered, the idle engine does not call it again.</span></span> <span data-ttu-id="d17af-139">**DeregisterIdleRoutine**を呼び出す任意の実装は、 **FtgRegisterIdleRoutine**関数の元の呼び出しで使用するアイドル状態のエンジンのポインターを渡すようにすべてのメモリ ブロックを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d17af-139">Any implementation that calls **DeregisterIdleRoutine** must deallocate any memory blocks to which it passed pointers for the idle engine to use in its original call to the **FtgRegisterIdleRoutine** function.</span></span> 
  

