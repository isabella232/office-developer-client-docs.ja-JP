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
ms.openlocfilehash: 6f025d54632fdb88a846f978b38a476355395b61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563374"
---
# <a name="pidlidtimezonedescription-canonical-property"></a><span data-ttu-id="a28b2-103">PidLidTimeZoneDescription 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a28b2-103">PidLidTimeZoneDescription Canonical Property</span></span>

  
  
<span data-ttu-id="a28b2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a28b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a28b2-105">タイム ゾーンについて説明する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-105">Specifies a string description of the time zone.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a28b2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a28b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a28b2-107">dispidTimeZoneDesc</span><span class="sxs-lookup"><span data-stu-id="a28b2-107">dispidTimeZoneDesc</span></span>  <br/> |
|<span data-ttu-id="a28b2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="a28b2-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a28b2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a28b2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a28b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a28b2-111">0x00008234</span><span class="sxs-lookup"><span data-stu-id="a28b2-111">0x00008234</span></span>  <br/> |
|<span data-ttu-id="a28b2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a28b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="a28b2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a28b2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a28b2-114">領域:</span><span class="sxs-lookup"><span data-stu-id="a28b2-114">Area:</span></span>  <br/> |<span data-ttu-id="a28b2-115">予定表</span><span class="sxs-lookup"><span data-stu-id="a28b2-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a28b2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a28b2-116">Remarks</span></span>

<span data-ttu-id="a28b2-117">このプロパティは、 **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) のプロパティ内のデータによって表されるタイム ゾーンのユーザーが判読できる説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-117">This property specifies a human-readable description of the time zone that is represented by the data in the **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a28b2-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a28b2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a28b2-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a28b2-119">Protocol specifications</span></span>

<span data-ttu-id="a28b2-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a28b2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a28b2-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a28b2-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a28b2-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a28b2-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a28b2-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a28b2-124">Header files</span></span>

<span data-ttu-id="a28b2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a28b2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a28b2-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a28b2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a28b2-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a28b2-127">See also</span></span>



[<span data-ttu-id="a28b2-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a28b2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a28b2-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a28b2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a28b2-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a28b2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a28b2-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a28b2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

