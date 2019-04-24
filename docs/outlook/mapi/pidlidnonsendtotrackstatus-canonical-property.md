---
title: PidLidNonSendToTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331368"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="2d570-103">PidLidNonSendToTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d570-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="2d570-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d570-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d570-105">**dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) プロパティに表示される各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d570-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d570-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2d570-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d570-107">dispidnonsendtotrackstatus</span><span class="sxs-lookup"><span data-stu-id="2d570-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="2d570-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="2d570-108">Property set:</span></span>  <br/> |<span data-ttu-id="2d570-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2d570-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2d570-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2d570-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2d570-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="2d570-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="2d570-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2d570-112">Data type:</span></span>  <br/> |<span data-ttu-id="2d570-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="2d570-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="2d570-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="2d570-114">Area:</span></span>  <br/> |<span data-ttu-id="2d570-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="2d570-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d570-116">解説</span><span class="sxs-lookup"><span data-stu-id="2d570-116">Remarks</span></span>

<span data-ttu-id="2d570-117">このプロパティは、 **dispidNonSendableTo**プロパティが設定されている場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="2d570-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="2d570-118">このプロパティの値の数は、 **dispidNonSendableTo**の値の数と等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2d570-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="2d570-119">このプロパティの各 PT_LONG 値は、同じインデックスの**dispidNonSendableTo**プロパティの出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="2d570-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d570-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2d570-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d570-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2d570-121">Protocol specifications</span></span>

<span data-ttu-id="2d570-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d570-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d570-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2d570-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d570-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d570-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d570-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d570-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d570-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2d570-126">Header files</span></span>

<span data-ttu-id="2d570-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d570-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d570-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2d570-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d570-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d570-129">See also</span></span>



[<span data-ttu-id="2d570-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2d570-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d570-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d570-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d570-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d570-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d570-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d570-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

