---
title: PidTagRecipientProposedEndTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedEndTime
api_type:
- COM
ms.assetid: 08dc1f81-964b-4059-9167-e517391b26e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ea6d634b0e69cf6895c076815941754ba5e83a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332775"
---
# <a name="pidtagrecipientproposedendtime-canonical-property"></a><span data-ttu-id="e3d95-103">PidTagRecipientProposedEndTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d95-103">PidTagRecipientProposedEndTime Canonical Property</span></span>

  
  
<span data-ttu-id="e3d95-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3d95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3d95-105">会議の終了時刻の提案を示します。</span><span class="sxs-lookup"><span data-stu-id="e3d95-105">Indicates a proposed end time of a meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3d95-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e3d95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3d95-107">PR_RECIPIENT_PROPOSEDENDTIME</span><span class="sxs-lookup"><span data-stu-id="e3d95-107">PR_RECIPIENT_PROPOSEDENDTIME</span></span>  <br/> |
|<span data-ttu-id="e3d95-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e3d95-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e3d95-109">0x5fe4</span><span class="sxs-lookup"><span data-stu-id="e3d95-109">0x5FE4</span></span>  <br/> |
|<span data-ttu-id="e3d95-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e3d95-110">Data type:</span></span>  <br/> |<span data-ttu-id="e3d95-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e3d95-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e3d95-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e3d95-112">Area:</span></span>  <br/> |<span data-ttu-id="e3d95-113">トランスポート受信者</span><span class="sxs-lookup"><span data-stu-id="e3d95-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3d95-114">解説</span><span class="sxs-lookup"><span data-stu-id="e3d95-114">Remarks</span></span>

<span data-ttu-id="e3d95-115">**PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) プロパティの値が TRUE に設定されている場合、このプロパティの値は出席者が要求した値を**dispidApptEndWhole**の値として設定することを示します ([](pidlidappointmentendwhole-canonical-property.md)単一インスタンスの会議オブジェクトまたは exception オブジェクトの PidLidAppointmentEndWhole) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="e3d95-115">When the value of the **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) property is set to TRUE, the value of this property indicates the value requested by the attendee to set as the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property for the single instance meeting object or exception object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e3d95-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e3d95-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3d95-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e3d95-117">Protocol specifications</span></span>

<span data-ttu-id="e3d95-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3d95-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3d95-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3d95-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3d95-120">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3d95-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3d95-121">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3d95-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3d95-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e3d95-122">Header files</span></span>

<span data-ttu-id="e3d95-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3d95-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3d95-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3d95-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3d95-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e3d95-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e3d95-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3d95-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3d95-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3d95-127">See also</span></span>



[<span data-ttu-id="e3d95-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d95-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3d95-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3d95-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3d95-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e3d95-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3d95-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e3d95-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

