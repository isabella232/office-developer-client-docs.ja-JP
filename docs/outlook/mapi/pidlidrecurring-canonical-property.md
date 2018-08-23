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
ms.openlocfilehash: c1b8c55a019ee3243de18d5e20ee4084bf6ca11f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581252"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="59535-103">PidLidRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="59535-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="59535-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59535-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59535-105">予定のメッセージが繰り返しかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59535-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59535-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="59535-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59535-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="59535-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="59535-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="59535-108">Property set:</span></span>  <br/> |<span data-ttu-id="59535-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="59535-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="59535-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="59535-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="59535-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="59535-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="59535-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="59535-112">Data type:</span></span>  <br/> |<span data-ttu-id="59535-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="59535-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="59535-114">領域:</span><span class="sxs-lookup"><span data-stu-id="59535-114">Area:</span></span>  <br/> |<span data-ttu-id="59535-115">予定表</span><span class="sxs-lookup"><span data-stu-id="59535-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59535-116">注釈</span><span class="sxs-lookup"><span data-stu-id="59535-116">Remarks</span></span>

<span data-ttu-id="59535-117">予定は定期的な予定の場合で、定期的なしない場合は、FALSE の場合、このプロパティは TRUE です。</span><span class="sxs-lookup"><span data-stu-id="59535-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="59535-118">このプロパティは、オブジェクトが定期的な系列を表すかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59535-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="59535-119">TRUE の値は、オブジェクトが一連の定期的なであることを示します。</span><span class="sxs-lookup"><span data-stu-id="59535-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="59535-120">値 FALSE、または、このプロパティがない場合は、オブジェクトが 1 つのインスタンスまたは (孤立したインスタンスを含む) の例外のいずれかを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="59535-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="59535-121">このプロパティは、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) のプロパティの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="59535-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59535-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="59535-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="59535-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="59535-123">Protocol specifications</span></span>

<span data-ttu-id="59535-124">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59535-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59535-125">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="59535-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="59535-126">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="59535-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="59535-127">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="59535-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="59535-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="59535-128">Header files</span></span>

<span data-ttu-id="59535-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="59535-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="59535-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="59535-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59535-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="59535-131">See also</span></span>



[<span data-ttu-id="59535-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="59535-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59535-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="59535-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59535-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="59535-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59535-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="59535-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

