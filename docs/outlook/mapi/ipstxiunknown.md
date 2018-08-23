---
title: IPSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX
api_type:
- COM
ms.assetid: 73752f57-6fbc-0201-bf95-0e75c56c04e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e7df570851aa515e07117d05103f7c0631c90f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801205"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="e2753-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2753-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="e2753-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e2753-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e2753-105">このインターフェイスは、 **[IOSTX](iostxiunknown.md)** インターフェイスを使用するレプリケーションを実行するときに、ヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2753-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2753-106">によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-106">Provided by</span></span>  <br/> |<span data-ttu-id="e2753-107">[IMsgStore](imsgstoreimapiprop.md)に対してクエリを実行</span><span class="sxs-lookup"><span data-stu-id="e2753-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="e2753-108">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="e2753-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e2753-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="e2753-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e2753-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e2753-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2753-111">**[発生しました](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="e2753-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="e2753-112">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="e2753-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="e2753-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="e2753-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="e2753-114">関連付けられている**[IOSTX](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="e2753-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="e2753-115">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-116">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-117">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-118">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-119">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-120">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-121">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-122">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e2753-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="e2753-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="e2753-124">サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするためにローカル ストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="e2753-125">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-126">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-127">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-128">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-129">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-130">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-131">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-132">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e2753-133">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="e2753-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e2753-134">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="e2753-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2753-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2753-135">See also</span></span>



[<span data-ttu-id="e2753-136">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e2753-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e2753-137">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e2753-137">MAPI Constants</span></span>](mapi-constants.md)

