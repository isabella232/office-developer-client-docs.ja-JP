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
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341959"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="75374-103">PidTagOriginatorNonDeliveryReportRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75374-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="75374-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75374-105">メッセージ送信者が特定の受信者の配信不能レポートを要求する場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="75374-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75374-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="75374-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75374-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="75374-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="75374-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="75374-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75374-109">0x0c08</span><span class="sxs-lookup"><span data-stu-id="75374-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="75374-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="75374-110">Data type:</span></span>  <br/> |<span data-ttu-id="75374-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="75374-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="75374-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="75374-112">Area:</span></span>  <br/> |<span data-ttu-id="75374-113">MIME</span><span class="sxs-lookup"><span data-stu-id="75374-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75374-114">解説</span><span class="sxs-lookup"><span data-stu-id="75374-114">Remarks</span></span>

<span data-ttu-id="75374-115">このプロパティは、配信できないメッセージを処理するようにメッセージングシステムに指示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="75374-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="75374-116">この場合、メッセージでは、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="75374-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75374-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="75374-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75374-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="75374-118">Protocol specifications</span></span>

<span data-ttu-id="75374-119">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75374-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75374-120">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="75374-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75374-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="75374-121">Header files</span></span>

<span data-ttu-id="75374-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75374-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="75374-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="75374-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="75374-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="75374-124">Mapitags.h</span></span>
  
> <span data-ttu-id="75374-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75374-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75374-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="75374-126">See also</span></span>



[<span data-ttu-id="75374-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="75374-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75374-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75374-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75374-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="75374-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75374-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="75374-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

