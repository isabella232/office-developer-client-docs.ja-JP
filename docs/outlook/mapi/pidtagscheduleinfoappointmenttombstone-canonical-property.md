---
title: PidTagScheduleInfoAppointmentTombstone 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e554a496dd1869dd7c07b315d92a136676e05006
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590044"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="8207d-103">PidTagScheduleInfoAppointmentTombstone 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8207d-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="8207d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8207d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8207d-105">辞退された会議を表すデータ ブロックのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8207d-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8207d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8207d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8207d-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="8207d-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="8207d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8207d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8207d-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="8207d-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="8207d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8207d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8207d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8207d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8207d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="8207d-112">Area:</span></span>  <br/> |<span data-ttu-id="8207d-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="8207d-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8207d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8207d-114">Remarks</span></span>

<span data-ttu-id="8207d-115">データ ブロックは、32 ビットの値として定義されているヘッダーで始まります。</span><span class="sxs-lookup"><span data-stu-id="8207d-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="8207d-116">**値**</span><span class="sxs-lookup"><span data-stu-id="8207d-116">**Value**</span></span>|<span data-ttu-id="8207d-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="8207d-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8207d-118">Identifier</span><span class="sxs-lookup"><span data-stu-id="8207d-118">Identifier</span></span>  <br/> |<span data-ttu-id="8207d-119">このフィールドには、0xBEDEAFCD の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8207d-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="8207d-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="8207d-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="8207d-121">0x00000014 の値がこのフィールドに必要です。</span><span class="sxs-lookup"><span data-stu-id="8207d-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="8207d-122">バージョン</span><span class="sxs-lookup"><span data-stu-id="8207d-122">Version</span></span>  <br/> |<span data-ttu-id="8207d-123">このフィールドには、値 3 が必要です。</span><span class="sxs-lookup"><span data-stu-id="8207d-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="8207d-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="8207d-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="8207d-125">以下のレコードの数。</span><span class="sxs-lookup"><span data-stu-id="8207d-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="8207d-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="8207d-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="8207d-127">0x00000014 の値がこのフィールドに必要です。</span><span class="sxs-lookup"><span data-stu-id="8207d-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="8207d-128">ヘッダーには、32 ビットの値として定義されているの**RecordsCount**エントリが続きます。</span><span class="sxs-lookup"><span data-stu-id="8207d-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="8207d-129">**値**</span><span class="sxs-lookup"><span data-stu-id="8207d-129">**Value**</span></span>|<span data-ttu-id="8207d-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="8207d-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8207d-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="8207d-131">StartTime</span></span>  <br/> |<span data-ttu-id="8207d-132">1601 年 1 月 1 日午前 0: 00 UTC 以降の分で、会議オブジェクトの開始時刻。</span><span class="sxs-lookup"><span data-stu-id="8207d-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="8207d-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="8207d-133">EndTime</span></span>  <br/> |<span data-ttu-id="8207d-134">1601 年 1 月 1 日午前 0: 00 UTC からの分単位の会議オブジェクトの終了時間です。</span><span class="sxs-lookup"><span data-stu-id="8207d-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="8207d-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="8207d-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="8207d-136">GlobalObjectId フィールドのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="8207d-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="8207d-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="8207d-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="8207d-138">会議のレコードの**LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティの値を表します。</span><span class="sxs-lookup"><span data-stu-id="8207d-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="8207d-139">UserName</span><span class="sxs-lookup"><span data-stu-id="8207d-139">UserName</span></span>  <br/> |<span data-ttu-id="8207d-140">最初の 2 バイトは、後に続く PT_STRING8 文字列の長さです。</span><span class="sxs-lookup"><span data-stu-id="8207d-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8207d-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8207d-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8207d-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8207d-142">Protocol specifications</span></span>

<span data-ttu-id="8207d-143">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8207d-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8207d-144">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8207d-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8207d-145">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8207d-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8207d-146">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8207d-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8207d-147">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8207d-147">Header files</span></span>

<span data-ttu-id="8207d-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8207d-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="8207d-149">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8207d-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="8207d-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8207d-150">Mapitags.h</span></span>
  
> <span data-ttu-id="8207d-151">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8207d-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8207d-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="8207d-152">See also</span></span>



[<span data-ttu-id="8207d-153">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8207d-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8207d-154">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8207d-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8207d-155">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8207d-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8207d-156">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8207d-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

