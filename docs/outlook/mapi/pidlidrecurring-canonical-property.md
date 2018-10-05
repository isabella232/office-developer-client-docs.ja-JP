---
title: PidLidRecurring 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399481"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="abbf0-103">PidLidRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="abbf0-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="abbf0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abbf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abbf0-105">予定のメッセージが繰り返しかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abbf0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="abbf0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abbf0-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="abbf0-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="abbf0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-108">Property set:</span></span>  <br/> |<span data-ttu-id="abbf0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="abbf0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="abbf0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="abbf0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abbf0-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="abbf0-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="abbf0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="abbf0-112">Data type:</span></span>  <br/> |<span data-ttu-id="abbf0-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="abbf0-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="abbf0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="abbf0-114">Area:</span></span>  <br/> |<span data-ttu-id="abbf0-115">予定表</span><span class="sxs-lookup"><span data-stu-id="abbf0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abbf0-116">備考</span><span class="sxs-lookup"><span data-stu-id="abbf0-116">Remarks</span></span>

<span data-ttu-id="abbf0-117">予定は定期的な予定の場合で、定期的なしない場合は、FALSE の場合、このプロパティは TRUE です。</span><span class="sxs-lookup"><span data-stu-id="abbf0-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="abbf0-118">このプロパティは、オブジェクトが定期的な系列を表すかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="abbf0-119">TRUE の値は、オブジェクトが一連の定期的なであることを示します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="abbf0-120">値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスまたは (孤立したインスタンスを含む) の例外のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="abbf0-121">このプロパティは、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) のプロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="abbf0-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abbf0-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="abbf0-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abbf0-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="abbf0-123">Protocol specifications</span></span>

<span data-ttu-id="abbf0-124">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf0-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf0-125">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abbf0-126">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abbf0-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abbf0-127">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abbf0-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="abbf0-128">Header files</span></span>

<span data-ttu-id="abbf0-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abbf0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="abbf0-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="abbf0-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abbf0-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="abbf0-131">See also</span></span>



[<span data-ttu-id="abbf0-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="abbf0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abbf0-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="abbf0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abbf0-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="abbf0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abbf0-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="abbf0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

