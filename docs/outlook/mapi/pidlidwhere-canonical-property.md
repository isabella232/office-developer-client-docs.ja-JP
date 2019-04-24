---
title: PidLidWhere 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidWhere
api_type:
- COM
ms.assetid: b21a3aa4-7536-4728-b4a4-273cfb25c57e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 19c3ed57d2a0bdd6902a93ca5f29deb91418b8ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360432"
---
# <a name="pidlidwhere-canonical-property"></a><span data-ttu-id="310e8-103">PidLidWhere 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="310e8-103">PidLidWhere Canonical Property</span></span>

  
  
<span data-ttu-id="310e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="310e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="310e8-105">イベントの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="310e8-105">Specifies the location of an event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="310e8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="310e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="310e8-107">LID_WHERE</span><span class="sxs-lookup"><span data-stu-id="310e8-107">LID_WHERE</span></span>  <br/> |
|<span data-ttu-id="310e8-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="310e8-108">Property set:</span></span>  <br/> |<span data-ttu-id="310e8-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="310e8-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="310e8-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="310e8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="310e8-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="310e8-111">0x00000002</span></span>  <br/> |
|<span data-ttu-id="310e8-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="310e8-112">Data type:</span></span>  <br/> |<span data-ttu-id="310e8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="310e8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="310e8-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="310e8-114">Area:</span></span>  <br/> |<span data-ttu-id="310e8-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="310e8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="310e8-116">解説</span><span class="sxs-lookup"><span data-stu-id="310e8-116">Remarks</span></span>

<span data-ttu-id="310e8-117">このプロパティの値は、関連付けられている会議の**dispidlocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) プロパティの値と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="310e8-117">The value of this property should be the same as the value of the **dispidLocation** ([PidLidLocation](pidlidlocation-canonical-property.md)) property from the associated meeting.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="310e8-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="310e8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="310e8-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="310e8-119">Protocol specifications</span></span>

<span data-ttu-id="310e8-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="310e8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="310e8-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="310e8-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="310e8-122">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="310e8-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="310e8-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="310e8-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="310e8-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="310e8-124">Header files</span></span>

<span data-ttu-id="310e8-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="310e8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="310e8-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="310e8-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="310e8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="310e8-127">See also</span></span>



[<span data-ttu-id="310e8-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="310e8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="310e8-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="310e8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="310e8-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="310e8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="310e8-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="310e8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

