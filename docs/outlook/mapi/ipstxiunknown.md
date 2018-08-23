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
ms.openlocfilehash: 98c3f33c5f9b4745787d6acb55d7afb230e23518
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564242"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="bddfd-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bddfd-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="bddfd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bddfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bddfd-105">このインターフェイスは、 **[IOSTX](iostxiunknown.md)** インターフェイスを使用するレプリケーションを実行するときに、ヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="bddfd-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bddfd-106">によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="bddfd-106">Provided by</span></span>  <br/> |<span data-ttu-id="bddfd-107">[IMsgStore](imsgstoreimapiprop.md)に対してクエリを実行</span><span class="sxs-lookup"><span data-stu-id="bddfd-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="bddfd-108">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="bddfd-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bddfd-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="bddfd-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bddfd-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="bddfd-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bddfd-111">**[発生しました](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="bddfd-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="bddfd-112">最後のエラーに関する情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="bddfd-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="bddfd-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="bddfd-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="bddfd-114">関連付けられている**[IOSTX](iostxiunknown.md)** インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="bddfd-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="bddfd-115">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-116">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-117">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-118">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-119">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-120">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-121">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-122">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="bddfd-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="bddfd-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="bddfd-124">サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするためにローカル ストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="bddfd-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="bddfd-125">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-126">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-127">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-128">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-129">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-130">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-131">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-132">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bddfd-133">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="bddfd-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bddfd-134">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="bddfd-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bddfd-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="bddfd-135">See also</span></span>



[<span data-ttu-id="bddfd-136">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="bddfd-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bddfd-137">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="bddfd-137">MAPI Constants</span></span>](mapi-constants.md)

