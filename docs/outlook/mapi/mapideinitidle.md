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
ms.openlocfilehash: 33f4634623662b7bc09e0830e8bd0b51adc7799d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583499"
---
# <a name="mapideinitidle"></a><span data-ttu-id="ba29a-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="ba29a-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="ba29a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba29a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba29a-105">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="ba29a-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba29a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ba29a-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba29a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ba29a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ba29a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ba29a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba29a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba29a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba29a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ba29a-110">Called by:</span></span>  <br/> |<span data-ttu-id="ba29a-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ba29a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="ba29a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba29a-112">Parameters</span></span>

<span data-ttu-id="ba29a-113">なし。</span><span class="sxs-lookup"><span data-stu-id="ba29a-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="ba29a-114">Return value</span><span class="sxs-lookup"><span data-stu-id="ba29a-114">Return value</span></span>

<span data-ttu-id="ba29a-115">なし。</span><span class="sxs-lookup"><span data-stu-id="ba29a-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba29a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="ba29a-116">Remarks</span></span>

<span data-ttu-id="ba29a-117">クライアント アプリケーションまたはサービス プロバイダーは、不要になったときに必要なアイドル状態のエンジンでは、たとえば、処理を停止しようとしているときに**MAPIDeInitIdle**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba29a-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="ba29a-118">[MAPIInitIdle](mapiinitidle.md)へのすべての呼び出しを**MAPIDeInitIdle**、それ以降の呼び出しに一致する必要があるまたは呼び出し元のアプリケーションを実行しているアイドル状態のエンジンのままです。</span><span class="sxs-lookup"><span data-stu-id="ba29a-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="ba29a-119">次の関数では、MAPI アイドル エンジンと[FNIDLE](fnidle.md)関数のプロトタイプに基づくのアイドル処理ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="ba29a-120">**アイドル状態の日常的な関数**</span><span class="sxs-lookup"><span data-stu-id="ba29a-120">**Idle routine function**</span></span>|<span data-ttu-id="ba29a-121">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="ba29a-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba29a-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ba29a-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="ba29a-123">登録されているアイドル状態のルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="ba29a-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ba29a-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="ba29a-125">MAPI システムから登録されているアイドル状態のルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ba29a-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ba29a-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="ba29a-127">無効または MAPI システムから削除することがなく、登録されているアイドル状態のルーチンを再度有効にします。</span><span class="sxs-lookup"><span data-stu-id="ba29a-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="ba29a-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="ba29a-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="ba29a-129">MAPI システム、またはそれを有効にせずに、アイドル状態のルーチンを追加します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="ba29a-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="ba29a-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="ba29a-131">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャット ダウンします。</span><span class="sxs-lookup"><span data-stu-id="ba29a-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="ba29a-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="ba29a-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="ba29a-133">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="ba29a-134">プラットフォーム用のすべてのフォア グラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは実行する準備が最高の優先順位のアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ba29a-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="ba29a-135">同じ優先順位のアイドル処理ルーチンの間で順序を呼び出すことの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="ba29a-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

