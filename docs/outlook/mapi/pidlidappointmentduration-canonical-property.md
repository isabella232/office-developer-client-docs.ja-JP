---
title: PidLidAppointmentDuration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345396"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="47c68-103">PidLidAppointmentDuration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47c68-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="47c68-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c68-105">予定がスケジュールされている時間の長さを分単位で表します。</span><span class="sxs-lookup"><span data-stu-id="47c68-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47c68-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47c68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47c68-107">dispidapptduration</span><span class="sxs-lookup"><span data-stu-id="47c68-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="47c68-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="47c68-108">Property set:</span></span>  <br/> |<span data-ttu-id="47c68-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="47c68-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="47c68-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="47c68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="47c68-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="47c68-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="47c68-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47c68-112">Data type:</span></span>  <br/> |<span data-ttu-id="47c68-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47c68-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47c68-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="47c68-114">Area:</span></span>  <br/> |<span data-ttu-id="47c68-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="47c68-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47c68-116">解説</span><span class="sxs-lookup"><span data-stu-id="47c68-116">Remarks</span></span>

<span data-ttu-id="47c68-117">この値は、 **dispidapptstartwhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) と**dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) の各プロパティの値の間の分数である必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c68-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47c68-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47c68-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47c68-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47c68-119">Protocol specifications</span></span>

<span data-ttu-id="47c68-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47c68-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47c68-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47c68-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47c68-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47c68-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47c68-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c68-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47c68-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="47c68-124">Header files</span></span>

<span data-ttu-id="47c68-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47c68-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="47c68-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47c68-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47c68-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="47c68-127">See also</span></span>



[<span data-ttu-id="47c68-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="47c68-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47c68-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47c68-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47c68-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47c68-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47c68-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47c68-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

