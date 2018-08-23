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
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801837"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="024a0-103">PidLidAppointmentTimeZoneDefinitionRecur 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="024a0-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="024a0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="024a0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="024a0-105">定期的な予定または会議出席依頼の作成時に使用されるタイム ゾーンの説明を格納する[TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx)構造体の保存形式に対応するストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="024a0-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="024a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="024a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="024a0-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="024a0-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="024a0-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="024a0-108">Property set:</span></span>  <br/> |<span data-ttu-id="024a0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="024a0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="024a0-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="024a0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="024a0-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="024a0-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="024a0-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="024a0-112">Data type:</span></span>  <br/> |<span data-ttu-id="024a0-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="024a0-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="024a0-114">領域:</span><span class="sxs-lookup"><span data-stu-id="024a0-114">Area:</span></span>  <br/> |<span data-ttu-id="024a0-115">予定表</span><span class="sxs-lookup"><span data-stu-id="024a0-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="024a0-116">注釈</span><span class="sxs-lookup"><span data-stu-id="024a0-116">Remarks</span></span>

<span data-ttu-id="024a0-117">Outlook または Exchange Server の予定表を実行している Microsoft Outlook を Microsoft Office Outlook 2007 では、ソリューションでは、コラボレーション データ オブジェクト (CDO) 1.2.1 以降のバージョンは、ツールの使用方法**dispidApptTZDefRecur**と**を更新します。dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) のプロパティをタイム ゾーンの規則を変更する場合に、定期的な会議を調整する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="024a0-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="024a0-118">古いクライアントが、 **dispidTimeZoneStruct**プロパティを操作するため、これらのプロパティを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="024a0-119">2 つのプロパティーを同期するかどうかを検出するには、 **dispidTimeZoneStruct**に一致するルールの**wFlags**メンバーに、TZRULE_FLAG_RECUR_CURRENT_TZREG フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="024a0-120">このフラグは設定されていない、または設定されている、 **dispidTimeZoneStruct**プロパティの規則は、マークされたルールと一致しない場合、 **dispidApptTZDefRecur**プロパティを破棄する必要があり、 **dispidTimeZoneStruct**を代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="024a0-121">新しい定期的な会議、または、 **dispidTimeZoneStruct**プロパティ、タイム ゾーン (の現在の定義を使用して任意の選択を行うと、 **dispidApptTZDefRecur**と**dispidTimeZoneStruct**の両方のプロパティを記述する場合Windows レジストリ) に従って使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="024a0-122">パーサーは、 **dispidApptTZDefRecur**から取得するストリームを読み取るとき、または**dispidApptTZDefRecur**などのバイナリのプロパティへの取り組みのためのストリームに**TZDEFINITION**が引き続き発生する場合注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="024a0-123">詳細については、[バイナリのプロパティをコミットするためのストリームに永続化する TZDEFINITION](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="024a0-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="024a0-124">**dispidApptTZDefRecur**を世界協定時刻 (UTC) から、会議の日付と時刻、定期的に変換する方法を説明するタイム ゾーン情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="024a0-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="024a0-125">このプロパティが**dispidTimeZoneStruct**で表されるデータと一致しないデータがある場合は、クライアントは、 **dispidApptTZDefRecur**の代わりに**dispidTimeZoneStruct**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="024a0-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="024a0-126">**DispidApptTZDefRecur**が設定されていない場合、 **PidLidTimeZoneStruct**プロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="024a0-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="024a0-127">この BLOB 内のフィールドは、リトル エンディアン バイト順でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="024a0-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="024a0-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="024a0-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="024a0-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="024a0-129">Protocol specifications</span></span>

<span data-ttu-id="024a0-130">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="024a0-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="024a0-131">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="024a0-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="024a0-132">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="024a0-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="024a0-133">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="024a0-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="024a0-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="024a0-134">Header files</span></span>

<span data-ttu-id="024a0-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="024a0-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="024a0-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="024a0-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="024a0-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="024a0-137">See also</span></span>



[<span data-ttu-id="024a0-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="024a0-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="024a0-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="024a0-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="024a0-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="024a0-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="024a0-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="024a0-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

