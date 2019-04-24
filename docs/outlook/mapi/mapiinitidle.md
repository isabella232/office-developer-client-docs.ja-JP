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
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346656"
---
# <a name="mapiinitidle"></a><span data-ttu-id="d2a0f-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d2a0f-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="d2a0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2a0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2a0f-105">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2a0f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d2a0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2a0f-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="d2a0f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d2a0f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d2a0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2a0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2a0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2a0f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d2a0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2a0f-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d2a0f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="d2a0f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2a0f-112">Parameters</span></span>

 <span data-ttu-id="d2a0f-113">_lpvreserved_</span><span class="sxs-lookup"><span data-stu-id="d2a0f-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="d2a0f-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="d2a0f-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2a0f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="d2a0f-115">Return value</span></span>

<span data-ttu-id="d2a0f-116">**MAPIInitIdle**関数は、初期化が成功した場合は0を返し、それ以外の場合は1を返します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="d2a0f-117">**MAPIInitIdle**が複数回呼び出された場合、追加の呼び出しはすべて成功しますが、参照カウントを増分する場合を除いて無視されます。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2a0f-118">解説</span><span class="sxs-lookup"><span data-stu-id="d2a0f-118">Remarks</span></span>

<span data-ttu-id="d2a0f-119">クライアントアプリケーションまたはサービスプロバイダーは、他の idle engine 関数を呼び出す前に、 **MAPIInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="d2a0f-120">**MAPIInitIdle**のすべての呼び出しは、以降の[MAPIDeInitIdle](mapideinitidle.md)の呼び出しで一致する必要があります。または、呼び出し元アプリケーションに対してアイドル状態のエンジンが実行されたままになります。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="d2a0f-121">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="d2a0f-122">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="d2a0f-122">**Idle routine function**</span></span>|<span data-ttu-id="d2a0f-123">**使用法**</span><span class="sxs-lookup"><span data-stu-id="d2a0f-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2a0f-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2a0f-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d2a0f-125">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d2a0f-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2a0f-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d2a0f-127">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d2a0f-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2a0f-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d2a0f-129">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d2a0f-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d2a0f-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="d2a0f-131">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d2a0f-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d2a0f-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d2a0f-133">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="d2a0f-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="d2a0f-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="d2a0f-135">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d2a0f-136">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d2a0f-137">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="d2a0f-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

