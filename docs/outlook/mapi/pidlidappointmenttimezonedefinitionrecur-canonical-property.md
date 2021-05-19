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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345354"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="fce9d-103">PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fce9d-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="fce9d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce9d-105">定期的な予定または会議出席依頼の作成時に使用されるタイム ゾーンの説明を格納する [、TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) 構造体の永続化された形式にマップするストリームを格納します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fce9d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fce9d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fce9d-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="fce9d-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="fce9d-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="fce9d-108">Property set:</span></span>  <br/> |<span data-ttu-id="fce9d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fce9d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fce9d-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fce9d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fce9d-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="fce9d-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="fce9d-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fce9d-112">Data type:</span></span>  <br/> |<span data-ttu-id="fce9d-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fce9d-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fce9d-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="fce9d-114">Area:</span></span>  <br/> |<span data-ttu-id="fce9d-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="fce9d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fce9d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="fce9d-116">Remarks</span></span>

<span data-ttu-id="fce9d-117">Microsoft Office Outlook 2007 以降の Microsoft Outlook のバージョンと、Outlook または Exchange Server カレンダー更新ツールを実行したコラボレーション データ オブジェクト (CDO) 1.2.1 に基づくソリューションでは **、dispidApptTZDefRecur** プロパティと **dispidTimeZoneStruct** [(PidLidTimeZoneStruct)](pidlidtimezonestruct-canonical-property.md)プロパティを使用して、タイム ゾーンのルールが変更された場合に定期的な会議を調整するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="fce9d-118">古いクライアントが **dispidTimeZoneStruct** プロパティを操作する場合もありますので、これらのプロパティを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="fce9d-119">2 つのプロパティが同期されているかどうかを検出するには **、dispidTimeZoneStruct** に一致するルールの **wFlags** メンバーに、TZRULE_FLAG_RECUR_CURRENT_TZREGフラグが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="fce9d-120">このフラグが設定されていない場合、または設定され **、dispidTimeZoneStruct** プロパティのルールがマークされたルールと一致しない場合は **、dispidApptTZDefRecur** プロパティを破棄し、代わりに **dispidTimeZoneStruct** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="fce9d-121">**dispidApptTZDefRecur** プロパティと **dispidTimeZoneStruct** プロパティの両方を新しい定期的な会議に書き込む場合、または **dispidTimeZoneStruct** プロパティを使用する任意の選択を行う場合は、(Windows レジストリに従って) タイム ゾーンの現在の定義を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="fce9d-122">パーサーは **、dispidApptTZDefRecur** から取得されたストリームを読み取る場合、または **TZDEFINITION** をストリームに保持して **、dispidApptTZDefRecur** などのバイナリ プロパティへのコミットメントを行う場合には注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="fce9d-123">詳細については [、「TZDEFINITION をストリーム](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)に永続化してバイナリ プロパティにコミットする方法について」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fce9d-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="fce9d-124">**dispidApptTZDefRecur** は、定期的なシリーズの会議の日時を協定世界時 (UTC) との間で変換する方法を説明するタイム ゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fce9d-125">このプロパティが設定されているが **、dispidTimeZoneStruct** で表されるデータと矛盾するデータがある場合、クライアントは **dispidApptTZDefRecur** ではなく **dispidTimeZoneStruct** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fce9d-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="fce9d-126">**dispidApptTZDefRecur** が設定されていない場合は **、PidLidTimeZoneStruct** プロパティが代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fce9d-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="fce9d-127">この BLOB のフィールドは、リトル エンドのバイト順でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="fce9d-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fce9d-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fce9d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fce9d-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fce9d-129">Protocol specifications</span></span>

<span data-ttu-id="fce9d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fce9d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fce9d-131">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fce9d-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fce9d-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fce9d-133">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fce9d-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fce9d-134">Header files</span></span>

<span data-ttu-id="fce9d-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fce9d-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="fce9d-136">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fce9d-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fce9d-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="fce9d-137">See also</span></span>



[<span data-ttu-id="fce9d-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fce9d-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fce9d-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fce9d-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fce9d-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fce9d-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fce9d-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fce9d-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

