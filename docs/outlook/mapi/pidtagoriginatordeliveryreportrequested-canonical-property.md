---
title: PidTagOriginatorDeliveryReportRequested の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803126"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="ad1b6-103">PidTagOriginatorDeliveryReportRequested の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ad1b6-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="ad1b6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad1b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad1b6-105">メッセージの送信者は、メッセージがメッセージ ・ ストアに配置される前に特定の受信者のメッセージング システムから、配信レポートを要求した場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad1b6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad1b6-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="ad1b6-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="ad1b6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ad1b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad1b6-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="ad1b6-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="ad1b6-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad1b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ad1b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ad1b6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ad1b6-112">Area:</span></span>  <br/> |<span data-ttu-id="ad1b6-113">MIME</span><span class="sxs-lookup"><span data-stu-id="ad1b6-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad1b6-114">備考</span><span class="sxs-lookup"><span data-stu-id="ad1b6-114">Remarks</span></span>

<span data-ttu-id="ad1b6-115">メッセージング システムに配信されるメッセージの処理を指示するこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="ad1b6-116">この例では、メッセージは**PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定をも提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="ad1b6-117">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**プロパティをメッセージの設定は、すべての受信者に対する配信状態レポートを要求する方法です。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad1b6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ad1b6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ad1b6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ad1b6-119">Protocol specifications</span></span>

<span data-ttu-id="ad1b6-120">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ad1b6-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ad1b6-121">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ad1b6-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ad1b6-122">Header files</span></span>

<span data-ttu-id="ad1b6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad1b6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad1b6-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad1b6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad1b6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ad1b6-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad1b6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad1b6-127">See also</span></span>



[<span data-ttu-id="ad1b6-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad1b6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad1b6-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ad1b6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad1b6-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ad1b6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad1b6-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ad1b6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

