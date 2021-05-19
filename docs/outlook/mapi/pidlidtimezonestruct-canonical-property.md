---
title: PidLidTimeZoneStruct 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346376"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="d4b1b-103">PidLidTimeZoneStruct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4b1b-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="d4b1b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4b1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4b1b-105">定期的な予定または会議出席依頼の開始時刻と終了時刻に使用するタイム ゾーンを示す [、TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) 構造の永続化された形式にマップするストリームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4b1b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d4b1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4b1b-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="d4b1b-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="d4b1b-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="d4b1b-108">Property set:</span></span>  <br/> |<span data-ttu-id="d4b1b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d4b1b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d4b1b-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d4b1b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4b1b-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="d4b1b-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="d4b1b-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d4b1b-112">Data type:</span></span>  <br/> |<span data-ttu-id="d4b1b-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4b1b-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4b1b-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="d4b1b-114">Area:</span></span>  <br/> |<span data-ttu-id="d4b1b-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="d4b1b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b1b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="d4b1b-116">Remarks</span></span>

<span data-ttu-id="d4b1b-117">Microsoft Office Outlook 2003、以前のバージョンの Outlook、およびユーザーが Outlook または Exchange Server が提供する予定表更新ツールを実行していないコラボレーション データ オブジェクト (CDO) 1.21 に基づくアプリケーションは、定期的な予定または会議出席依頼の開始時刻と終了時刻を相対時間として格納し、予定または会議出席依頼が **dispidTimeZoneStruct** で作成されるタイム ゾーンを格納します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="d4b1b-118">ただし、このスキームでは、時間がたつ間にタイム ゾーン ルールが変更され、ルールが変更される前にスケジュールされた予定や会議が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="d4b1b-119">Windows Vista を実行していない、または自動更新を有効にしていないユーザーと管理者は、Outlook または Exchange Server によって提供される予定表の再調整ツールを使用して、そのような予定や会議出席依頼の時間を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="d4b1b-120">予定表をリベースするこれらの予定表の再調整ツールと API の詳細については、「夏時間に合わせてプログラムで予定表を再調整する方法について[」を参照してください](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="d4b1b-121">**dispidTimeZoneStruct** から取得したストリームを解析する場合、または **TZREG** 構造体をストリームに永続化して **dispidTimeZoneStruct** バイナリ プロパティにコミットする場合は、次のリトルエンディアン形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="d4b1b-122">このプロパティは、タイム ゾーン情報を指定するために定期的な系列に設定され、時刻フィールドを現地時間と協定世界時 (UTC) の間で変換する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4b1b-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d4b1b-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4b1b-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d4b1b-124">Protocol specifications</span></span>

<span data-ttu-id="d4b1b-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4b1b-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4b1b-126">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4b1b-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4b1b-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4b1b-128">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4b1b-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d4b1b-129">Header files</span></span>

<span data-ttu-id="d4b1b-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4b1b-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4b1b-131">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4b1b-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4b1b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4b1b-132">See also</span></span>



[<span data-ttu-id="d4b1b-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d4b1b-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4b1b-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d4b1b-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4b1b-135">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d4b1b-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4b1b-136">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d4b1b-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

