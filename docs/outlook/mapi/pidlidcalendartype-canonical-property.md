---
title: PidLidCalendarType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801834"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="234a6-103">PidLidCalendarType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="234a6-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="234a6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="234a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="234a6-105">**DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) のプロパティから [カレンダーの種類] フィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="234a6-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="234a6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="234a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="234a6-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="234a6-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="234a6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="234a6-108">Property set:</span></span>  <br/> |<span data-ttu-id="234a6-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="234a6-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="234a6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="234a6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="234a6-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="234a6-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="234a6-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="234a6-112">Data type:</span></span>  <br/> |<span data-ttu-id="234a6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="234a6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="234a6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="234a6-114">Area:</span></span>  <br/> |<span data-ttu-id="234a6-115">会議</span><span class="sxs-lookup"><span data-stu-id="234a6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="234a6-116">備考</span><span class="sxs-lookup"><span data-stu-id="234a6-116">Remarks</span></span>

<span data-ttu-id="234a6-117">会議出席依頼は、一連の定期的なまたは例外を表している場合は、 **dispidApptRecur**プロパティから [カレンダーの種類] フィールドの値になります。</span><span class="sxs-lookup"><span data-stu-id="234a6-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="234a6-118">それ以外の場合、このプロパティは設定されず、0 と見なされます。</span><span class="sxs-lookup"><span data-stu-id="234a6-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="234a6-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="234a6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="234a6-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="234a6-120">Protocol specifications</span></span>

<span data-ttu-id="234a6-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="234a6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="234a6-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="234a6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="234a6-123">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="234a6-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="234a6-124">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="234a6-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="234a6-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="234a6-125">Header files</span></span>

<span data-ttu-id="234a6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="234a6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="234a6-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="234a6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="234a6-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="234a6-128">See also</span></span>



[<span data-ttu-id="234a6-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="234a6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="234a6-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="234a6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="234a6-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="234a6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="234a6-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="234a6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

