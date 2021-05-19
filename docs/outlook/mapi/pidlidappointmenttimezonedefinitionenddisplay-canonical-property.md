---
title: PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345382"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="131f0-103">PidLidAppointmentTimeZoneDefinitionEndDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="131f0-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="131f0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="131f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="131f0-105">単一インスタンスの予定または会議出席依頼の終了時刻が選択されている場合に使用されるタイム ゾーンの説明を格納する [、TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) 構造体の永続化された形式にマップするストリームを格納します。</span><span class="sxs-lookup"><span data-stu-id="131f0-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="131f0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="131f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="131f0-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="131f0-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="131f0-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="131f0-108">Property set:</span></span>  <br/> |<span data-ttu-id="131f0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="131f0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="131f0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="131f0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="131f0-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="131f0-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="131f0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="131f0-112">Data type:</span></span>  <br/> |<span data-ttu-id="131f0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="131f0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="131f0-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="131f0-114">Area:</span></span>  <br/> |<span data-ttu-id="131f0-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="131f0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="131f0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="131f0-116">Remarks</span></span>

<span data-ttu-id="131f0-117">Microsoft Office Outlook 2003 以前、およびコラボレーション データ オブジェクト (CDO) 1.2.1 に基づいており、Outlook または Microsoft Exchange Server の予定表更新ツールを実行していないソリューションでは、1 インスタンスの予定と会議出席依頼の開始時刻と終了時刻を協定世界時 (UTC) に保存します。</span><span class="sxs-lookup"><span data-stu-id="131f0-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="131f0-118">これらのクライアントには、予定または会議出席依頼が作成されるタイム ゾーンの情報は保存されません。</span><span class="sxs-lookup"><span data-stu-id="131f0-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="131f0-119">Microsoft Office Outlook 2007 以降の Microsoft Outlook のバージョンと、Outlook または Exchange Server カレンダー更新ツールを実行した CDO 1.2.1 に基づくソリューションでは **、dispidApptTZDefEndDisplay** を使用して終了時刻のタイム ゾーンを格納します。</span><span class="sxs-lookup"><span data-stu-id="131f0-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="131f0-120">**dispidApptTZDefEndDisplay** は、スケジュールされた元のタイム ゾーンの予定または会議を表示し、タイム ゾーンのルールが変更された場合に終了時刻を調整するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="131f0-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="131f0-121">このプロパティが見つからない場合は **、dispidApptTZDefStartDisplay** [(PidLidAppointmentTimeZoneDefinitionStartDisplay)](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)プロパティで指定されたタイム ゾーンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="131f0-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="131f0-122">**dispidApptTZDefStartDisplay** が見つからないか無効な場合、現在のローカル タイム ゾーンが想定されます。</span><span class="sxs-lookup"><span data-stu-id="131f0-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="131f0-123">**dispidApptTZDefEndDisplay** は表示目的でのみ使用され、定期的な展開では使用されません。</span><span class="sxs-lookup"><span data-stu-id="131f0-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="131f0-124">パーサーは **、dispidApptTZDefEndDisplay** から取得したストリームを読み取る場合、または **dispidApptTZDefEndDisplay** などのバイナリ プロパティへのコミットメントのために **TZDEFINITION** をストリームに保持するときに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="131f0-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="131f0-125">詳細については [、「TZDEFINITION をストリーム](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)に永続化してバイナリ プロパティにコミットする方法について」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="131f0-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="131f0-126">**dispidApptTZDefEndDisplay は\*\*\*\*、dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティのタイム ゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="131f0-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="131f0-127">**dispidApptTZDefEndDisplay** の形式、制約、および計算は **、dispidApptTZDefStartDisplay** プロパティで指定した形式と同じです。</span><span class="sxs-lookup"><span data-stu-id="131f0-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="131f0-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="131f0-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="131f0-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="131f0-129">Protocol specifications</span></span>

<span data-ttu-id="131f0-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="131f0-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="131f0-131">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="131f0-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="131f0-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="131f0-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="131f0-133">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="131f0-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="131f0-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="131f0-134">Header files</span></span>

<span data-ttu-id="131f0-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="131f0-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="131f0-136">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="131f0-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="131f0-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="131f0-137">See also</span></span>



[<span data-ttu-id="131f0-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="131f0-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="131f0-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="131f0-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="131f0-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="131f0-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="131f0-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="131f0-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

