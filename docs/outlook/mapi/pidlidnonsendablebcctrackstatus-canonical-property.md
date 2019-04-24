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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359949"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="c1b03-103">PidLidNonSendableBccTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1b03-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c1b03-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1b03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1b03-105">**dispidnonsendablebcc** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) プロパティに一覧表示されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1b03-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1b03-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c1b03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1b03-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="c1b03-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="c1b03-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="c1b03-108">Property set:</span></span>  <br/> |<span data-ttu-id="c1b03-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c1b03-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c1b03-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c1b03-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c1b03-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="c1b03-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="c1b03-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c1b03-112">Data type:</span></span>  <br/> |<span data-ttu-id="c1b03-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c1b03-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c1b03-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c1b03-114">Area:</span></span>  <br/> |<span data-ttu-id="c1b03-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c1b03-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b03-116">解説</span><span class="sxs-lookup"><span data-stu-id="c1b03-116">Remarks</span></span>

<span data-ttu-id="c1b03-117">このプロパティは、 **dispidnonsendablebcc**プロパティが設定されている場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="c1b03-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="c1b03-118">このプロパティの値の数は、 **dispidnonsendablebcc**の値の数と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c1b03-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="c1b03-119">このプロパティの各値は、同じインデックスにある**dispidnonsendablebcc**プロパティの出席者に対応しています。</span><span class="sxs-lookup"><span data-stu-id="c1b03-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c1b03-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c1b03-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1b03-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c1b03-121">Protocol specifications</span></span>

<span data-ttu-id="c1b03-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b03-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b03-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1b03-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1b03-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1b03-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1b03-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c1b03-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1b03-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c1b03-126">Header files</span></span>

<span data-ttu-id="c1b03-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1b03-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1b03-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1b03-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1b03-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1b03-129">See also</span></span>



[<span data-ttu-id="c1b03-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c1b03-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1b03-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c1b03-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1b03-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1b03-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1b03-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c1b03-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

