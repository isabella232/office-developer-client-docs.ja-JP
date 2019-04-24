---
title: PidLidIntendedBusyStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIntendedBusyStatus
api_type:
- COM
ms.assetid: 84221dd3-de71-4c10-abd7-9f15aefd02ed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f64ff019212065efd651fd2562c48519b0c7c2d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332971"
---
# <a name="pidlidintendedbusystatus-canonical-property"></a><span data-ttu-id="1915e-103">PidLidIntendedBusyStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1915e-103">PidLidIntendedBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1915e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1915e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1915e-105">会議出席依頼または会議の更新を送信したときに開催者の予定表にある会議の**dispidBusyStatus** ([PidLidBusyStatus](pidlidbusystatus-canonical-property.md)) プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1915e-105">Specifies the value of the **dispidBusyStatus** ([PidLidBusyStatus](pidlidbusystatus-canonical-property.md)) property on the meeting in the organizer's calendar when the meeting request or meeting update was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1915e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1915e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1915e-107">dispidIntendedBusyStatus</span><span class="sxs-lookup"><span data-stu-id="1915e-107">dispidIntendedBusyStatus</span></span>  <br/> |
|<span data-ttu-id="1915e-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1915e-108">Property set:</span></span>  <br/> |<span data-ttu-id="1915e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1915e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1915e-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1915e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1915e-111">0x00008224</span><span class="sxs-lookup"><span data-stu-id="1915e-111">0x00008224</span></span>  <br/> |
|<span data-ttu-id="1915e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1915e-112">Data type:</span></span>  <br/> |<span data-ttu-id="1915e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1915e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1915e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1915e-114">Area:</span></span>  <br/> |<span data-ttu-id="1915e-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="1915e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1915e-116">解説</span><span class="sxs-lookup"><span data-stu-id="1915e-116">Remarks</span></span>

<span data-ttu-id="1915e-117">このプロパティに使用できる値は、 **dispidBusyStatus**プロパティの値と同じです。</span><span class="sxs-lookup"><span data-stu-id="1915e-117">The allowable values of this property are the same as those for the property **dispidBusyStatus**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1915e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1915e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1915e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1915e-119">Protocol specifications</span></span>

<span data-ttu-id="1915e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1915e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1915e-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1915e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1915e-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1915e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1915e-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1915e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1915e-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1915e-124">Header files</span></span>

<span data-ttu-id="1915e-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1915e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1915e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1915e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1915e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1915e-127">See also</span></span>



[<span data-ttu-id="1915e-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1915e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1915e-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1915e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1915e-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1915e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1915e-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1915e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

