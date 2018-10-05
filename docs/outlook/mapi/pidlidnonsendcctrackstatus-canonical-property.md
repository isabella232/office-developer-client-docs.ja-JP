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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383178"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="9e08f-103">PidLidNonSendCcTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e08f-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="9e08f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e08f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e08f-105">**DispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9e08f-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9e08f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9e08f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e08f-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="9e08f-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="9e08f-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e08f-108">Property set:</span></span>  <br/> |<span data-ttu-id="9e08f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="9e08f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="9e08f-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9e08f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9e08f-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="9e08f-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="9e08f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9e08f-112">Data type:</span></span>  <br/> |<span data-ttu-id="9e08f-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="9e08f-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="9e08f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="9e08f-114">Area:</span></span>  <br/> |<span data-ttu-id="9e08f-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="9e08f-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e08f-116">備考</span><span class="sxs-lookup"><span data-stu-id="9e08f-116">Remarks</span></span>

<span data-ttu-id="9e08f-117">**DispidNonSendableCC**プロパティが設定されている場合にのみ、このプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="9e08f-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="9e08f-118">このプロパティの値の数は、 **dispidNonSendableCC**内の値の数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9e08f-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="9e08f-119">このプロパティでは、各 PT_LONG 値は、同じインデックス位置にある**dispidNonSendableCC**プロパティに出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="9e08f-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9e08f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9e08f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9e08f-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9e08f-121">Protocol specifications</span></span>

<span data-ttu-id="9e08f-122">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e08f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e08f-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9e08f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9e08f-124">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9e08f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9e08f-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e08f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9e08f-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9e08f-126">Header files</span></span>

<span data-ttu-id="9e08f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e08f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e08f-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9e08f-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e08f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e08f-129">See also</span></span>



[<span data-ttu-id="9e08f-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e08f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e08f-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9e08f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e08f-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9e08f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e08f-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9e08f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

