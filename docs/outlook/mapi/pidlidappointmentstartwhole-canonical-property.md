---
title: PidLidAppointmentStartWhole の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f7137e3d5712e7d7ce12800a07b860679dd099a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801829"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="090f7-103">PidLidAppointmentStartWhole の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="090f7-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="090f7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="090f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="090f7-105">予定を開始する時刻と日付を表します。</span><span class="sxs-lookup"><span data-stu-id="090f7-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="090f7-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="090f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="090f7-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="090f7-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="090f7-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="090f7-108">Property set:</span></span>  <br/> |<span data-ttu-id="090f7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="090f7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="090f7-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="090f7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="090f7-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="090f7-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="090f7-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="090f7-112">Data type:</span></span>  <br/> |<span data-ttu-id="090f7-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="090f7-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="090f7-114">領域:</span><span class="sxs-lookup"><span data-stu-id="090f7-114">Area:</span></span>  <br/> |<span data-ttu-id="090f7-115">カレンダー</span><span class="sxs-lookup"><span data-stu-id="090f7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="090f7-116">備考</span><span class="sxs-lookup"><span data-stu-id="090f7-116">Remarks</span></span>

<span data-ttu-id="090f7-117">このプロパティは、イベントの開始日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="090f7-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="090f7-118">このプロパティは、世界協定時刻 (UTC) である必要があります、 **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) プロパティの値より小さくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="090f7-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="090f7-119">定期的な一連のこのプロパティは、定期的なアイテムのパターンに従って、最初のインスタンスの開始日時です。</span><span class="sxs-lookup"><span data-stu-id="090f7-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="090f7-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="090f7-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="090f7-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="090f7-121">Protocol specifications</span></span>

<span data-ttu-id="090f7-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="090f7-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="090f7-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="090f7-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="090f7-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="090f7-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="090f7-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="090f7-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="090f7-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="090f7-126">Header files</span></span>

<span data-ttu-id="090f7-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="090f7-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="090f7-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="090f7-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="090f7-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="090f7-129">See also</span></span>



[<span data-ttu-id="090f7-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="090f7-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="090f7-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="090f7-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="090f7-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="090f7-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="090f7-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="090f7-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

