---
title: PidLidAppointmentTimeZoneDefinitionStartDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345018"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="a1653-103">PidLidAppointmentTimeZoneDefinitionStartDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a1653-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="a1653-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1653-105">[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造の永続形式にマップするストリームを格納します。これは、単一インスタンスの予定または会議出席依頼の開始時刻が選択されたときに使用されるタイムゾーンの説明を格納します。</span><span class="sxs-lookup"><span data-stu-id="a1653-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1653-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a1653-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1653-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="a1653-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="a1653-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a1653-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1653-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a1653-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a1653-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a1653-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1653-111">0x0000825e</span><span class="sxs-lookup"><span data-stu-id="a1653-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="a1653-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a1653-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1653-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1653-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1653-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="a1653-114">Area:</span></span>  <br/> |<span data-ttu-id="a1653-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="a1653-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1653-116">解説</span><span class="sxs-lookup"><span data-stu-id="a1653-116">Remarks</span></span>

<span data-ttu-id="a1653-117">microsoft Office Outlook 2003 またはそれ以前のバージョンで、コラボレーションデータオブジェクト (CDO) 1.2.1 に基づいていて、Outlook または Microsoft Exchange Server 用の予定表更新ツールを実行していない場合は、単一インスタンスの開始時刻と終了時刻を格納します。協定世界時 (UTC) の予定および会議出席依頼。</span><span class="sxs-lookup"><span data-stu-id="a1653-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a1653-118">これらのクライアントには、予定または会議出席依頼が作成されたタイムゾーンの情報は格納されません。</span><span class="sxs-lookup"><span data-stu-id="a1653-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="a1653-119">Microsoft Office outlook 2007 以降のバージョンの outlook と、outlook または Exchange Server 予定表更新ツールを実行した CDO 1.2.1 に基づくソリューションこのプロパティを使用して、開始時刻のタイムゾーンを保存します。</span><span class="sxs-lookup"><span data-stu-id="a1653-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="a1653-120">**dispidApptTZDefStartDisplay**プロパティは、スケジュールされた元のタイムゾーンで予定または会議を表示します。</span><span class="sxs-lookup"><span data-stu-id="a1653-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="a1653-121">タイムゾーンのルールが変更された場合に、開始時刻を調整するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a1653-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="a1653-122">このプロパティが存在しない場合は、現在のローカルタイムゾーンが想定されます。</span><span class="sxs-lookup"><span data-stu-id="a1653-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="a1653-123">このプロパティは表示のみを目的として使用され、定期的な展開では使用されません。</span><span class="sxs-lookup"><span data-stu-id="a1653-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="a1653-124">パーサーは、このプロパティから取得されたストリームを読み取るとき、または**dispidApptTZDefStartDisplay**などのバイナリプロパティへのコミットメントを**TZDEFINITION**に保持するときに、注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1653-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="a1653-125">詳細については、「データを[バイナリプロパティにコミットするためのストリームへの永続化 TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1653-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="a1653-126">このプロパティは、 **dispidapptstartwhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) プロパティのタイムゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a1653-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="a1653-127">**dispidApptTZDefStartDisplay**の値は、表示を目的として、開始日と時刻を UTC からローカルタイムゾーンに変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1653-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="a1653-128">このプロパティで指定された**TZRULE**ごとに、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定してはなりません。</span><span class="sxs-lookup"><span data-stu-id="a1653-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="a1653-129">たとえば、 **TZRULE**が有効なルールである場合、フィールドの値**TZRULE**は "0x0002" である必要があります。それ以外の場合は、"0x0000" である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1653-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1653-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a1653-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1653-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a1653-131">Protocol specifications</span></span>

<span data-ttu-id="a1653-132">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1653-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1653-133">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a1653-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="a1653-134">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1653-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1653-135">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a1653-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1653-136">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a1653-136">Header files</span></span>

<span data-ttu-id="a1653-137">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1653-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1653-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a1653-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1653-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1653-139">See also</span></span>



[<span data-ttu-id="a1653-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a1653-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1653-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a1653-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1653-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a1653-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1653-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a1653-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

