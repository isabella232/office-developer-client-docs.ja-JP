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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432444"
---
# <a name="mapiinitidle"></a><span data-ttu-id="e7913-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e7913-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="e7913-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7913-105">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e7913-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7913-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e7913-106">Header file:</span></span>  <br/> |<span data-ttu-id="e7913-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e7913-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e7913-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e7913-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7913-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7913-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7913-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e7913-110">Called by:</span></span>  <br/> |<span data-ttu-id="e7913-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e7913-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="e7913-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7913-112">Parameters</span></span>

 <span data-ttu-id="e7913-113">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="e7913-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="e7913-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="e7913-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e7913-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="e7913-115">Return value</span></span>

<span data-ttu-id="e7913-116">**MAPIInitIdle 関数は**、初期化が成功した場合は 0 を返し、それ以外の場合は 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7913-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="e7913-117">**MAPIInitIdle が** 複数回呼び出された場合、追加の呼び出しはすべて成功しますが、参照カウントを増やす以外は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e7913-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e7913-118">注釈</span><span class="sxs-lookup"><span data-stu-id="e7913-118">Remarks</span></span>

<span data-ttu-id="e7913-119">クライアント アプリケーションまたはサービス プロバイダーは、他のアイドル 状態のエンジン関数を呼び出す前に **MAPIInitIdle** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7913-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="e7913-120">**MAPIInitIdle** へのすべての呼び出しは [、MAPIDeInitIdle](mapideinitidle.md)への後続の呼び出しによって一致する必要があります。または、アイドル 状態のエンジンが呼び出し元のアプリケーションに対して実行された状態を残している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7913-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="e7913-121">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="e7913-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="e7913-122">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="e7913-122">**Idle routine function**</span></span>|<span data-ttu-id="e7913-123">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="e7913-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7913-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7913-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e7913-125">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="e7913-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="e7913-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7913-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="e7913-127">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="e7913-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e7913-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7913-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="e7913-129">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="e7913-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e7913-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e7913-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e7913-131">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="e7913-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e7913-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e7913-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e7913-133">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="e7913-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="e7913-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="e7913-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="e7913-135">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e7913-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="e7913-136">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7913-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e7913-137">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="e7913-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

