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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408209"
---
# <a name="mapideinitidle"></a><span data-ttu-id="30dd7-103">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="30dd7-103">MAPIDeInitIdle</span></span>

  
  
<span data-ttu-id="30dd7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30dd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30dd7-105">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30dd7-105">Shuts down the MAPI idle engine for the calling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30dd7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="30dd7-106">Header file:</span></span>  <br/> |<span data-ttu-id="30dd7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="30dd7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="30dd7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="30dd7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="30dd7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="30dd7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="30dd7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="30dd7-110">Called by:</span></span>  <br/> |<span data-ttu-id="30dd7-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="30dd7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a><span data-ttu-id="30dd7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30dd7-112">Parameters</span></span>

<span data-ttu-id="30dd7-113">なし。</span><span class="sxs-lookup"><span data-stu-id="30dd7-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="30dd7-114">Return value</span><span class="sxs-lookup"><span data-stu-id="30dd7-114">Return value</span></span>

<span data-ttu-id="30dd7-115">なし。</span><span class="sxs-lookup"><span data-stu-id="30dd7-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30dd7-116">注釈</span><span class="sxs-lookup"><span data-stu-id="30dd7-116">Remarks</span></span>

<span data-ttu-id="30dd7-117">クライアント アプリケーションまたはサービス プロバイダーは、アイドル 状態のエンジンが不要になったときに **MAPIDeInitIdle** を呼び出す必要があります 。たとえば、処理を停止する場合などです。</span><span class="sxs-lookup"><span data-stu-id="30dd7-117">A client application or service provider should call **MAPIDeInitIdle** when it no longer needs the idle engine, for example, when it is about to stop processing.</span></span> 
  
<span data-ttu-id="30dd7-118">[MAPIInitIdle](mapiinitidle.md)へのすべての呼び出しは **、MAPIDeInitIdle** への後続の呼び出しによって一致する必要があります。または、アイドル 状態のエンジンが呼び出し元のアプリケーションに対して実行された状態を残している必要があります。</span><span class="sxs-lookup"><span data-stu-id="30dd7-118">Every call to [MAPIInitIdle](mapiinitidle.md) must be matched by a subsequent call to **MAPIDeInitIdle**, or the idle engine is left running for the calling application.</span></span> 
  
<span data-ttu-id="30dd7-119">次の関数は、MAPI アイドル エンジンと [、FNIDLE](fnidle.md) 関数プロトタイプに基づくアイドル ルーチンを処理します。</span><span class="sxs-lookup"><span data-stu-id="30dd7-119">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="30dd7-120">**アイドル ルーチン関数**</span><span class="sxs-lookup"><span data-stu-id="30dd7-120">**Idle routine function**</span></span>|<span data-ttu-id="30dd7-121">**使用状況**</span><span class="sxs-lookup"><span data-stu-id="30dd7-121">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30dd7-122">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30dd7-122">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="30dd7-123">登録済みのアイドル ルーチンの特性を変更します。</span><span class="sxs-lookup"><span data-stu-id="30dd7-123">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="30dd7-124">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30dd7-124">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="30dd7-125">MAPI システムから登録済みのアイドル ルーチンを削除します。</span><span class="sxs-lookup"><span data-stu-id="30dd7-125">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="30dd7-126">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30dd7-126">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="30dd7-127">MAPI システムから削除せずに、登録済みのアイドル ルーチンを無効または再び有効にします。</span><span class="sxs-lookup"><span data-stu-id="30dd7-127">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="30dd7-128">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="30dd7-128">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="30dd7-129">MAPI システムにアイドル 状態のルーチンを追加します。有効にするか、有効にしないか。</span><span class="sxs-lookup"><span data-stu-id="30dd7-129">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|<span data-ttu-id="30dd7-130">**MAPIDeInitIdle**</span><span class="sxs-lookup"><span data-stu-id="30dd7-130">**MAPIDeInitIdle**</span></span> <br/> |<span data-ttu-id="30dd7-131">呼び出し元のアプリケーションの MAPI アイドル エンジンをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="30dd7-131">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="30dd7-132">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="30dd7-132">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="30dd7-133">呼び出し元のアプリケーションの MAPI アイドル エンジンを初期化します。</span><span class="sxs-lookup"><span data-stu-id="30dd7-133">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="30dd7-134">プラットフォームのすべてのフォアグラウンド タスクがアイドル状態になると、MAPI アイドル エンジンは、実行の準備ができている優先度の高いアイドル ルーチンを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="30dd7-134">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="30dd7-135">同じ優先度のアイドル ルーチン間で順序を呼び出す保証はありません。</span><span class="sxs-lookup"><span data-stu-id="30dd7-135">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

