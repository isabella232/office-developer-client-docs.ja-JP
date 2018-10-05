---
title: PidTagRecipientProposed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388057"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="7516a-103">PidTagRecipientProposed 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7516a-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="7516a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7516a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7516a-105">会議の出席者が反応したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7516a-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7516a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7516a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7516a-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="7516a-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="7516a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7516a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7516a-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="7516a-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="7516a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7516a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7516a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7516a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7516a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7516a-112">Area:</span></span>  <br/> |<span data-ttu-id="7516a-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="7516a-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7516a-114">備考</span><span class="sxs-lookup"><span data-stu-id="7516a-114">Remarks</span></span>

<span data-ttu-id="7516a-115">このプロパティの値は、出席者が新しい日時を提案することを示します。</span><span class="sxs-lookup"><span data-stu-id="7516a-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="7516a-116">値の false の場合、または、このプロパティがない場合は、まだ応答して、参加者がいないか、出席者からの最新の応答は、新しい日付を含める/時間の提案でしたいないを意味します。</span><span class="sxs-lookup"><span data-stu-id="7516a-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="7516a-117">この値を TRUE にすることはできません定期的な一連の出席者のために。</span><span class="sxs-lookup"><span data-stu-id="7516a-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7516a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7516a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7516a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7516a-119">Protocol specifications</span></span>

<span data-ttu-id="7516a-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7516a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7516a-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7516a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7516a-122">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7516a-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7516a-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7516a-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7516a-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7516a-124">Header files</span></span>

<span data-ttu-id="7516a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7516a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7516a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7516a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7516a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7516a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7516a-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7516a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7516a-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7516a-129">See also</span></span>



[<span data-ttu-id="7516a-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7516a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7516a-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7516a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7516a-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7516a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7516a-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7516a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

