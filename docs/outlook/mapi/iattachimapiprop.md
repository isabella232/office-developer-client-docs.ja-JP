---
title: iattach imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409091"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="206d2-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="206d2-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="206d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="206d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="206d2-105">メッセージ内の添付ファイルのプロパティへのアクセスを保持および提供します。</span><span class="sxs-lookup"><span data-stu-id="206d2-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="206d2-106">**iattach**インターフェイスには、独自の独自のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="206d2-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="206d2-107">添付ファイルの使用方法の詳細については、「 [MAPI 添付](mapi-attachments.md)ファイルと[添付ファイルの表](attachment-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="206d2-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="206d2-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="206d2-108">Header file:</span></span>  <br/> |<span data-ttu-id="206d2-109">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="206d2-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="206d2-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="206d2-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="206d2-111">Attachment オブジェクト</span><span class="sxs-lookup"><span data-stu-id="206d2-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="206d2-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="206d2-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="206d2-113">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="206d2-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="206d2-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="206d2-114">Called by:</span></span>  <br/> |<span data-ttu-id="206d2-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="206d2-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="206d2-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="206d2-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="206d2-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="206d2-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="206d2-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="206d2-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="206d2-119">lpattach</span><span class="sxs-lookup"><span data-stu-id="206d2-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="206d2-120">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="206d2-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="206d2-121">一括</span><span class="sxs-lookup"><span data-stu-id="206d2-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="206d2-122">v の順序</span><span class="sxs-lookup"><span data-stu-id="206d2-122">Vtable order</span></span>

<span data-ttu-id="206d2-123">このインターフェイスには一意のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="206d2-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="206d2-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="206d2-124">**Required properties**</span></span>|<span data-ttu-id="206d2-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="206d2-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="206d2-126">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="206d2-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="206d2-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="206d2-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="206d2-128">**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="206d2-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="206d2-129">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="206d2-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="206d2-130">**PR_RENDERING_POSITION**([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="206d2-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="206d2-131">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="206d2-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="206d2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="206d2-132">See also</span></span>



[<span data-ttu-id="206d2-133">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="206d2-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

