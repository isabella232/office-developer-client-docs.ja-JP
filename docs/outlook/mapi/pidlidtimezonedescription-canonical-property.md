---
title: PidLidTimeZoneDescription 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneDescription
api_type:
- COM
ms.assetid: 24cb6429-1276-45f1-be0e-6c9d2ff6ce19
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ef68da1723a87fa30861eca5668ee94707f43c8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351149"
---
# <a name="pidlidtimezonedescription-canonical-property"></a><span data-ttu-id="e695a-103">PidLidTimeZoneDescription 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e695a-103">PidLidTimeZoneDescription Canonical Property</span></span>

  
  
<span data-ttu-id="e695a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e695a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e695a-105">タイムゾーンの文字列の説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="e695a-105">Specifies a string description of the time zone.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e695a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e695a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e695a-107">dispidTimeZoneDesc</span><span class="sxs-lookup"><span data-stu-id="e695a-107">dispidTimeZoneDesc</span></span>  <br/> |
|<span data-ttu-id="e695a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e695a-108">Property set:</span></span>  <br/> |<span data-ttu-id="e695a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e695a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e695a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e695a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e695a-111">0x00008234</span><span class="sxs-lookup"><span data-stu-id="e695a-111">0x00008234</span></span>  <br/> |
|<span data-ttu-id="e695a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e695a-112">Data type:</span></span>  <br/> |<span data-ttu-id="e695a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e695a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e695a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e695a-114">Area:</span></span>  <br/> |<span data-ttu-id="e695a-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="e695a-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e695a-116">解説</span><span class="sxs-lookup"><span data-stu-id="e695a-116">Remarks</span></span>

<span data-ttu-id="e695a-117">このプロパティは、 **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) プロパティのデータによって表されるタイムゾーンの、人間が判読できる説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="e695a-117">This property specifies a human-readable description of the time zone that is represented by the data in the **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e695a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e695a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e695a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e695a-119">Protocol specifications</span></span>

<span data-ttu-id="e695a-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e695a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e695a-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e695a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e695a-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e695a-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e695a-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e695a-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e695a-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e695a-124">Header files</span></span>

<span data-ttu-id="e695a-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e695a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e695a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e695a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e695a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e695a-127">See also</span></span>



[<span data-ttu-id="e695a-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e695a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e695a-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e695a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e695a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e695a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e695a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e695a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

