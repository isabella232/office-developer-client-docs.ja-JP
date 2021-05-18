---
title: PidLidNonSendableBccTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBccTrackStatus
api_type:
- COM
ms.assetid: daad8735-a3da-4a0b-9329-6eb253c281fd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5c795f15046bcab40abc2396b36e14925d3869d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359949"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="c5903-103">PidLidNonSendableBccTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5903-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c5903-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5903-105">**dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) プロパティにリストされている各出席者の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="c5903-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5903-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c5903-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5903-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="c5903-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="c5903-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="c5903-108">Property set:</span></span>  <br/> |<span data-ttu-id="c5903-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c5903-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c5903-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c5903-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c5903-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="c5903-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="c5903-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c5903-112">Data type:</span></span>  <br/> |<span data-ttu-id="c5903-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c5903-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c5903-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c5903-114">Area:</span></span>  <br/> |<span data-ttu-id="c5903-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="c5903-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5903-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c5903-116">Remarks</span></span>

<span data-ttu-id="c5903-117">このプロパティは **、dispidNonSendableBCC** プロパティが設定されている場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="c5903-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="c5903-118">このプロパティの値の数は **、dispidNonSendableBCC の値の数と等しくする必要があります**。</span><span class="sxs-lookup"><span data-stu-id="c5903-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="c5903-119">このプロパティの各値は、同じインデックスにある **dispidNonSendableBCC** プロパティの出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="c5903-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c5903-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c5903-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5903-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c5903-121">Protocol specifications</span></span>

<span data-ttu-id="c5903-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5903-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5903-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="c5903-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5903-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5903-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5903-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5903-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5903-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c5903-126">Header files</span></span>

<span data-ttu-id="c5903-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5903-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5903-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5903-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5903-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5903-129">See also</span></span>



[<span data-ttu-id="c5903-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c5903-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5903-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c5903-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5903-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5903-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5903-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c5903-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

