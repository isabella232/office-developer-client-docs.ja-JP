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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85e78695a7c4fca5a1e5cd28b0254d4559be0c13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315919"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="05df8-103">PidLidRecurring 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05df8-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="05df8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05df8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05df8-105">予定メッセージが繰り返し表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="05df8-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05df8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05df8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05df8-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="05df8-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="05df8-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="05df8-108">Property set:</span></span>  <br/> |<span data-ttu-id="05df8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="05df8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="05df8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="05df8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05df8-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="05df8-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="05df8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05df8-112">Data type:</span></span>  <br/> |<span data-ttu-id="05df8-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="05df8-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="05df8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="05df8-114">Area:</span></span>  <br/> |<span data-ttu-id="05df8-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="05df8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05df8-116">注釈</span><span class="sxs-lookup"><span data-stu-id="05df8-116">Remarks</span></span>

<span data-ttu-id="05df8-117">このプロパティは、予定が定期的な予定の場合は TRUE、定期的ではない場合は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="05df8-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="05df8-118">このプロパティは、オブジェクトが定期的な系列を表すかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="05df8-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="05df8-119">TRUE の値は、オブジェクトが定期的な系列を表します。</span><span class="sxs-lookup"><span data-stu-id="05df8-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="05df8-120">FALSE の値、またはこのプロパティがない場合は、オブジェクトが単一のインスタンスまたは例外 (孤立インスタンスを含む) を表します。</span><span class="sxs-lookup"><span data-stu-id="05df8-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="05df8-121">このプロパティとプロパティ ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md) **)** プロパティLID_IS_RECURRINGの違いに注意してください。</span><span class="sxs-lookup"><span data-stu-id="05df8-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05df8-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05df8-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05df8-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05df8-123">Protocol specifications</span></span>

<span data-ttu-id="05df8-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05df8-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05df8-125">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="05df8-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05df8-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05df8-126">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05df8-127">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="05df8-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05df8-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05df8-128">Header files</span></span>

<span data-ttu-id="05df8-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05df8-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="05df8-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05df8-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05df8-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="05df8-131">See also</span></span>



[<span data-ttu-id="05df8-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="05df8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05df8-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05df8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05df8-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="05df8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05df8-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="05df8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

