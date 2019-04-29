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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e04c872762665f4b3a22559dc2ed1504e7b8f9af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410222"
---
# <a name="enableidleroutine"></a><span data-ttu-id="e04b4-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e04b4-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="e04b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e04b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e04b4-105">[FNIDLE](fnidle.md)ベースのアイドルルーチンを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="e04b4-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e04b4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e04b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="e04b4-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="e04b4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e04b4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e04b4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e04b4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e04b4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e04b4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e04b4-110">Called by:</span></span>  <br/> |<span data-ttu-id="e04b4-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e04b4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="e04b4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e04b4-112">Parameters</span></span>

 <span data-ttu-id="e04b4-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="e04b4-113">_ftg_</span></span>
  
> <span data-ttu-id="e04b4-114">順番有効または無効にする idle ルーチンを識別する関数タグ。</span><span class="sxs-lookup"><span data-stu-id="e04b4-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="e04b4-115">_fenable_</span><span class="sxs-lookup"><span data-stu-id="e04b4-115">_fEnable_</span></span>
  
> <span data-ttu-id="e04b4-116">順番アイドルエンジンがアイドル状態のルーチンを有効にする必要がある場合は TRUE、無効にする場合は FALSE を指定します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e04b4-117">Return value</span><span class="sxs-lookup"><span data-stu-id="e04b4-117">Return value</span></span>

<span data-ttu-id="e04b4-118">なし。</span><span class="sxs-lookup"><span data-stu-id="e04b4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e04b4-119">注釈</span><span class="sxs-lookup"><span data-stu-id="e04b4-119">Remarks</span></span>

<span data-ttu-id="e04b4-120">次の関数は、MAPI アイドルエンジンと、 [FNIDLE](fnidle.md)関数プロトタイプに基づいてアイドルルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="e04b4-121">**Idle ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="e04b4-121">**Idle routine function**</span></span>|<span data-ttu-id="e04b4-122">**使用法**</span><span class="sxs-lookup"><span data-stu-id="e04b4-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e04b4-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e04b4-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="e04b4-124">登録されているアイドルルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="e04b4-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e04b4-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="e04b4-126">登録されているアイドルルーチンを MAPI システムから削除します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="e04b4-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="e04b4-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="e04b4-128">登録済みのアイドル状態を、MAPI システムから削除せずに無効または再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="e04b4-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="e04b4-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e04b4-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="e04b4-130">アイドルルーチンを MAPI システムに追加するか、有効にします。</span><span class="sxs-lookup"><span data-stu-id="e04b4-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="e04b4-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e04b4-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="e04b4-132">呼び出し元アプリケーションの MAPI アイドルエンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="e04b4-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="e04b4-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e04b4-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="e04b4-134">呼び出し元アプリケーションの MAPI アイドルエンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="e04b4-135">**changeidleroutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**は、 **FtgRegisterIdleRoutine**によって返される function タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="e04b4-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="e04b4-136">プラットフォームのすべてのフォアグラウンドタスクがアイドル状態になると、MAPI アイドルエンジンは、実行の準備ができている最も優先度の高いアイドルルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e04b4-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="e04b4-137">同じ優先度のアイドルルーチン間での通話順序は保証されません。</span><span class="sxs-lookup"><span data-stu-id="e04b4-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

