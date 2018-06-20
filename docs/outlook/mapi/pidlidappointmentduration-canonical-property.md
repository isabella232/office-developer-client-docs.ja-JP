---
title: PidLidAppointmentDuration の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d124bd3aa4350863351284a9e4b19ca4533e382
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801732"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="06277-103">PidLidAppointmentDuration の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="06277-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="06277-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06277-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06277-105">分単位で予定をスケジュールするときの時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="06277-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06277-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="06277-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06277-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="06277-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="06277-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="06277-108">Property set:</span></span>  <br/> |<span data-ttu-id="06277-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="06277-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="06277-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="06277-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="06277-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="06277-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="06277-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="06277-112">Data type:</span></span>  <br/> |<span data-ttu-id="06277-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06277-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06277-114">領域:</span><span class="sxs-lookup"><span data-stu-id="06277-114">Area:</span></span>  <br/> |<span data-ttu-id="06277-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="06277-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06277-116">備考</span><span class="sxs-lookup"><span data-stu-id="06277-116">Remarks</span></span>

<span data-ttu-id="06277-117">値は**dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) の値と**dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) のプロパティとの間の時間を分単位である必要があります。</span><span class="sxs-lookup"><span data-stu-id="06277-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="06277-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06277-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06277-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="06277-119">Protocol specifications</span></span>

<span data-ttu-id="06277-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06277-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06277-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="06277-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06277-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06277-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06277-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="06277-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06277-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06277-124">Header files</span></span>

<span data-ttu-id="06277-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06277-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="06277-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06277-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06277-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="06277-127">See also</span></span>



[<span data-ttu-id="06277-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06277-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06277-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="06277-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06277-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="06277-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06277-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="06277-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

