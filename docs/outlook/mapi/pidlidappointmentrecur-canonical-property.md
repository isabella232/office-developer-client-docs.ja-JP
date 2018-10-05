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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393370"
---
# <a name="pidlidappointmentrecur-canonical-property"></a><span data-ttu-id="e51ce-103">PidLidAppointmentRecur 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e51ce-103">PidLidAppointmentRecur Canonical Property</span></span>

  
  
<span data-ttu-id="e51ce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e51ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e51ce-105">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で指定されている範囲、定期的なパターンのいずれかを使用して定期的な系列が発生したときの日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-105">Specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges that are specified in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e51ce-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e51ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e51ce-107">dispidApptRecur</span><span class="sxs-lookup"><span data-stu-id="e51ce-107">dispidApptRecur</span></span>  <br/> |
|<span data-ttu-id="e51ce-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="e51ce-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e51ce-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e51ce-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e51ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e51ce-111">0x00008216</span><span class="sxs-lookup"><span data-stu-id="e51ce-111">0x00008216</span></span>  <br/> |
|<span data-ttu-id="e51ce-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e51ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="e51ce-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e51ce-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e51ce-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e51ce-114">Area:</span></span>  <br/> |<span data-ttu-id="e51ce-115">予定表</span><span class="sxs-lookup"><span data-stu-id="e51ce-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e51ce-116">備考</span><span class="sxs-lookup"><span data-stu-id="e51ce-116">Remarks</span></span>

<span data-ttu-id="e51ce-117">このプロパティは、一連の定期的な定期的なパターンのいずれかで発生して範囲の詳細な[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-117">This property specifies the dates and times when a recurring series occurs by using one of the recurrence patterns and ranges detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).</span></span> <span data-ttu-id="e51ce-118">このプロパティの値は、変更と削除の両方の例外に関する情報も含まれています。日付、件名、場所、およびその他のいくつかの例外のプロパティなどの情報。</span><span class="sxs-lookup"><span data-stu-id="e51ce-118">The value of this property also contains information about both modified and deleted exceptions; information such as dates, subject, location, and several other properties of exceptions.</span></span> <span data-ttu-id="e51ce-119">定期的な予定表アイテムのこのプロパティのバイナリ データは、 **AppointmentRecurrencePattern**構造体として格納されます。</span><span class="sxs-lookup"><span data-stu-id="e51ce-119">The binary data in this property for recurring calendar items is stored as the **AppointmentRecurrencePattern** structure.</span></span> <span data-ttu-id="e51ce-120">このプロパティは、単一インスタンスの予定表アイテムに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e51ce-120">This property must not exist on single instance calendar items.</span></span> 
  
<span data-ttu-id="e51ce-121">定期的なアイテムをいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="e51ce-121">There are some limitations to recurrences:</span></span>
  
- <span data-ttu-id="e51ce-122">複数のインスタンスは、同じ日に開始する必要がありますできません。</span><span class="sxs-lookup"><span data-stu-id="e51ce-122">Multiple instances must not start on the same day.</span></span>
    
- <span data-ttu-id="e51ce-123">出現回数が重複する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e51ce-123">Occurrences must not overlap.</span></span> <span data-ttu-id="e51ce-124">具体的には、以前のインスタンスの末尾と次の定期的な系列のインスタンスの開始後の日付に定期的な系列のインスタンスの開始日を変更するの例外が発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e51ce-124">Specifically, an exception that modifies the start date of an instance in the recurring series must occur on a date that is after the end of the prior instance and the start of the next instance in the recurring series.</span></span> <span data-ttu-id="e51ce-125">定期的な系列の前または次のインスタンスが例外の場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="e51ce-125">The same is true if the prior or next instances in the recurring series are exceptions.</span></span>
    
<span data-ttu-id="e51ce-126">一連の定期的なスケジュールは、その定期的なパターンと範囲が決定されます。</span><span class="sxs-lookup"><span data-stu-id="e51ce-126">The schedule of a recurring series is determined by its recurrence pattern and range.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e51ce-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e51ce-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e51ce-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e51ce-128">Protocol specifications</span></span>

<span data-ttu-id="e51ce-129">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e51ce-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e51ce-130">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e51ce-131">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e51ce-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e51ce-132">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e51ce-133">[[MS OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e51ce-133">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e51ce-134">電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-134">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e51ce-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e51ce-135">Header files</span></span>

<span data-ttu-id="e51ce-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e51ce-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="e51ce-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e51ce-137">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e51ce-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="e51ce-138">See also</span></span>



[<span data-ttu-id="e51ce-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e51ce-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e51ce-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e51ce-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e51ce-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e51ce-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e51ce-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e51ce-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

