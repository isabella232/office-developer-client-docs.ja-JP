---
title: PidLidClipEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349183"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="a363d-103">PidLidClipEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a363d-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="a363d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a363d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a363d-105">単一インスタンスカレンダー オブジェクトの協定世界時 (UTC) でイベントの終了日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="a363d-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a363d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a363d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a363d-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="a363d-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="a363d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="a363d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a363d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a363d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a363d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a363d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a363d-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="a363d-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="a363d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a363d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a363d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a363d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a363d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a363d-114">Area:</span></span>  <br/> |<span data-ttu-id="a363d-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="a363d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a363d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="a363d-116">Remarks</span></span>

<span data-ttu-id="a363d-117">単一インスタンスの予定表オブジェクトの場合、イベントの終了日時を UTC で指定します。</span><span class="sxs-lookup"><span data-stu-id="a363d-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="a363d-118">定期的な系列の場合、このプロパティは、定期的な系列の最後のインスタンスの日付の午前 0 時を UTC で指定します。この場合、値は 8 月 4500 年 8 月 31 日午後 11 時 59 分である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a363d-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="a363d-119">このプロパティの値は **、dispidApptEndWhole** ([PidLidAppointmentEndWhole) の値に設定する必要があります](pidlidappointmentendwhole-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="a363d-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a363d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a363d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a363d-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a363d-121">Protocol specifications</span></span>

<span data-ttu-id="a363d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a363d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a363d-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="a363d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a363d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a363d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a363d-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a363d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a363d-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a363d-126">Header files</span></span>

<span data-ttu-id="a363d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a363d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a363d-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a363d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a363d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="a363d-129">See also</span></span>



[<span data-ttu-id="a363d-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a363d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a363d-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a363d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a363d-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a363d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a363d-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a363d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

