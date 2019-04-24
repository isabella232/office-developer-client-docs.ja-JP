---
title: PidLidAppointmentMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358101"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="e897e-103">PidLidAppointmentMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e897e-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="e897e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e897e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e897e-105">会議出席依頼から生成される会議の**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="e897e-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e897e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e897e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e897e-107">dispidapptmessageclass</span><span class="sxs-lookup"><span data-stu-id="e897e-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="e897e-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="e897e-108">Property set:</span></span>  <br/> |<span data-ttu-id="e897e-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="e897e-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="e897e-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e897e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e897e-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="e897e-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="e897e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e897e-112">Data type:</span></span>  <br/> |<span data-ttu-id="e897e-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="e897e-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="e897e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="e897e-114">Area:</span></span>  <br/> |<span data-ttu-id="e897e-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="e897e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e897e-116">解説</span><span class="sxs-lookup"><span data-stu-id="e897e-116">Remarks</span></span>

<span data-ttu-id="e897e-117">このプロパティの値は、「IPM.」である必要があります。予定」、またはプレフィックス "IPM.予定。</span><span class="sxs-lookup"><span data-stu-id="e897e-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="e897e-118">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e897e-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e897e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e897e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e897e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e897e-120">Protocol specifications</span></span>

<span data-ttu-id="e897e-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e897e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e897e-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e897e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e897e-123">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e897e-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e897e-124">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e897e-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e897e-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e897e-125">Header files</span></span>

<span data-ttu-id="e897e-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e897e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e897e-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e897e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e897e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="e897e-128">See also</span></span>



[<span data-ttu-id="e897e-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e897e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e897e-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e897e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e897e-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e897e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e897e-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e897e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

