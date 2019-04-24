---
title: PidLidClipStart 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipStart
api_type:
- COM
ms.assetid: d348988d-a84e-4318-8d48-62e4982ebaf1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4a466b31b5411b1c0467896c031c6560d6c5c880
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349246"
---
# <a name="pidlidclipstart-canonical-property"></a><span data-ttu-id="66b02-103">PidLidClipStart 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66b02-103">PidLidClipStart Canonical Property</span></span>

  
  
<span data-ttu-id="66b02-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66b02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66b02-105">単一インスタンスの予定表オブジェクトのイベントの開始日時を協定世界時 (utc) で指定し、定期的なアイテムの最初のインスタンスの日付の午前0時を utc で指定します。</span><span class="sxs-lookup"><span data-stu-id="66b02-105">Specifies the start date and time of the event in Coordinated Universal Times (UTC) for single instance calendar objects, and specifies midnight on the date of the first instance in UTC for a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66b02-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="66b02-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66b02-107">dispidclipstart</span><span class="sxs-lookup"><span data-stu-id="66b02-107">dispidClipStart</span></span>  <br/> |
|<span data-ttu-id="66b02-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="66b02-108">Property set:</span></span>  <br/> |<span data-ttu-id="66b02-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="66b02-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="66b02-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="66b02-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="66b02-111">0x00008235</span><span class="sxs-lookup"><span data-stu-id="66b02-111">0x00008235</span></span>  <br/> |
|<span data-ttu-id="66b02-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="66b02-112">Data type:</span></span>  <br/> |<span data-ttu-id="66b02-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="66b02-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="66b02-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="66b02-114">Area:</span></span>  <br/> |<span data-ttu-id="66b02-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="66b02-115">Calendar</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="66b02-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="66b02-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66b02-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="66b02-117">Protocol specifications</span></span>

<span data-ttu-id="66b02-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66b02-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66b02-119">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="66b02-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66b02-120">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66b02-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66b02-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="66b02-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66b02-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="66b02-122">Header files</span></span>

<span data-ttu-id="66b02-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66b02-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="66b02-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="66b02-124">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66b02-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="66b02-125">See also</span></span>



[<span data-ttu-id="66b02-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="66b02-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66b02-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="66b02-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66b02-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66b02-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66b02-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="66b02-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

