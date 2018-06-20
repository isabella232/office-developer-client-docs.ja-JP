---
title: PidTagOriginatorNonDeliveryReportRequested の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 841d2b14efc781d89727b0c7ed677f527526a4ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803111"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="9bf08-103">PidTagOriginatorNonDeliveryReportRequested の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9bf08-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="9bf08-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bf08-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bf08-105">メッセージの送信者は、特定の受信者に配信不能レポートを要求した場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="9bf08-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bf08-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9bf08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bf08-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="9bf08-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="9bf08-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9bf08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9bf08-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="9bf08-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="9bf08-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9bf08-110">Data type:</span></span>  <br/> |<span data-ttu-id="9bf08-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9bf08-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9bf08-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9bf08-112">Area:</span></span>  <br/> |<span data-ttu-id="9bf08-113">MIME</span><span class="sxs-lookup"><span data-stu-id="9bf08-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bf08-114">備考</span><span class="sxs-lookup"><span data-stu-id="9bf08-114">Remarks</span></span>

<span data-ttu-id="9bf08-115">未配信のメッセージを処理するときのメッセージをシステムに指示するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9bf08-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="9bf08-116">この例では、メッセージは**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定をも提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bf08-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bf08-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9bf08-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bf08-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9bf08-118">Protocol specifications</span></span>

<span data-ttu-id="9bf08-119">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bf08-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bf08-120">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9bf08-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bf08-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9bf08-121">Header files</span></span>

<span data-ttu-id="9bf08-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bf08-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bf08-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9bf08-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="9bf08-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9bf08-124">Mapitags.h</span></span>
  
> <span data-ttu-id="9bf08-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9bf08-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bf08-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="9bf08-126">See also</span></span>



[<span data-ttu-id="9bf08-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bf08-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bf08-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9bf08-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bf08-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9bf08-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bf08-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9bf08-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

