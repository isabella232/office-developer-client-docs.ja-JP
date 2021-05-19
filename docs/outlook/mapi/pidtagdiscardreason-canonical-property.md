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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32c81474580dbe4948c40390dadd0445776ab825
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434803"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="bf7a5-103">PidTagDiscardReason 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf7a5-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="bf7a5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf7a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf7a5-105">メッセージ転送エージェント (MTA) がメッセージを破棄した理由が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bf7a5-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf7a5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf7a5-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="bf7a5-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="bf7a5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf7a5-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="bf7a5-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="bf7a5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bf7a5-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf7a5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bf7a5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bf7a5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bf7a5-112">Area:</span></span>  <br/> |<span data-ttu-id="bf7a5-113">MAPI 封筒</span><span class="sxs-lookup"><span data-stu-id="bf7a5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf7a5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bf7a5-114">Remarks</span></span>

<span data-ttu-id="bf7a5-115">このプロパティに含まれる理由は、メッセージの非送信レポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf7a5-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf7a5-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bf7a5-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bf7a5-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bf7a5-117">Header files</span></span>

<span data-ttu-id="bf7a5-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf7a5-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf7a5-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf7a5-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf7a5-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf7a5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="bf7a5-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bf7a5-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf7a5-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf7a5-122">See also</span></span>



[<span data-ttu-id="bf7a5-123">PidTagNonDeliveryReportReasonCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf7a5-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="bf7a5-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bf7a5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf7a5-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf7a5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf7a5-126">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf7a5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf7a5-127">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf7a5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

