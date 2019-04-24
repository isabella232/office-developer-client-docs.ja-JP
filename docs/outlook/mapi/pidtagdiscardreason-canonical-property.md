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
ms.openlocfilehash: 32c81474580dbe4948c40390dadd0445776ab825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360845"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="37a4d-103">PidTagDiscardReason 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37a4d-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="37a4d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37a4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37a4d-105">メッセージ転送エージェント (MTA) がメッセージを破棄した理由が含まれています。</span><span class="sxs-lookup"><span data-stu-id="37a4d-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37a4d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="37a4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37a4d-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="37a4d-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="37a4d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="37a4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37a4d-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="37a4d-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="37a4d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="37a4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="37a4d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37a4d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37a4d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="37a4d-112">Area:</span></span>  <br/> |<span data-ttu-id="37a4d-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="37a4d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37a4d-114">解説</span><span class="sxs-lookup"><span data-stu-id="37a4d-114">Remarks</span></span>

<span data-ttu-id="37a4d-115">このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="37a4d-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37a4d-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="37a4d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="37a4d-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="37a4d-117">Header files</span></span>

<span data-ttu-id="37a4d-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37a4d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="37a4d-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="37a4d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="37a4d-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="37a4d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="37a4d-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="37a4d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37a4d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="37a4d-122">See also</span></span>



[<span data-ttu-id="37a4d-123">PidTagNonDeliveryReportReasonCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37a4d-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="37a4d-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="37a4d-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37a4d-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="37a4d-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37a4d-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="37a4d-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37a4d-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="37a4d-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

