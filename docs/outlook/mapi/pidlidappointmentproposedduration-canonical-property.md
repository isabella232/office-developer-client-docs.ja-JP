---
title: PidLidAppointmentProposedDuration 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e3983a110ee9a72f3c82eaf1bbebc810d07f3c4b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591304"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a><span data-ttu-id="47546-103">PidLidAppointmentProposedDuration 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="47546-103">PidLidAppointmentProposedDuration Canonical Property</span></span>

  
  
<span data-ttu-id="47546-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47546-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47546-105">提案された新しい日時の指定の**dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) プロパティの値を示します。</span><span class="sxs-lookup"><span data-stu-id="47546-105">Indicates the proposed value for the **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) property for a counter proposal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47546-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="47546-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="47546-107">dispidApptProposedDuration</span><span class="sxs-lookup"><span data-stu-id="47546-107">dispidApptProposedDuration</span></span>  <br/> |
|<span data-ttu-id="47546-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="47546-108">Property set:</span></span>  <br/> |<span data-ttu-id="47546-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="47546-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="47546-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="47546-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="47546-111">0x00008256</span><span class="sxs-lookup"><span data-stu-id="47546-111">0x00008256</span></span>  <br/> |
|<span data-ttu-id="47546-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="47546-112">Data type:</span></span>  <br/> |<span data-ttu-id="47546-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="47546-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="47546-114">領域:</span><span class="sxs-lookup"><span data-stu-id="47546-114">Area:</span></span>  <br/> |<span data-ttu-id="47546-115">会議</span><span class="sxs-lookup"><span data-stu-id="47546-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47546-116">注釈</span><span class="sxs-lookup"><span data-stu-id="47546-116">Remarks</span></span>

<span data-ttu-id="47546-117">かどうかを設定する必要がありますである**dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) と**dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) のプロパティの間の分の数に等しい。</span><span class="sxs-lookup"><span data-stu-id="47546-117">If set, it must be equal to the number of minutes between the **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) and **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="47546-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="47546-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="47546-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="47546-119">Protocol specifications</span></span>

<span data-ttu-id="47546-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47546-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47546-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="47546-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="47546-122">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47546-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="47546-123">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="47546-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="47546-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="47546-124">Header files</span></span>

<span data-ttu-id="47546-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47546-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="47546-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="47546-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="47546-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="47546-127">See also</span></span>



[<span data-ttu-id="47546-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47546-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="47546-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="47546-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="47546-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47546-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="47546-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="47546-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

