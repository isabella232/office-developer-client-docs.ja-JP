---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339397"
---
# <a name="enableidleroutine"></a><span data-ttu-id="714bc-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="714bc-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="714bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="714bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="714bc-105">[FNIDLE](fnidle.md)ベースのアイドルルーチンを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="714bc-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="714bc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="714bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="714bc-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="714bc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="714bc-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="714bc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="714bc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="714bc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="714bc-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="714bc-110">Called by:</span></span>  <br/> |<span data-ttu-id="714bc-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="714bc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="714bc-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="714bc-112">Parameters</span></span>

 <span data-ttu-id="714bc-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="714bc-113">_ftg_</span></span>
  
> <span data-ttu-id="714bc-114">順番有効または無効にする idle ルーチンを識別する関数タグ。</span><span class="sxs-lookup"><span data-stu-id="714bc-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="714bc-115">_fenable_</span><span class="sxs-lookup"><span data-stu-id="714bc-115">_fEnable_</span></span>
  
> <span data-ttu-id="714bc-116">順番アイドルエンジンがアイドル状態のルーチンを有効にする必要がある場合は TRUE、無効にする場合は FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="714bc-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="714bc-117">Return value</span><span class="sxs-lookup"><span data-stu-id="714bc-117">Return value</span></span>

<span data-ttu-id="714bc-118">なし。</span><span class="sxs-lookup"><span data-stu-id="714bc-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="714bc-119">解説</span><span class="sxs-lookup"><span data-stu-id="714bc-119">Remarks</span></span>

<span data-ttu-id="714bc-120">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="714bc-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="714bc-121">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="714bc-121">**Idle routine function**</span></span>|<span data-ttu-id="714bc-122">**使用法**</span><span class="sxs-lookup"><span data-stu-id="714bc-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="714bc-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="714bc-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="714bc-124">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="714bc-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="714bc-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="714bc-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="714bc-126">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="714bc-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="714bc-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="714bc-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="714bc-128">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="714bc-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="714bc-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="714bc-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="714bc-130">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="714bc-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="714bc-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="714bc-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="714bc-132">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="714bc-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="714bc-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="714bc-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="714bc-134">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="714bc-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="714bc-135">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="714bc-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="714bc-136">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="714bc-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="714bc-137">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="714bc-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

