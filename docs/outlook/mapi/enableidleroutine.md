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
ms.openlocfilehash: 00b5c123e588636654fb4287cc7b45500d47d89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800001"
---
# <a name="enableidleroutine"></a><span data-ttu-id="98799-103">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="98799-103">EnableIdleRoutine</span></span>

  
  
<span data-ttu-id="98799-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98799-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98799-105">有効または[FNIDLE](fnidle.md)ベース アイドル ルーチンを無効にします。</span><span class="sxs-lookup"><span data-stu-id="98799-105">Enables or disables a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98799-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="98799-106">Header file:</span></span>  <br/> |<span data-ttu-id="98799-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="98799-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98799-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="98799-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98799-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98799-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98799-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="98799-110">Called by:</span></span>  <br/> |<span data-ttu-id="98799-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="98799-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a><span data-ttu-id="98799-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98799-112">Parameters</span></span>

 <span data-ttu-id="98799-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="98799-113">_ftg_</span></span>
  
> <span data-ttu-id="98799-114">[in]関数を有効または無効になっているアイドル状態のルーチンを識別するタグです。</span><span class="sxs-lookup"><span data-stu-id="98799-114">[in] Function tag that identifies the idle routine to be enabled or disabled.</span></span> 
    
 <span data-ttu-id="98799-115">_fEnable_</span><span class="sxs-lookup"><span data-stu-id="98799-115">_fEnable_</span></span>
  
> <span data-ttu-id="98799-116">[in]TRUE が含まれる場合、アイドル状態のエンジンする必要がありますを有効にするアイドル状態のルーチン、または FALSE 場合は、無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98799-116">[in] Contains TRUE if the idle engine should enable the idle routine, or FALSE if it should disable it.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98799-117">Return value</span><span class="sxs-lookup"><span data-stu-id="98799-117">Return value</span></span>

<span data-ttu-id="98799-118">なし。</span><span class="sxs-lookup"><span data-stu-id="98799-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98799-119">注釈</span><span class="sxs-lookup"><span data-stu-id="98799-119">Remarks</span></span>

<span data-ttu-id="98799-120">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="98799-120">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="98799-121">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="98799-121">**Idle routine function**</span></span>|<span data-ttu-id="98799-122">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="98799-122">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98799-123">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="98799-123">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="98799-124">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="98799-124">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="98799-125">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="98799-125">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="98799-126">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="98799-126">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="98799-127">**EnableIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="98799-127">**EnableIdleRoutine**</span></span> <br/> |<span data-ttu-id="98799-128">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="98799-128">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="98799-129">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="98799-129">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="98799-130">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="98799-130">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="98799-131">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="98799-131">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="98799-132">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="98799-132">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="98799-133">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="98799-133">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="98799-134">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="98799-134">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
 <span data-ttu-id="98799-135">**ChangeIdleRoutine**、 **DeregisterIdleRoutine**、および**EnableIdleRoutine**関数のタグは、 **FtgRegisterIdleRoutine**によって返される入力パラメーターとして実行します。</span><span class="sxs-lookup"><span data-stu-id="98799-135">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="98799-136">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98799-136">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="98799-137">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="98799-137">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

