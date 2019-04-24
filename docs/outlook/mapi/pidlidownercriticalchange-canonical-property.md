---
title: PidLidOwnerCriticalChange 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOwnerCriticalChange
api_type:
- COM
ms.assetid: b79aa2b7-b6e0-46dc-89f1-f801a6b5737a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: afc3c93e56c8beda9cb04c79164790b2246de983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357947"
---
# <a name="pidlidownercriticalchange-canonical-property"></a><span data-ttu-id="62aed-103">PidLidOwnerCriticalChange 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="62aed-103">PidLidOwnerCriticalChange Canonical Property</span></span>

  
  
<span data-ttu-id="62aed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62aed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62aed-105">開催者が会議出席依頼を送信した日付と時刻を指定します。</span><span class="sxs-lookup"><span data-stu-id="62aed-105">Specifies the date and time when a meeting request was sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62aed-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="62aed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62aed-107">LID_OWNER_CRITICAL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="62aed-107">LID_OWNER_CRITICAL_CHANGE</span></span>  <br/> |
|<span data-ttu-id="62aed-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="62aed-108">Property set:</span></span>  <br/> |<span data-ttu-id="62aed-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="62aed-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="62aed-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="62aed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62aed-111">0x0000001a</span><span class="sxs-lookup"><span data-stu-id="62aed-111">0x0000001A</span></span>  <br/> |
|<span data-ttu-id="62aed-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="62aed-112">Data type:</span></span>  <br/> |<span data-ttu-id="62aed-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="62aed-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="62aed-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="62aed-114">Area:</span></span>  <br/> |<span data-ttu-id="62aed-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="62aed-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62aed-116">解説</span><span class="sxs-lookup"><span data-stu-id="62aed-116">Remarks</span></span>

<span data-ttu-id="62aed-117">値は協定世界時 (UTC) で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62aed-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62aed-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="62aed-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62aed-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="62aed-119">Protocol specifications</span></span>

<span data-ttu-id="62aed-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62aed-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62aed-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="62aed-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62aed-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62aed-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62aed-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="62aed-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62aed-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="62aed-124">Header files</span></span>

<span data-ttu-id="62aed-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62aed-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="62aed-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="62aed-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62aed-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="62aed-127">See also</span></span>



[<span data-ttu-id="62aed-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="62aed-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62aed-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="62aed-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62aed-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="62aed-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62aed-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="62aed-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

