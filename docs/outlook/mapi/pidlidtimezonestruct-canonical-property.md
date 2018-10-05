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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401616"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="b80de-103">PidLidTimeZoneStruct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b80de-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="b80de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b80de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b80de-105">定期的な予定または会議出席依頼の開始と終了時に使用するタイム ゾーンを記述する[TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx)構造体の保存形式に対応するストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b80de-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b80de-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b80de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b80de-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="b80de-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="b80de-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b80de-108">Property set:</span></span>  <br/> |<span data-ttu-id="b80de-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b80de-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b80de-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b80de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b80de-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="b80de-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="b80de-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b80de-112">Data type:</span></span>  <br/> |<span data-ttu-id="b80de-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b80de-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b80de-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b80de-114">Area:</span></span>  <br/> |<span data-ttu-id="b80de-115">予定表</span><span class="sxs-lookup"><span data-stu-id="b80de-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b80de-116">備考</span><span class="sxs-lookup"><span data-stu-id="b80de-116">Remarks</span></span>

<span data-ttu-id="b80de-117">Microsoft Office Outlook 2003 では、以前のバージョンの Outlook、およびユーザーが Outlook または Exchange Server によって提供される予定表更新ツールを実行していないのでは、コラボレーション データ オブジェクト (CDO) 1.21 をベースとするアプリケーションは、開始時刻と終了時刻を格納します。予定かの相対的な時間として会議出席依頼を定期的な予定と**dispidTimeZoneStruct**で、予定または会議出席依頼を作成する場所のタイム ゾーンを格納します。</span><span class="sxs-lookup"><span data-stu-id="b80de-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="b80de-118">ただし、このスキームは、時間の経過と共にタイム ゾーン規則を変更できるように、ユーザーは、ルールが変更され、不適切なタイミングで発生する前にスケジュールするにいくつかの予定および会議の結果を無視します。</span><span class="sxs-lookup"><span data-stu-id="b80de-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="b80de-119">ユーザーと管理者が Windows Vista を実行していない、またはされていて、自動更新を有効にしないのは、このような予定と会議出席依頼の時刻を調整するには、Outlook または Exchange Server によって提供されるツールを再配置する予定表を使用してください。</span><span class="sxs-lookup"><span data-stu-id="b80de-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="b80de-120">これらの再配置ツールの予定表と予定表を再配置するための Api の詳細については、[夏時間から標準時のプログラムを使用して予定表を再配置の詳細](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b80de-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="b80de-121">ストリームに**TZREG**構造体を保持する場合、 **dispidTimeZoneStruct**、またはを取得するストリームを解析するとき**dispidTimeZoneStruct**のバイナリ プロパティをコミットするのには次のリトル エンディアンの形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="b80de-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="b80de-122">このプロパティでは、タイム ゾーン情報を指定するのには定期的に設定され、現地時刻と世界協定時刻 (UTC) との間の時間フィールドに変換する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="b80de-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b80de-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b80de-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b80de-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b80de-124">Protocol specifications</span></span>

<span data-ttu-id="b80de-125">[[MS OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b80de-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b80de-126">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b80de-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b80de-127">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b80de-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b80de-128">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b80de-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b80de-129">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b80de-129">Header files</span></span>

<span data-ttu-id="b80de-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b80de-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b80de-131">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b80de-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b80de-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="b80de-132">See also</span></span>



[<span data-ttu-id="b80de-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b80de-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b80de-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b80de-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b80de-135">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b80de-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b80de-136">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b80de-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

