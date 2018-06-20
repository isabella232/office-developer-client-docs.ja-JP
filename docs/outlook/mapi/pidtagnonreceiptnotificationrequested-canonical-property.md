---
title: PidTagNonReceiptNotificationRequested の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803021"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="8fd8a-103">PidTagNonReceiptNotificationRequested の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd8a-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="8fd8a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fd8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fd8a-105">メッセージの送信者が指定した受信者の受信不能の通知を希望する場合は TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fd8a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fd8a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="8fd8a-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="8fd8a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8fd8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fd8a-109">0x0C06</span><span class="sxs-lookup"><span data-stu-id="8fd8a-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="8fd8a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fd8a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8fd8a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8fd8a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8fd8a-112">Area:</span></span>  <br/> |<span data-ttu-id="8fd8a-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="8fd8a-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fd8a-114">備考</span><span class="sxs-lookup"><span data-stu-id="8fd8a-114">Remarks</span></span>

<span data-ttu-id="8fd8a-115">このプロパティに FALSE が含まれている**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) のプロパティに TRUE が含まれている場合は、サービス プロバイダーは、 **PR_NON_RECEIPT_NOTIFICATION_REQUESTED**プロパティをオーバーライドして生成します。配信不能レポートです。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8fd8a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8fd8a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8fd8a-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8fd8a-117">Header files</span></span>

<span data-ttu-id="8fd8a-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fd8a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fd8a-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fd8a-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8fd8a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8fd8a-121">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fd8a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8fd8a-122">See also</span></span>



[<span data-ttu-id="8fd8a-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd8a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fd8a-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8fd8a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fd8a-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8fd8a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fd8a-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8fd8a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

