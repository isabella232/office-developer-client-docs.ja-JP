---
title: PidLidOriginalStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOriginalStoreEntryId
api_type:
- COM
ms.assetid: 1b1fc008-9cd5-49f6-9f91-b59e305a1e82
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 83ca47d0b7e10bff4b2274ef8a8c7dd7b5421d54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359116"
---
# <a name="pidlidoriginalstoreentryid-canonical-property"></a><span data-ttu-id="91e5e-103">PidLidOriginalStoreEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91e5e-103">PidLidOriginalStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="91e5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91e5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91e5e-105">委任者のストアのエントリ ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="91e5e-105">Specifies the entry ID of the delegator's store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91e5e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="91e5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91e5e-107">dispidOrigStoreEid</span><span class="sxs-lookup"><span data-stu-id="91e5e-107">dispidOrigStoreEid</span></span>  <br/> |
|<span data-ttu-id="91e5e-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="91e5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="91e5e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="91e5e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="91e5e-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="91e5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91e5e-111">0x00008237</span><span class="sxs-lookup"><span data-stu-id="91e5e-111">0x00008237</span></span>  <br/> |
|<span data-ttu-id="91e5e-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="91e5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="91e5e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91e5e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91e5e-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="91e5e-114">Area:</span></span>  <br/> |<span data-ttu-id="91e5e-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="91e5e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91e5e-116">解説</span><span class="sxs-lookup"><span data-stu-id="91e5e-116">Remarks</span></span>

<span data-ttu-id="91e5e-117">このプロパティは、代理人によって作成または更新された会議オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91e5e-117">This property should be set on meeting objects which have been created or updated by a delegate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91e5e-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="91e5e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91e5e-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="91e5e-119">Protocol specifications</span></span>

<span data-ttu-id="91e5e-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91e5e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91e5e-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="91e5e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91e5e-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91e5e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91e5e-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="91e5e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91e5e-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="91e5e-124">Header files</span></span>

<span data-ttu-id="91e5e-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91e5e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="91e5e-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="91e5e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91e5e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="91e5e-127">See also</span></span>



[<span data-ttu-id="91e5e-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="91e5e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91e5e-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="91e5e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91e5e-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91e5e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91e5e-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="91e5e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

