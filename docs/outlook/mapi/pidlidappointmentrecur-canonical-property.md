---
title: PidLidAppointmentRecur 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331781"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="b4d54-103">PidLidAppointmentRecur 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4d54-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="b4d54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4d54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4d54-105">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で指定されている繰り返しパターンと範囲のいずれかを使用して、定期的な系列が発生する日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4d54-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b4d54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4d54-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="b4d54-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="b4d54-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="b4d54-108">Property set:</span></span>  <br/> |<span data-ttu-id="b4d54-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b4d54-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b4d54-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b4d54-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b4d54-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="b4d54-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="b4d54-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b4d54-112">Data type:</span></span>  <br/> |<span data-ttu-id="b4d54-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4d54-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4d54-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b4d54-114">Area:</span></span>  <br/> |<span data-ttu-id="b4d54-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="b4d54-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4d54-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b4d54-116">Remarks</span></span>

<span data-ttu-id="b4d54-117">このプロパティは [、[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で説明されている繰り返しパターンと範囲のいずれかを使用して、定期的な系列が発生する日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="b4d54-118">このプロパティの値には、変更された例外と削除された例外の両方に関する情報も含まれる。日付、件名、場所、および例外の他のいくつかのプロパティなどの情報。</span><span class="sxs-lookup"><span data-stu-id="b4d54-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="b4d54-119">定期的な予定表アイテムのこのプロパティのバイナリ データは **、AppointmentRecurrencePattern 構造体として格納** されます。</span><span class="sxs-lookup"><span data-stu-id="b4d54-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="b4d54-120">このプロパティは、単一インスタンスの予定表アイテムに存在していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b4d54-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="b4d54-121">繰り返しにはいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="b4d54-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="b4d54-122">複数のインスタンスが同じ日に開始される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4d54-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="b4d54-123">オカレンスは重なってはなりません。</span><span class="sxs-lookup"><span data-stu-id="b4d54-123">Occurrences must not overlap.</span></span> <span data-ttu-id="b4d54-124">具体的には、定期的な系列内のインスタンスの開始日を変更する例外は、前のインスタンスの終了および定期的な系列の次のインスタンスの開始後の日付に発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4d54-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="b4d54-125">定期的なシリーズの前または次のインスタンスが例外である場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="b4d54-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="b4d54-126">定期的な系列のスケジュールは、定期的なパターンと範囲によって決まります。</span><span class="sxs-lookup"><span data-stu-id="b4d54-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4d54-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b4d54-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4d54-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b4d54-128">Protocol specifications</span></span>

<span data-ttu-id="b4d54-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4d54-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4d54-130">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4d54-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4d54-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4d54-132">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="b4d54-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4d54-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4d54-134">メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4d54-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b4d54-135">Header files</span></span>

<span data-ttu-id="b4d54-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4d54-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4d54-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b4d54-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4d54-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4d54-138">See also</span></span>



[<span data-ttu-id="b4d54-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b4d54-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4d54-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b4d54-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4d54-141">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b4d54-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4d54-142">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b4d54-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

