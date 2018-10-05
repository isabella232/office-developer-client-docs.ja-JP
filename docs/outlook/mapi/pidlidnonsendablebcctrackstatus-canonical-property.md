---
title: PidLidNonSendableBccTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386944"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="94670-103">PidLidNonSendableBccTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="94670-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="94670-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94670-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94670-105">**DispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94670-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94670-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="94670-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94670-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="94670-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="94670-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="94670-108">Property set:</span></span>  <br/> |<span data-ttu-id="94670-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="94670-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="94670-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="94670-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="94670-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="94670-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="94670-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="94670-112">Data type:</span></span>  <br/> |<span data-ttu-id="94670-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="94670-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="94670-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="94670-114">Area:</span></span>  <br/> |<span data-ttu-id="94670-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="94670-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94670-116">備考</span><span class="sxs-lookup"><span data-stu-id="94670-116">Remarks</span></span>

<span data-ttu-id="94670-117">**DispidNonSendableBCC**プロパティが設定されている場合にのみ、このプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="94670-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="94670-118">このプロパティの値の数は、 **dispidNonSendableBCC**内の値の数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="94670-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="94670-119">このプロパティの各値は、同じインデックス位置にある**dispidNonSendableBCC**プロパティに出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="94670-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94670-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="94670-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94670-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="94670-121">Protocol specifications</span></span>

<span data-ttu-id="94670-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94670-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94670-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="94670-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94670-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94670-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94670-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="94670-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94670-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="94670-126">Header files</span></span>

<span data-ttu-id="94670-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94670-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="94670-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="94670-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94670-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="94670-129">See also</span></span>



[<span data-ttu-id="94670-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="94670-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94670-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="94670-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94670-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94670-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94670-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="94670-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

