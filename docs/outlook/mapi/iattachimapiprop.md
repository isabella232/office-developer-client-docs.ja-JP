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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800387"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="e9c92-103">IAttach: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e9c92-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="e9c92-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9c92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9c92-105">保持し、メッセージの添付ファイルのプロパティへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e9c92-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="e9c92-106">**IAttach**インターフェイスには、独自の一意のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="e9c92-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="e9c92-107">添付ファイルを使用する方法の詳細については、 [MAPI の添付ファイル](mapi-attachments.md)や[添付ファイル テーブル](attachment-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9c92-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9c92-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9c92-108">Header file:</span></span>  <br/> |<span data-ttu-id="e9c92-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9c92-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e9c92-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="e9c92-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e9c92-111">オブジェクトの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="e9c92-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="e9c92-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e9c92-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9c92-113">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9c92-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="e9c92-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e9c92-114">Called by:</span></span>  <br/> |<span data-ttu-id="e9c92-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e9c92-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="e9c92-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="e9c92-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e9c92-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="e9c92-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="e9c92-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="e9c92-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="e9c92-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="e9c92-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="e9c92-120">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="e9c92-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="e9c92-121">トランザクション処理</span><span class="sxs-lookup"><span data-stu-id="e9c92-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e9c92-122">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e9c92-122">Vtable order</span></span>

<span data-ttu-id="e9c92-123">このインターフェイスには、固有のメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="e9c92-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="e9c92-124">**必要なプロパティ**</span><span class="sxs-lookup"><span data-stu-id="e9c92-124">**Required properties**</span></span>|<span data-ttu-id="e9c92-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="e9c92-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9c92-126">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e9c92-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e9c92-127">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e9c92-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="e9c92-128">**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e9c92-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e9c92-129">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="e9c92-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="e9c92-130">**PR_RENDERING_POSITION**([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e9c92-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e9c92-131">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="e9c92-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9c92-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9c92-132">See also</span></span>



[<span data-ttu-id="e9c92-133">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e9c92-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

