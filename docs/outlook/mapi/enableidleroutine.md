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
# <a name="enableidleroutine"></a><span data-ttu-id="9fb0d-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fb0d-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="9fb0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fb0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fb0d-105">FNIDLE ベースのアイドル [ルーチンを有効](fnidle.md) または無効にします。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fb0d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9fb0d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9fb0d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9fb0d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9fb0d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="9fb0d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9fb0d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9fb0d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9fb0d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="9fb0d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9fb0d-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9fb0d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="9fb0d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9fb0d-112">Parameters</span></span>

 <span data-ttu-id="9fb0d-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="9fb0d-113">_ftg_</span></span>
  
> <span data-ttu-id="9fb0d-114">[in]有効または無効にするアイドル ルーチンを識別する関数タグ。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="9fb0d-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="9fb0d-115">_fEnable_</span></span>
  
> <span data-ttu-id="9fb0d-116">[in]アイドル 状態のエンジンでアイドル ルーチンを有効にする必要がある場合は TRUE、無効にする必要がある場合は FALSE を含む。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fb0d-117">Return value</span><span class="sxs-lookup"><span data-stu-id="9fb0d-117">Return value</span></span>

<span data-ttu-id="9fb0d-118">なし。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fb0d-119">注釈</span><span class="sxs-lookup"><span data-stu-id="9fb0d-119">Remarks</span></span>

<span data-ttu-id="9fb0d-120">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="9fb0d-121">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="9fb0d-121">**Idle routine function**</span></span>|<span data-ttu-id="9fb0d-122">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="9fb0d-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fb0d-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fb0d-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="9fb0d-124">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="9fb0d-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fb0d-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="9fb0d-126">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="9fb0d-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="9fb0d-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="9fb0d-128">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="9fb0d-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="9fb0d-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="9fb0d-130">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="9fb0d-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="9fb0d-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="9fb0d-132">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="9fb0d-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="9fb0d-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="9fb0d-134">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="9fb0d-135">**ChangeIdleRoutine** **、DeregisterIdleRoutine、\*\*\*\*および EnableIdleRoutine** は **、FtgRegisterIdleRoutine** によって返される関数タグを入力パラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="9fb0d-136">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="9fb0d-137">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="9fb0d-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

