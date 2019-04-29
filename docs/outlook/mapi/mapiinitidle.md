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
# <a name="mapiinitidle"></a><span data-ttu-id="44015-103">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="44015-103">MAPIInitIdle</span></span>

  
  
<span data-ttu-id="44015-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44015-105">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="44015-105">Initializes the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44015-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="44015-106">Header file:</span></span>  <br/> |<span data-ttu-id="44015-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="44015-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44015-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="44015-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44015-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44015-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44015-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="44015-110">Called by:</span></span>  <br/> |<span data-ttu-id="44015-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="44015-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a><span data-ttu-id="44015-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44015-112">Parameters</span></span>

 <span data-ttu-id="44015-113">_lpvreserved_</span><span class="sxs-lookup"><span data-stu-id="44015-113">_lpvReserved_</span></span>
  
> <span data-ttu-id="44015-114">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="44015-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44015-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="44015-115">Return value</span></span>

<span data-ttu-id="44015-116">**MAPIInitIdle**関数は、初期化が成功した場合は0を返し、それ以外の場合は1を返します。</span><span class="sxs-lookup"><span data-stu-id="44015-116">The **MAPIInitIdle** function returns zero if initialization is successful, and 1 otherwise.</span></span> <span data-ttu-id="44015-117">**MAPIInitIdle**が複数回呼び出された場合、追加の呼び出しはすべて成功しますが、参照カウントを増分する場合を除いて無視されます。</span><span class="sxs-lookup"><span data-stu-id="44015-117">If **MAPIInitIdle** is called multiple times, all additional calls succeed but are ignored except to increment the reference count.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="44015-118">注釈</span><span class="sxs-lookup"><span data-stu-id="44015-118">Remarks</span></span>

<span data-ttu-id="44015-119">クライアントアプリケーションまたはサービスプロバイダーは、他の idle engine 関数を呼び出す前に、 **MAPIInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="44015-119">A client application or service provider must call **MAPIInitIdle** before calling any other idle engine function.</span></span> 
  
<span data-ttu-id="44015-120">**MAPIInitIdle**のすべての呼び出しは、以降の[MAPIDeInitIdle](mapideinitidle.md)の呼び出しで一致する必要があります。または、呼び出し元アプリケーションに対してアイドル状態のエンジンが実行されたままになります。</span><span class="sxs-lookup"><span data-stu-id="44015-120">Every call to **MAPIInitIdle** must be matched by a subsequent call to [MAPIDeInitIdle](mapideinitidle.md), or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="44015-121">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="44015-121">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="44015-122">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="44015-122">**Idle routine function**</span></span>|<span data-ttu-id="44015-123">**使用法**</span><span class="sxs-lookup"><span data-stu-id="44015-123">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44015-124">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="44015-124">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="44015-125">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="44015-125">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="44015-126">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="44015-126">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="44015-127">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="44015-127">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="44015-128">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="44015-128">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="44015-129">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="44015-129">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="44015-130">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="44015-130">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="44015-131">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="44015-131">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="44015-132">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="44015-132">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="44015-133">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="44015-133">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|<span data-ttu-id="44015-134">**MAPIInitIdle**</span><span class="sxs-lookup"><span data-stu-id="44015-134">**MAPIInitIdle**</span></span> <br/> |<span data-ttu-id="44015-135">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="44015-135">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="44015-136">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="44015-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="44015-137">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="44015-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

