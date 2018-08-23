---
title: PidTagDiscardReason 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscardReason
api_type:
- HeaderDef
ms.assetid: 5004dc1f-6bd3-4764-b83c-d04d83161dba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a8835b7234a209d5cb80a19593632380f6d83826
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593159"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="7bdb1-103">PidTagDiscardReason 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdb1-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="7bdb1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bdb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bdb1-105">メッセージ転送エージェント (MTA) がメッセージを破棄する理由の理由が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7bdb1-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bdb1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7bdb1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bdb1-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="7bdb1-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="7bdb1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7bdb1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7bdb1-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="7bdb1-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="7bdb1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7bdb1-110">Data type:</span></span>  <br/> |<span data-ttu-id="7bdb1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7bdb1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7bdb1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7bdb1-112">Area:</span></span>  <br/> |<span data-ttu-id="7bdb1-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="7bdb1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bdb1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7bdb1-114">Remarks</span></span>

<span data-ttu-id="7bdb1-115">このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bdb1-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7bdb1-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7bdb1-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7bdb1-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7bdb1-117">Header files</span></span>

<span data-ttu-id="7bdb1-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bdb1-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bdb1-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7bdb1-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="7bdb1-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7bdb1-120">Mapitags.h</span></span>
  
> <span data-ttu-id="7bdb1-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7bdb1-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bdb1-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bdb1-122">See also</span></span>



[<span data-ttu-id="7bdb1-123">PidTagNonDeliveryReportReasonCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdb1-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="7bdb1-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdb1-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bdb1-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7bdb1-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bdb1-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7bdb1-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bdb1-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7bdb1-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

