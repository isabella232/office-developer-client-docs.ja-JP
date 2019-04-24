---
title: PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345354"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="3b113-103">PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b113-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="3b113-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b113-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b113-105">[TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造の永続形式にマップするストリームを格納します。このストリームには、定期的な予定または会議出席依頼の作成時に使用されるタイムゾーンの説明を格納します。</span><span class="sxs-lookup"><span data-stu-id="3b113-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b113-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3b113-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b113-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="3b113-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="3b113-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="3b113-108">Property set:</span></span>  <br/> |<span data-ttu-id="3b113-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="3b113-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="3b113-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="3b113-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b113-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="3b113-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="3b113-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3b113-112">Data type:</span></span>  <br/> |<span data-ttu-id="3b113-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b113-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b113-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="3b113-114">Area:</span></span>  <br/> |<span data-ttu-id="3b113-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="3b113-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b113-116">解説</span><span class="sxs-lookup"><span data-stu-id="3b113-116">Remarks</span></span>

<span data-ttu-id="3b113-117">microsoft Office outlook 2007 以降のバージョンの microsoft outlook と、outlook または Exchange Server 予定表更新ツールを実行したコラボレーションデータオブジェクト (CDO) 1.2.1 に基づくソリューションは、 **dispidApptTZDefRecur**と**を使用します。dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) プロパティを使用して、タイムゾーンのルールが変更された場合に、定期的な会議を調整する必要があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3b113-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="3b113-118">以前のクライアントでは、 **dispidTimeZoneStruct**プロパティを引き続き操作できるため、これらのプロパティを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="3b113-119">2つのプロパティが同期されているかどうかを検出するには、 **dispidTimeZoneStruct**に一致するルールの**wflags**メンバに TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="3b113-120">このフラグが設定されていない場合、または設定されていて、 **dispidTimeZoneStruct**プロパティのルールがマークされたルールと一致しない場合は、 **dispidApptTZDefRecur**プロパティを破棄して、代わりに**dispidTimeZoneStruct**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="3b113-121">**dispidApptTZDefRecur**プロパティと**dispidTimeZoneStruct**プロパティの両方を新しい定期的な会議に書き込む場合、または**dispidTimeZoneStruct**プロパティを使用する任意の選択肢を作成する場合は、タイムゾーンの現在の定義 (Windows レジストリに従う) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="3b113-122">パーサーは、 **dispidApptTZDefRecur**から取得されたストリームを読み取るとき、または**dispidApptTZDefRecur**などのバイナリプロパティへのコミットメントを得るために**TZDEFINITION**に保持されている場合は、注意を払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="3b113-123">詳細については、「データを[バイナリプロパティにコミットするためのストリームへの永続化 TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b113-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="3b113-124">**dispidApptTZDefRecur**は、定期的な会議の日付と時刻を協定世界時 (UTC) との間で変換する方法を示すタイムゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b113-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3b113-125">このプロパティが設定されていて、 **dispidTimeZoneStruct**によって表されるデータと矛盾するデータがある場合、クライアントは**dispidApptTZDefRecur**ではなく**dispidTimeZoneStruct**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b113-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="3b113-126">**dispidApptTZDefRecur**が設定されていない場合は、 **PidLidTimeZoneStruct**プロパティが代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b113-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="3b113-127">この BLOB のフィールドは、リトルエンディアンバイト順でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="3b113-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3b113-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3b113-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b113-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3b113-129">Protocol specifications</span></span>

<span data-ttu-id="3b113-130">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b113-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b113-131">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3b113-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b113-132">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b113-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b113-133">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b113-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b113-134">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3b113-134">Header files</span></span>

<span data-ttu-id="3b113-135">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b113-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b113-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3b113-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b113-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b113-137">See also</span></span>



[<span data-ttu-id="3b113-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3b113-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b113-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b113-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b113-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3b113-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b113-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3b113-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

