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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346376"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="744fe-103">PidLidTimeZoneStruct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="744fe-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="744fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="744fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="744fe-105">[TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx)構造の永続形式にマップするストリームを格納します。これは、定期的な予定または会議出席依頼の開始時刻と終了時刻に使用されるタイムゾーンを表します。</span><span class="sxs-lookup"><span data-stu-id="744fe-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="744fe-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="744fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="744fe-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="744fe-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="744fe-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="744fe-108">Property set:</span></span>  <br/> |<span data-ttu-id="744fe-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="744fe-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="744fe-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="744fe-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="744fe-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="744fe-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="744fe-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="744fe-112">Data type:</span></span>  <br/> |<span data-ttu-id="744fe-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="744fe-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="744fe-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="744fe-114">Area:</span></span>  <br/> |<span data-ttu-id="744fe-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="744fe-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="744fe-116">解説</span><span class="sxs-lookup"><span data-stu-id="744fe-116">Remarks</span></span>

<span data-ttu-id="744fe-117">Microsoft Office outlook 2003、以前のバージョンの outlook、およびユーザーが outlook または Exchange Server ストアが提供する予定表更新ツールを実行していないグループ作業データオブジェクト (CDO) 1.21 に基づくアプリケーション相対時間としての定期的な予定または会議出席依頼。 **dispidTimeZoneStruct**で予定または会議出席依頼が作成されたタイムゾーンを保存します。</span><span class="sxs-lookup"><span data-stu-id="744fe-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="744fe-118">ただし、このスキームでは時間が経過すると、タイムゾーンの規則が変化し、ルールが変更される前にユーザーがスケジュールを設定して、誤った時間に発生する予定と会議を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="744fe-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="744fe-119">Windows Vista を実行していない、または自動更新が有効になっていないユーザーと管理者は、Outlook または Exchange Server によって提供される予定表の再配置ツールを使用して、そのような予定や会議出席依頼の時刻を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="744fe-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="744fe-120">カレンダーを再配置するための、これらの予定表の再配置ツールと api の詳細については、「[夏時間のプログラムを使用して予定表](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)を再配置する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="744fe-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="744fe-121">**dispidTimeZoneStruct**から取得したストリームを解析するとき、または**TZREG**構造体を**dispidTimeZoneStruct** binary プロパティにコミットするストリームに永続化するときは、次のリトルエンディアン形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="744fe-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="744fe-122">このプロパティは、タイムゾーン情報を指定するために定期的なアイテムに対して設定され、時刻フィールドを現地時刻と協定世界時 (UTC) の間で変換する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="744fe-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="744fe-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="744fe-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="744fe-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="744fe-124">Protocol specifications</span></span>

<span data-ttu-id="744fe-125">[[OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744fe-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744fe-126">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="744fe-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="744fe-127">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744fe-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744fe-128">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="744fe-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="744fe-129">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="744fe-129">Header files</span></span>

<span data-ttu-id="744fe-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="744fe-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="744fe-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="744fe-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="744fe-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="744fe-132">See also</span></span>



[<span data-ttu-id="744fe-133">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="744fe-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="744fe-134">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="744fe-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="744fe-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="744fe-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="744fe-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="744fe-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

