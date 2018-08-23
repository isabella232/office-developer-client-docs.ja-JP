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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570913"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="88f30-103">IAttach : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="88f30-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="88f30-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88f30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88f30-105">保持し、メッセージの添付ファイルのプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="88f30-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="88f30-106">**IAttach**インターフェイスには、独自の一意のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="88f30-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="88f30-107">添付ファイルを使用する方法の詳細については、 [MAPI の添付ファイル](mapi-attachments.md)や[添付ファイル テーブル](attachment-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88f30-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88f30-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="88f30-108">Header file:</span></span>  <br/> |<span data-ttu-id="88f30-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88f30-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="88f30-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="88f30-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="88f30-111">オブジェクトの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="88f30-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="88f30-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="88f30-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="88f30-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="88f30-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="88f30-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="88f30-114">Called by:</span></span>  <br/> |<span data-ttu-id="88f30-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="88f30-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="88f30-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="88f30-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="88f30-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="88f30-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="88f30-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="88f30-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="88f30-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="88f30-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="88f30-120">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="88f30-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="88f30-121">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="88f30-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="88f30-122">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="88f30-122">Vtable order</span></span>

<span data-ttu-id="88f30-123">このインターフェイスには、固有のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="88f30-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="88f30-124">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="88f30-124">**Required properties**</span></span>|<span data-ttu-id="88f30-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="88f30-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88f30-126">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88f30-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88f30-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="88f30-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="88f30-128">**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88f30-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88f30-129">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="88f30-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="88f30-130">**PR_RENDERING_POSITION**([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="88f30-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="88f30-131">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="88f30-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88f30-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="88f30-132">See also</span></span>



[<span data-ttu-id="88f30-133">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="88f30-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

