---
title: PidLidNonSendCcTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319671"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="99fef-103">PidLidNonSendCcTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="99fef-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="99fef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99fef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99fef-105">**dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) プロパティにリストされている各出席者の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="99fef-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="99fef-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="99fef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="99fef-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="99fef-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="99fef-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="99fef-108">Property set:</span></span>  <br/> |<span data-ttu-id="99fef-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="99fef-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="99fef-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="99fef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="99fef-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="99fef-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="99fef-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="99fef-112">Data type:</span></span>  <br/> |<span data-ttu-id="99fef-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="99fef-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="99fef-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="99fef-114">Area:</span></span>  <br/> |<span data-ttu-id="99fef-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="99fef-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99fef-116">注釈</span><span class="sxs-lookup"><span data-stu-id="99fef-116">Remarks</span></span>

<span data-ttu-id="99fef-117">このプロパティは **、dispidNonSendableCC** プロパティが設定されている場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="99fef-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="99fef-118">このプロパティの値の数は **、dispidNonSendableCC の値の数と等しくする必要があります**。</span><span class="sxs-lookup"><span data-stu-id="99fef-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="99fef-119">このPT_LONGの各値は、同じインデックスにある **dispidNonSendableCC** プロパティの出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="99fef-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="99fef-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="99fef-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="99fef-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="99fef-121">Protocol specifications</span></span>

<span data-ttu-id="99fef-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99fef-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99fef-123">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="99fef-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="99fef-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="99fef-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="99fef-125">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="99fef-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="99fef-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="99fef-126">Header files</span></span>

<span data-ttu-id="99fef-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="99fef-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="99fef-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="99fef-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99fef-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="99fef-129">See also</span></span>



[<span data-ttu-id="99fef-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="99fef-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="99fef-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="99fef-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="99fef-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="99fef-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="99fef-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="99fef-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

