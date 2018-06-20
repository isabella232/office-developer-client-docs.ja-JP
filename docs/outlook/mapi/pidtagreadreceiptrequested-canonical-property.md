---
title: PidTagReadReceiptRequested の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1d4d4404d175458d5b708948b11c93b734a8bd1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803242"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="5a2ff-103">PidTagReadReceiptRequested の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="5a2ff-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="5a2ff-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a2ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a2ff-105">メッセージの送信者は受信者がメッセージを読んだときは、リードのレポートを生成するメッセージング システムを希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a2ff-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a2ff-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="5a2ff-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="5a2ff-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5a2ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a2ff-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="5a2ff-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="5a2ff-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a2ff-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5a2ff-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5a2ff-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5a2ff-112">Area:</span></span>  <br/> |<span data-ttu-id="5a2ff-113">Email</span><span class="sxs-lookup"><span data-stu-id="5a2ff-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a2ff-114">備考</span><span class="sxs-lookup"><span data-stu-id="5a2ff-114">Remarks</span></span>

<span data-ttu-id="5a2ff-115">このプロパティは、[ **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) と**PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) のプロパティ値を検証するのには TRUE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="5a2ff-116">**PR_READ_RECEIPT_REQUESTED**セットを含むメッセージは、削除したり、メッセージング システムは、読み取りレポートを生成する前に有効期限が切れる、nonread のレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a2ff-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5a2ff-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a2ff-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5a2ff-118">Protocol specifications</span></span>

<span data-ttu-id="5a2ff-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a2ff-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a2ff-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a2ff-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a2ff-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a2ff-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a2ff-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5a2ff-123">Header files</span></span>

<span data-ttu-id="5a2ff-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a2ff-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a2ff-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a2ff-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a2ff-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5a2ff-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a2ff-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a2ff-128">See also</span></span>



[<span data-ttu-id="5a2ff-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a2ff-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a2ff-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a2ff-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a2ff-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="5a2ff-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a2ff-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="5a2ff-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

