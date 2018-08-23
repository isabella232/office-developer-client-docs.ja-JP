---
title: PidTagReadReceiptRequested 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1d4d4404d175458d5b708948b11c93b734a8bd1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803242"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="d9274-103">PidTagReadReceiptRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9274-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="d9274-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9274-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9274-105">メッセージの送信者は受信者がメッセージを読んだときは、リードのレポートを生成するメッセージング システムを希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9274-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9274-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d9274-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9274-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="d9274-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="d9274-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d9274-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9274-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="d9274-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="d9274-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d9274-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9274-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d9274-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d9274-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d9274-112">Area:</span></span>  <br/> |<span data-ttu-id="d9274-113">メール</span><span class="sxs-lookup"><span data-stu-id="d9274-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9274-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d9274-114">Remarks</span></span>

<span data-ttu-id="d9274-115">このプロパティは、[ **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) と**PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) のプロパティ値を検証するのには TRUE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9274-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="d9274-116">**PR_READ_RECEIPT_REQUESTED**セットを含むメッセージは、削除したり、メッセージング システムは、読み取りレポートを生成する前に有効期限が切れる、nonread のレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="d9274-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9274-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d9274-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9274-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d9274-118">Protocol specifications</span></span>

<span data-ttu-id="d9274-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9274-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9274-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9274-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9274-121">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9274-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9274-122">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9274-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9274-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d9274-123">Header files</span></span>

<span data-ttu-id="d9274-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9274-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9274-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9274-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9274-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9274-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d9274-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9274-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9274-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9274-128">See also</span></span>



[<span data-ttu-id="d9274-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9274-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9274-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9274-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9274-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9274-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9274-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9274-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

