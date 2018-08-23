---
title: PidTagOriginatorNonDeliveryReportRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 86b5d76cab1b85b38d76315cf7d905d1a07f0777
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569065"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="ac69c-103">PidTagOriginatorNonDeliveryReportRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac69c-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="ac69c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac69c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac69c-105">メッセージの送信者は、特定の受信者に配信不能レポートを要求した場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ac69c-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac69c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ac69c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac69c-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="ac69c-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="ac69c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ac69c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac69c-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="ac69c-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="ac69c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ac69c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac69c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac69c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ac69c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ac69c-112">Area:</span></span>  <br/> |<span data-ttu-id="ac69c-113">MIME</span><span class="sxs-lookup"><span data-stu-id="ac69c-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac69c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ac69c-114">Remarks</span></span>

<span data-ttu-id="ac69c-115">未配信のメッセージを処理するときのメッセージをシステムに指示するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac69c-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="ac69c-116">この例では、メッセージは**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定をも提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac69c-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac69c-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ac69c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac69c-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ac69c-118">Protocol specifications</span></span>

<span data-ttu-id="ac69c-119">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac69c-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac69c-120">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ac69c-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac69c-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ac69c-121">Header files</span></span>

<span data-ttu-id="ac69c-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac69c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac69c-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac69c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac69c-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ac69c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ac69c-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac69c-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac69c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac69c-126">See also</span></span>



[<span data-ttu-id="ac69c-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac69c-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac69c-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ac69c-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac69c-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac69c-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac69c-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ac69c-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

