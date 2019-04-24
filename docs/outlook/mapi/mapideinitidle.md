---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357324"
---
# <a name="mapideinitidle"></a><span data-ttu-id="0ac78-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ac78-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="0ac78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ac78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ac78-105">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="0ac78-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ac78-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0ac78-106">Header file:</span></span>  <br/> |<span data-ttu-id="0ac78-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="0ac78-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0ac78-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="0ac78-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0ac78-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0ac78-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0ac78-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0ac78-110">Called by:</span></span>  <br/> |<span data-ttu-id="0ac78-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="0ac78-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="0ac78-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0ac78-112">Parameters</span></span>

<span data-ttu-id="0ac78-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0ac78-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="0ac78-114">Return value</span><span class="sxs-lookup"><span data-stu-id="0ac78-114">Return value</span></span>

<span data-ttu-id="0ac78-115">なし。</span><span class="sxs-lookup"><span data-stu-id="0ac78-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ac78-116">解説</span><span class="sxs-lookup"><span data-stu-id="0ac78-116">Remarks</span></span>

<span data-ttu-id="0ac78-117">クライアントアプリケーションまたはサービスプロバイダーは、アイドル状態のエンジンが不要になったとき (たとえば、処理を停止しようとしているとき) に**MAPIDeInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ac78-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="0ac78-118">[MAPIInitIdle](mapiinitidle.md)のすべての呼び出しは、以降の**MAPIDeInitIdle**の呼び出しで一致する必要があります。または、呼び出し元アプリケーションに対してアイドル状態のエンジンが実行されたままになります。</span><span class="sxs-lookup"><span data-stu-id="0ac78-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="0ac78-119">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="0ac78-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="0ac78-120">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="0ac78-120">**Idle routine function**</span></span>|<span data-ttu-id="0ac78-121">**使用法**</span><span class="sxs-lookup"><span data-stu-id="0ac78-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ac78-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ac78-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="0ac78-123">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="0ac78-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="0ac78-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ac78-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="0ac78-125">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="0ac78-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ac78-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ac78-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="0ac78-127">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="0ac78-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="0ac78-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="0ac78-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="0ac78-129">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="0ac78-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="0ac78-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="0ac78-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="0ac78-131">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="0ac78-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="0ac78-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="0ac78-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="0ac78-133">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0ac78-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="0ac78-134">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ac78-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="0ac78-135">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="0ac78-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

