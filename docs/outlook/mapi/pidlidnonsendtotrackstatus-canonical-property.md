---
title: PidLidNonSendToTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf9d11b7a53ee0b9911e32cb3c3e2a0a490e4729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592788"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="c4551-103">PidLidNonSendToTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4551-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c4551-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4551-105">**DispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c4551-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4551-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c4551-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4551-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="c4551-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="c4551-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4551-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4551-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c4551-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c4551-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c4551-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c4551-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="c4551-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="c4551-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c4551-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4551-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c4551-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c4551-114">領域:</span><span class="sxs-lookup"><span data-stu-id="c4551-114">Area:</span></span>  <br/> |<span data-ttu-id="c4551-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="c4551-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4551-116">注釈</span><span class="sxs-lookup"><span data-stu-id="c4551-116">Remarks</span></span>

<span data-ttu-id="c4551-117">**DispidNonSendableTo**プロパティが設定されている場合にのみ、このプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="c4551-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="c4551-118">このプロパティの値の数は、 **dispidNonSendableTo**内の値の数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c4551-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="c4551-119">このプロパティでは、各 PT_LONG 値は、同じインデックス位置にある**dispidNonSendableTo**プロパティに出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="c4551-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c4551-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4551-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4551-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4551-121">Protocol specifications</span></span>

<span data-ttu-id="c4551-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4551-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4551-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4551-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4551-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4551-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4551-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4551-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4551-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4551-126">Header files</span></span>

<span data-ttu-id="c4551-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4551-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4551-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4551-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4551-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4551-129">See also</span></span>



[<span data-ttu-id="c4551-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4551-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4551-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4551-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4551-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c4551-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4551-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c4551-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

