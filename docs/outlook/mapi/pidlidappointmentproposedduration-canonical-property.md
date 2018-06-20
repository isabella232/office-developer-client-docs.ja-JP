---
title: PidLidAppointmentProposedDuration の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 56891591871831ba9496f50b69bf4b94ef012c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801729"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="f6df8-103">PidLidAppointmentProposedDuration の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="f6df8-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="f6df8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6df8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6df8-105">提案された新しい日時の指定の**dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) プロパティの値を示します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f6df8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f6df8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6df8-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="f6df8-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="f6df8-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-108">Property set:</span></span>  <br/> |<span data-ttu-id="f6df8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f6df8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f6df8-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f6df8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f6df8-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="f6df8-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="f6df8-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-112">Data type:</span></span>  <br/> |<span data-ttu-id="f6df8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f6df8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f6df8-114">領域:</span><span class="sxs-lookup"><span data-stu-id="f6df8-114">Area:</span></span>  <br/> |<span data-ttu-id="f6df8-115">会議</span><span class="sxs-lookup"><span data-stu-id="f6df8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6df8-116">備考</span><span class="sxs-lookup"><span data-stu-id="f6df8-116">Remarks</span></span>

<span data-ttu-id="f6df8-117">かどうかを設定する必要がありますである**dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) と**dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) のプロパティの間の分の数に等しい。</span><span class="sxs-lookup"><span data-stu-id="f6df8-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f6df8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f6df8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6df8-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f6df8-119">Protocol specifications</span></span>

<span data-ttu-id="f6df8-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6df8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6df8-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6df8-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6df8-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6df8-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6df8-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f6df8-124">Header files</span></span>

<span data-ttu-id="f6df8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6df8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6df8-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6df8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6df8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6df8-127">See also</span></span>



[<span data-ttu-id="f6df8-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6df8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6df8-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6df8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6df8-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="f6df8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6df8-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="f6df8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

