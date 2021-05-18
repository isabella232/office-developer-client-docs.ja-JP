---
title: IAttach IMAPIProp
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
# <a name="iattach--imapiprop"></a><span data-ttu-id="0dbda-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0dbda-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="0dbda-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dbda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dbda-105">メッセージ内の添付ファイルのプロパティへのアクセスを維持し、提供します。</span><span class="sxs-lookup"><span data-stu-id="0dbda-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="0dbda-106">**IAttach インターフェイス** には独自のメソッドはありません。</span><span class="sxs-lookup"><span data-stu-id="0dbda-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="0dbda-107">添付ファイルの使用方法の詳細については、「MAPI 添付ファイルと[添付ファイルテーブル」](mapi-attachments.md)[を参照してください](attachment-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="0dbda-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dbda-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0dbda-108">Header file:</span></span>  <br/> |<span data-ttu-id="0dbda-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dbda-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0dbda-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="0dbda-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="0dbda-111">添付ファイル オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0dbda-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="0dbda-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="0dbda-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="0dbda-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0dbda-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="0dbda-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="0dbda-114">Called by:</span></span>  <br/> |<span data-ttu-id="0dbda-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0dbda-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="0dbda-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="0dbda-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0dbda-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="0dbda-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="0dbda-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="0dbda-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="0dbda-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="0dbda-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="0dbda-120">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="0dbda-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="0dbda-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="0dbda-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0dbda-122">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="0dbda-122">Vtable order</span></span>

<span data-ttu-id="0dbda-123">このインターフェイスには、一意のメソッドが含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0dbda-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="0dbda-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="0dbda-124">**Required properties**</span></span>|<span data-ttu-id="0dbda-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="0dbda-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dbda-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0dbda-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0dbda-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="0dbda-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="0dbda-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0dbda-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0dbda-129">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="0dbda-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="0dbda-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0dbda-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0dbda-131">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="0dbda-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dbda-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dbda-132">See also</span></span>



[<span data-ttu-id="0dbda-133">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="0dbda-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

