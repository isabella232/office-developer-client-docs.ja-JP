---
title: PidTagDiscardReason の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4799cd14000b46053d1e571a7ab1c2c0c394a014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802685"
---
# <a name="pidtagdiscardreason-canonical-property"></a><span data-ttu-id="52671-103">PidTagDiscardReason の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="52671-103">PidTagDiscardReason Canonical Property</span></span>

  
  
<span data-ttu-id="52671-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52671-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52671-105">メッセージ転送エージェント (MTA) がメッセージを破棄する理由の理由が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52671-105">Contains a reason why a message transfer agent (MTA) has discarded a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52671-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="52671-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52671-107">PR_DISCARD_REASON</span><span class="sxs-lookup"><span data-stu-id="52671-107">PR_DISCARD_REASON</span></span>  <br/> |
|<span data-ttu-id="52671-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="52671-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52671-109">0x0011</span><span class="sxs-lookup"><span data-stu-id="52671-109">0x0011</span></span>  <br/> |
|<span data-ttu-id="52671-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="52671-110">Data type:</span></span>  <br/> |<span data-ttu-id="52671-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="52671-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="52671-112">領域:</span><span class="sxs-lookup"><span data-stu-id="52671-112">Area:</span></span>  <br/> |<span data-ttu-id="52671-113">MAPI の封筒</span><span class="sxs-lookup"><span data-stu-id="52671-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52671-114">備考</span><span class="sxs-lookup"><span data-stu-id="52671-114">Remarks</span></span>

<span data-ttu-id="52671-115">このプロパティに含まれている理由は、メッセージの配信不能レポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="52671-115">The reason contained in this property is used in a nondelivery report for the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="52671-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="52671-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="52671-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="52671-117">Header files</span></span>

<span data-ttu-id="52671-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="52671-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="52671-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="52671-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="52671-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="52671-120">Mapitags.h</span></span>
  
> <span data-ttu-id="52671-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="52671-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52671-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="52671-122">See also</span></span>



[<span data-ttu-id="52671-123">PidTagNonDeliveryReportReasonCode の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="52671-123">PidTagNonDeliveryReportReasonCode Canonical Property</span></span>](pidtagnondeliveryreportreasoncode-canonical-property.md)


[<span data-ttu-id="52671-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52671-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52671-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="52671-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52671-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="52671-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52671-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="52671-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

