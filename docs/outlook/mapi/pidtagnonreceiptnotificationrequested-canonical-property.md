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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c6b56a786ea794587e140c9555cc88cd862b489
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419752"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a><span data-ttu-id="3debf-103">PidTagNonReceiptNotificationRequested 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3debf-103">PidTagNonReceiptNotificationRequested Canonical Property</span></span>

  
  
<span data-ttu-id="3debf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3debf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3debf-105">メッセージの送信者が、指定された受信者に対して配信不能通知を要求している場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3debf-105">Contains TRUE if a message sender wants notification of non-receipt for a specified recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3debf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3debf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3debf-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="3debf-107">PR_NON_RECEIPT_NOTIFICATION_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="3debf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3debf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3debf-109">0x0c06</span><span class="sxs-lookup"><span data-stu-id="3debf-109">0x0C06</span></span>  <br/> |
|<span data-ttu-id="3debf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3debf-110">Data type:</span></span>  <br/> |<span data-ttu-id="3debf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3debf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3debf-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3debf-112">Area:</span></span>  <br/> |<span data-ttu-id="3debf-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="3debf-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3debf-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3debf-114">Remarks</span></span>

<span data-ttu-id="3debf-115">このプロパティに FALSE が含まれ、 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティに TRUE が含まれている場合、サービスプロバイダーは**PR_NON_RECEIPT_NOTIFICATION_REQUESTED**プロパティを上書きし、配信不能レポート。</span><span class="sxs-lookup"><span data-stu-id="3debf-115">If this property contains FALSE and the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property contains TRUE, the service provider can override the **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** property and generate a non-delivery report.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3debf-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3debf-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3debf-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3debf-117">Header files</span></span>

<span data-ttu-id="3debf-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3debf-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="3debf-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3debf-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="3debf-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3debf-120">Mapitags.h</span></span>
  
> <span data-ttu-id="3debf-121">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3debf-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3debf-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="3debf-122">See also</span></span>



[<span data-ttu-id="3debf-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3debf-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3debf-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3debf-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3debf-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3debf-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3debf-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3debf-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

