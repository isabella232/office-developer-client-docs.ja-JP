---
title: PidLidTimeZone の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802261"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="6c032-103">PidLidTimeZone の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="6c032-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="6c032-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c032-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c032-105">定期的なミーティングのタイム ゾーンに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c032-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c032-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="6c032-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c032-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="6c032-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="6c032-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6c032-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c032-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="6c032-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="6c032-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6c032-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c032-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="6c032-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="6c032-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="6c032-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c032-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c032-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c032-114">領域:</span><span class="sxs-lookup"><span data-stu-id="6c032-114">Area:</span></span>  <br/> |<span data-ttu-id="6c032-115">会議</span><span class="sxs-lookup"><span data-stu-id="6c032-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c032-116">備考</span><span class="sxs-lookup"><span data-stu-id="6c032-116">Remarks</span></span>

<span data-ttu-id="6c032-117">**DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティが設定されていない場合ですが、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) プロパティが TRUE と**LID_IS_EXCEPTION** ([の場合にこのプロパティが読み取りのみPidLidIsException](pidlidisexception-canonical-property.md)) は、FALSE にします。</span><span class="sxs-lookup"><span data-stu-id="6c032-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="6c032-118">下位ワードは、タイム ゾーン情報を格納するテーブルにインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="6c032-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="6c032-119">上の word では、最上位のビットだけが読み取られます。</span><span class="sxs-lookup"><span data-stu-id="6c032-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="6c032-120">そのビットが設定されている場合、参照されているタイム ゾーンは見られません夏時間 (DST) は、それ以外の場合、夏時間の日付が[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で詳細に説明の後に。</span><span class="sxs-lookup"><span data-stu-id="6c032-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c032-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6c032-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c032-122">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6c032-122">Protocol specifications</span></span>

<span data-ttu-id="6c032-123">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c032-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c032-124">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6c032-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c032-125">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c032-125">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c032-126">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c032-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c032-127">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6c032-127">Header files</span></span>

<span data-ttu-id="6c032-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c032-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c032-129">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6c032-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c032-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c032-130">See also</span></span>



[<span data-ttu-id="6c032-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6c032-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c032-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6c032-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c032-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="6c032-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c032-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="6c032-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

