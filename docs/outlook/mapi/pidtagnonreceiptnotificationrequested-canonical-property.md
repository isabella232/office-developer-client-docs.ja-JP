---
title: PidTagNonReceiptNotificationRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 896cfa2bf8a1b33fd6dee09649853b71618f31be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582785"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="d3b8e-103">PidTagNonReceiptNotificationRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d3b8e-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="d3b8e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3b8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3b8e-105">メッセージの送信者が指定した受信者の受信不能の通知を希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3b8e-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3b8e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d3b8e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3b8e-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="d3b8e-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="d3b8e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d3b8e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3b8e-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="d3b8e-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="d3b8e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d3b8e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3b8e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d3b8e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d3b8e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d3b8e-112">Area:</span></span>  <br/> |<span data-ttu-id="d3b8e-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="d3b8e-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3b8e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d3b8e-114">Remarks</span></span>

<span data-ttu-id="d3b8e-115">このプロパティに FALSE が含まれている**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) のプロパティに TRUE が含まれている場合は、サービス プロバイダーは、 **PR_NON_RECEIPT_NOTIFICATION_REQUESTED**プロパティをオーバーライドして生成します。配信不能レポートです。</span><span class="sxs-lookup"><span data-stu-id="d3b8e-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3b8e-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d3b8e-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d3b8e-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d3b8e-117">Header files</span></span>

<span data-ttu-id="d3b8e-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3b8e-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3b8e-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3b8e-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3b8e-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3b8e-120">Mapitags.h</span></span>
  
> <span data-ttu-id="d3b8e-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3b8e-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3b8e-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3b8e-122">See also</span></span>



[<span data-ttu-id="d3b8e-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d3b8e-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3b8e-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d3b8e-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3b8e-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d3b8e-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3b8e-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d3b8e-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

