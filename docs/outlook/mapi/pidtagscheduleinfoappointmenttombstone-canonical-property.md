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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321323"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="249e1-103">PidTagScheduleInfoAppointmentTombstone 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="249e1-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="249e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="249e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="249e1-105">拒否された会議を表すデータ ブロックの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="249e1-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="249e1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="249e1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="249e1-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="249e1-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="249e1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="249e1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="249e1-109">0x686A</span><span class="sxs-lookup"><span data-stu-id="249e1-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="249e1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="249e1-110">Data type:</span></span>  <br/> |<span data-ttu-id="249e1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="249e1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="249e1-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="249e1-112">Area:</span></span>  <br/> |<span data-ttu-id="249e1-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="249e1-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="249e1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="249e1-114">Remarks</span></span>

<span data-ttu-id="249e1-115">データ ブロックは、次のように定義された 32 ビット値のヘッダーで始まります。</span><span class="sxs-lookup"><span data-stu-id="249e1-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="249e1-116">**値**</span><span class="sxs-lookup"><span data-stu-id="249e1-116">**Value**</span></span>|<span data-ttu-id="249e1-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="249e1-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="249e1-118">識別子</span><span class="sxs-lookup"><span data-stu-id="249e1-118">Identifier</span></span>  <br/> |<span data-ttu-id="249e1-119">このフィールドは、次の値0xBEDEAFCD。</span><span class="sxs-lookup"><span data-stu-id="249e1-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="249e1-120">HeaderSize</span><span class="sxs-lookup"><span data-stu-id="249e1-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="249e1-121">このフィールドには、値が0x00000014。</span><span class="sxs-lookup"><span data-stu-id="249e1-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="249e1-122">バージョン</span><span class="sxs-lookup"><span data-stu-id="249e1-122">Version</span></span>  <br/> |<span data-ttu-id="249e1-123">このフィールドの値は 3 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="249e1-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="249e1-124">RecordsCount</span><span class="sxs-lookup"><span data-stu-id="249e1-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="249e1-125">続くレコードの数。</span><span class="sxs-lookup"><span data-stu-id="249e1-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="249e1-126">RecordsSize</span><span class="sxs-lookup"><span data-stu-id="249e1-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="249e1-127">このフィールドには、値が0x00000014。</span><span class="sxs-lookup"><span data-stu-id="249e1-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="249e1-128">ヘッダーの後に、次のように定義された 32 ビット値の **RecordsCount** エントリが続きます。</span><span class="sxs-lookup"><span data-stu-id="249e1-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="249e1-129">**値**</span><span class="sxs-lookup"><span data-stu-id="249e1-129">**Value**</span></span>|<span data-ttu-id="249e1-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="249e1-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="249e1-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="249e1-131">StartTime</span></span>  <br/> |<span data-ttu-id="249e1-132">会議オブジェクトの開始時刻 (1601 年 1 月 1 日午前 0 時から分) (UTC)。</span><span class="sxs-lookup"><span data-stu-id="249e1-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="249e1-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="249e1-133">EndTime</span></span>  <br/> |<span data-ttu-id="249e1-134">1601 年 1 月 1 日午前 0 時以降の会議オブジェクトの終了時刻 (分)。</span><span class="sxs-lookup"><span data-stu-id="249e1-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="249e1-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="249e1-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="249e1-136">GlobalObjectId フィールドのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="249e1-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="249e1-137">GlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="249e1-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="249e1-138">このレコードが表 **す会議LID_GLOBAL_OBJID** [(PidLidGlobalObjectId)](pidlidglobalobjectid-canonical-property.md)プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="249e1-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="249e1-139">UserName</span><span class="sxs-lookup"><span data-stu-id="249e1-139">UserName</span></span>  <br/> |<span data-ttu-id="249e1-140">最初の 2 バイトは、次の文字列PT_STRING8長さです。</span><span class="sxs-lookup"><span data-stu-id="249e1-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="249e1-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="249e1-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="249e1-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="249e1-142">Protocol specifications</span></span>

<span data-ttu-id="249e1-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="249e1-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="249e1-144">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="249e1-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="249e1-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="249e1-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="249e1-146">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="249e1-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="249e1-147">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="249e1-147">Header files</span></span>

<span data-ttu-id="249e1-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="249e1-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="249e1-149">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="249e1-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="249e1-150">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="249e1-150">Mapitags.h</span></span>
  
> <span data-ttu-id="249e1-151">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="249e1-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="249e1-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="249e1-152">See also</span></span>



[<span data-ttu-id="249e1-153">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="249e1-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="249e1-154">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="249e1-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="249e1-155">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="249e1-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="249e1-156">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="249e1-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

