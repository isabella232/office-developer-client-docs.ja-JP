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
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321323"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a><span data-ttu-id="bb881-103">PidTagScheduleInfoAppointmentTombstone 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb881-103">PidTagScheduleInfoAppointmentTombstone Canonical Property</span></span>

  
  
<span data-ttu-id="bb881-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb881-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb881-105">辞退された会議を表すデータブロックの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb881-105">Contains a list of data blocks that represent meetings that have been declined.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb881-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bb881-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb881-107">PR_SCHDINFO_APPT_TOMBSTONE</span><span class="sxs-lookup"><span data-stu-id="bb881-107">PR_SCHDINFO_APPT_TOMBSTONE</span></span>  <br/> |
|<span data-ttu-id="bb881-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bb881-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb881-109">0x686a</span><span class="sxs-lookup"><span data-stu-id="bb881-109">0x686A</span></span>  <br/> |
|<span data-ttu-id="bb881-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bb881-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb881-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb881-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb881-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bb881-112">Area:</span></span>  <br/> |<span data-ttu-id="bb881-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="bb881-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb881-114">解説</span><span class="sxs-lookup"><span data-stu-id="bb881-114">Remarks</span></span>

<span data-ttu-id="bb881-115">データブロックは、次のように定義された32ビット値のヘッダーで始まります。</span><span class="sxs-lookup"><span data-stu-id="bb881-115">The data blocks begin with a header of 32 bit values defined as:</span></span>
  
|<span data-ttu-id="bb881-116">**値**</span><span class="sxs-lookup"><span data-stu-id="bb881-116">**Value**</span></span>|<span data-ttu-id="bb881-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="bb881-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb881-118">Identifier</span><span class="sxs-lookup"><span data-stu-id="bb881-118">Identifier</span></span>  <br/> |<span data-ttu-id="bb881-119">このフィールドには、0xBEDEAFCD の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb881-119">This field must be the value 0xBEDEAFCD.</span></span>  <br/> |
|<span data-ttu-id="bb881-120">headersize</span><span class="sxs-lookup"><span data-stu-id="bb881-120">HeaderSize</span></span>  <br/> |<span data-ttu-id="bb881-121">このフィールドの値は0x00000014 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb881-121">This field must have the value 0x00000014.</span></span>  <br/> |
|<span data-ttu-id="bb881-122">バージョン</span><span class="sxs-lookup"><span data-stu-id="bb881-122">Version</span></span>  <br/> |<span data-ttu-id="bb881-123">このフィールドの値は3である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb881-123">This field must have the value 3.</span></span>  <br/> |
|<span data-ttu-id="bb881-124">レコード数</span><span class="sxs-lookup"><span data-stu-id="bb881-124">RecordsCount</span></span>  <br/> |<span data-ttu-id="bb881-125">フォローされているレコードの数。</span><span class="sxs-lookup"><span data-stu-id="bb881-125">The count of records that follow.</span></span>  <br/> |
|<span data-ttu-id="bb881-126">レコードサイズ</span><span class="sxs-lookup"><span data-stu-id="bb881-126">RecordsSize</span></span>  <br/> |<span data-ttu-id="bb881-127">このフィールドの値は0x00000014 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb881-127">This field must have the value 0x00000014.</span></span>  <br/> |
   
<span data-ttu-id="bb881-128">ヘッダーの後には、次のように定義された32ビット値の**レコード数**エントリが続きます。</span><span class="sxs-lookup"><span data-stu-id="bb881-128">The header is followed by **RecordsCount** entries of 32 bit values defined as:</span></span> 
  
|<span data-ttu-id="bb881-129">**値**</span><span class="sxs-lookup"><span data-stu-id="bb881-129">**Value**</span></span>|<span data-ttu-id="bb881-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="bb881-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb881-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="bb881-131">StartTime</span></span>  <br/> |<span data-ttu-id="bb881-132">会議オブジェクトの開始時刻を、1601年1月1日午前0時からの経過時間 (分) で示します。</span><span class="sxs-lookup"><span data-stu-id="bb881-132">The meeting object's start time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="bb881-133">EndTime</span><span class="sxs-lookup"><span data-stu-id="bb881-133">EndTime</span></span>  <br/> |<span data-ttu-id="bb881-134">会議オブジェクトの終了時刻を、1601年1月1日午前0時からの経過時間 (分) で示します。</span><span class="sxs-lookup"><span data-stu-id="bb881-134">The meeting object's end time in minutes since midnight, January 1, 1601, UTC.</span></span>  <br/> |
|<span data-ttu-id="bb881-135">GlobalObjectIdSize</span><span class="sxs-lookup"><span data-stu-id="bb881-135">GlobalObjectIdSize</span></span>  <br/> |<span data-ttu-id="bb881-136">globalobjectid フィールドのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="bb881-136">The size, in bytes, of the GlobalObjectId field.</span></span>  <br/> |
|<span data-ttu-id="bb881-137">globalobjectid</span><span class="sxs-lookup"><span data-stu-id="bb881-137">GlobalObjectId</span></span>  <br/> |<span data-ttu-id="bb881-138">このレコードが表す会議の**LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="bb881-138">The value of the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) property of the meeting this record represents.</span></span>  <br/> |
|<span data-ttu-id="bb881-139">UserName</span><span class="sxs-lookup"><span data-stu-id="bb881-139">UserName</span></span>  <br/> |<span data-ttu-id="bb881-140">最初の2バイトは、その後に続く PT_STRING8 文字列の長さです。</span><span class="sxs-lookup"><span data-stu-id="bb881-140">The first two bytes are the length of the PT_STRING8 string that follows.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bb881-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb881-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb881-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bb881-142">Protocol specifications</span></span>

<span data-ttu-id="bb881-143">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb881-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb881-144">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb881-144">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb881-145">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb881-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb881-146">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb881-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb881-147">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bb881-147">Header files</span></span>

<span data-ttu-id="bb881-148">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb881-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb881-149">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb881-149">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb881-150">Mapitags</span><span class="sxs-lookup"><span data-stu-id="bb881-150">Mapitags.h</span></span>
  
> <span data-ttu-id="bb881-151">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb881-151">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb881-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb881-152">See also</span></span>



[<span data-ttu-id="bb881-153">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb881-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb881-154">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb881-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb881-155">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb881-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb881-156">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bb881-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

