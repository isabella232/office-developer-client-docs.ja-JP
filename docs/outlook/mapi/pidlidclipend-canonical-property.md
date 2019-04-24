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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349183"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="fef91-103">PidLidClipEnd 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fef91-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="fef91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fef91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fef91-105">単一インスタンスの予定表オブジェクトの、世界協定時刻 (UTC) でのイベントの終了日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="fef91-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fef91-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fef91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fef91-107">dispidclipend</span><span class="sxs-lookup"><span data-stu-id="fef91-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="fef91-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="fef91-108">Property set:</span></span>  <br/> |<span data-ttu-id="fef91-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fef91-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fef91-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fef91-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fef91-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="fef91-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="fef91-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fef91-112">Data type:</span></span>  <br/> |<span data-ttu-id="fef91-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fef91-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fef91-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fef91-114">Area:</span></span>  <br/> |<span data-ttu-id="fef91-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="fef91-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fef91-116">解説</span><span class="sxs-lookup"><span data-stu-id="fef91-116">Remarks</span></span>

<span data-ttu-id="fef91-117">単一インスタンスの calendar オブジェクトの場合は、イベントの終了日時を UTC で指定します。</span><span class="sxs-lookup"><span data-stu-id="fef91-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="fef91-118">定期的なアイテムの場合、このプロパティは定期的なアイテムの最後のインスタンスの日付の午前0時を指定します。この場合、定期的なアイテムの最後のインスタンスの日付は7月31日である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fef91-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="fef91-119">このプロパティの値には、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) の値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fef91-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fef91-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fef91-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fef91-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fef91-121">Protocol specifications</span></span>

<span data-ttu-id="fef91-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fef91-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fef91-123">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fef91-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fef91-124">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fef91-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fef91-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fef91-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fef91-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="fef91-126">Header files</span></span>

<span data-ttu-id="fef91-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fef91-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fef91-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fef91-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fef91-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fef91-129">See also</span></span>



[<span data-ttu-id="fef91-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fef91-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fef91-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fef91-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fef91-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fef91-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fef91-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fef91-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

