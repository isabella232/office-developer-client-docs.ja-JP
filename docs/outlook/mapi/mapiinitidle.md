---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801501"
---
# <a name="mapiinitidle"></a><span data-ttu-id="42342-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="42342-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="42342-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42342-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42342-105">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="42342-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42342-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="42342-106">Header file:</span></span>  <br/> |<span data-ttu-id="42342-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="42342-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="42342-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="42342-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42342-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42342-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42342-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="42342-110">Called by:</span></span>  <br/> |<span data-ttu-id="42342-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="42342-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="42342-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="42342-112">Parameters</span></span>

 <span data-ttu-id="42342-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="42342-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="42342-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="42342-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42342-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="42342-115">Return value</span></span>

<span data-ttu-id="42342-116">**MAPIInitIdle**関数は、初期化、および 1 それ以外の場合に 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="42342-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="42342-117">**MAPIInitIdle**は、複数回呼び出されると、その他のすべての呼び出しは成功しますが、参照カウントをインクリメントする以外は無視されます。</span><span class="sxs-lookup"><span data-stu-id="42342-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="42342-118">備考</span><span class="sxs-lookup"><span data-stu-id="42342-118">Remarks</span></span>

<span data-ttu-id="42342-119">クライアント アプリケーションまたはサービス プロバイダーは、他のアイドル状態のエンジンの関数を呼び出す前に**MAPIInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="42342-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="42342-120">**MAPIInitIdle**へのすべての呼び出しを[MAPIDeInitIdle](mapideinitidle.md)、それ以降の呼び出しに一致する必要があるまたは呼び出し元のアプリケーションを実行しているアイドル状態のエンジンのままです。</span><span class="sxs-lookup"><span data-stu-id="42342-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="42342-121">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="42342-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="42342-122">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="42342-122">**Idle routine function**</span></span>|<span data-ttu-id="42342-123">**使用例**</span><span class="sxs-lookup"><span data-stu-id="42342-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42342-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="42342-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="42342-125">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="42342-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="42342-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="42342-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="42342-127">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="42342-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="42342-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="42342-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="42342-129">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="42342-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="42342-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="42342-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="42342-131">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="42342-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="42342-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="42342-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="42342-133">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="42342-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="42342-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="42342-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="42342-135">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="42342-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="42342-136">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="42342-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="42342-137">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="42342-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

