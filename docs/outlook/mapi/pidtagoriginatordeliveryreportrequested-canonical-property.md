---
title: PidTagOriginatorDeliveryReportRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356302"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="e27d3-103">PidTagOriginatorDeliveryReportRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e27d3-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="e27d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e27d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e27d3-105">メッセージがメッセージストアに配置される前に、メッセージ送信者がメッセージングシステムからの特定の受信者の配信レポートを要求する場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e27d3-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e27d3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e27d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e27d3-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="e27d3-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="e27d3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e27d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e27d3-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="e27d3-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="e27d3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e27d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e27d3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e27d3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e27d3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e27d3-112">Area:</span></span>  <br/> |<span data-ttu-id="e27d3-113">MIME</span><span class="sxs-lookup"><span data-stu-id="e27d3-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e27d3-114">解説</span><span class="sxs-lookup"><span data-stu-id="e27d3-114">Remarks</span></span>

<span data-ttu-id="e27d3-115">このプロパティは、配信されたメッセージを処理するようにメッセージングシステムに指示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e27d3-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="e27d3-116">この場合、メッセージでは、 **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="e27d3-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="e27d3-117">メッセージの**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**プロパティを設定することにより、すべての受信者に対して配信状況レポートを要求できます。</span><span class="sxs-lookup"><span data-stu-id="e27d3-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e27d3-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e27d3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e27d3-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e27d3-119">Protocol specifications</span></span>

<span data-ttu-id="e27d3-120">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27d3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27d3-121">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e27d3-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e27d3-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e27d3-122">Header files</span></span>

<span data-ttu-id="e27d3-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e27d3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e27d3-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e27d3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e27d3-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e27d3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e27d3-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e27d3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e27d3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e27d3-127">See also</span></span>



[<span data-ttu-id="e27d3-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e27d3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e27d3-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e27d3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e27d3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e27d3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e27d3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e27d3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

