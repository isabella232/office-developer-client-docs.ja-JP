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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569226"
---
# <a name="mapiinitidle"></a><span data-ttu-id="a6677-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="a6677-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="a6677-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6677-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6677-105">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6677-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6677-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a6677-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6677-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a6677-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a6677-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a6677-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6677-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a6677-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a6677-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a6677-110">Called by:</span></span>  <br/> |<span data-ttu-id="a6677-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a6677-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="a6677-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6677-112">Parameters</span></span>

 <span data-ttu-id="a6677-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="a6677-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="a6677-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a6677-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6677-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6677-115">Return value</span></span>

<span data-ttu-id="a6677-116">**MAPIInitIdle**関数は、初期化、および 1 それ以外の場合に 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="a6677-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="a6677-117">**MAPIInitIdle**は、複数回呼び出されると、その他のすべての呼び出しは成功しますが、参照カウントをインクリメントする以外は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a6677-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6677-118">注釈</span><span class="sxs-lookup"><span data-stu-id="a6677-118">Remarks</span></span>

<span data-ttu-id="a6677-119">クライアント アプリケーションまたはサービス プロバイダーは、他のアイドル状態のエンジンの関数を呼び出す前に**MAPIInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6677-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="a6677-120">**MAPIInitIdle**へのすべての呼び出しを[MAPIDeInitIdle](mapideinitidle.md)、それ以降の呼び出しに一致する必要があるまたは呼び出し元のアプリケーションを実行しているアイドル状態のエンジンのままです。</span><span class="sxs-lookup"><span data-stu-id="a6677-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="a6677-121">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="a6677-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="a6677-122">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="a6677-122">**Idle routine function**</span></span>|<span data-ttu-id="a6677-123">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="a6677-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6677-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a6677-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="a6677-125">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="a6677-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="a6677-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a6677-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="a6677-127">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="a6677-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a6677-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a6677-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="a6677-129">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6677-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a6677-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a6677-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="a6677-131">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="a6677-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="a6677-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="a6677-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="a6677-133">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="a6677-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="a6677-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="a6677-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="a6677-135">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6677-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="a6677-136">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6677-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="a6677-137">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="a6677-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

