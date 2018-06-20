---
title: PidLidNonSendableBccTrackStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: da2bd4e87c7076872ccff708983cfbe631b27122
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802048"
---
# <a name="pidlidnonsendablebcctrackstatus-canonical-property"></a><span data-ttu-id="972ab-103">PidLidNonSendableBccTrackStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="972ab-103">PidLidNonSendableBccTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="972ab-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="972ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="972ab-105">**DispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="972ab-105">Contains the value for each attendee that is listed in the **dispidNonSendableBCC** ([PidLidNonSendableBcc](pidlidnonsendablebcc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="972ab-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="972ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="972ab-107">dispidNonSendBccTrackStatus</span><span class="sxs-lookup"><span data-stu-id="972ab-107">dispidNonSendBccTrackStatus</span></span>  <br/> |
|<span data-ttu-id="972ab-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="972ab-108">Property set:</span></span>  <br/> |<span data-ttu-id="972ab-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="972ab-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="972ab-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="972ab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="972ab-111">0x00008545</span><span class="sxs-lookup"><span data-stu-id="972ab-111">0x00008545</span></span>  <br/> |
|<span data-ttu-id="972ab-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="972ab-112">Data type:</span></span>  <br/> |<span data-ttu-id="972ab-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="972ab-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="972ab-114">領域:</span><span class="sxs-lookup"><span data-stu-id="972ab-114">Area:</span></span>  <br/> |<span data-ttu-id="972ab-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="972ab-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="972ab-116">備考</span><span class="sxs-lookup"><span data-stu-id="972ab-116">Remarks</span></span>

<span data-ttu-id="972ab-117">**DispidNonSendableBCC**プロパティが設定されている場合にのみ、このプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="972ab-117">This property is required only when the **dispidNonSendableBCC** property is set.</span></span> <span data-ttu-id="972ab-118">このプロパティの値の数は、 **dispidNonSendableBCC**内の値の数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="972ab-118">The number of values in this property must equal the number of values in the **dispidNonSendableBCC**.</span></span> <span data-ttu-id="972ab-119">このプロパティの各値は、同じインデックス位置にある**dispidNonSendableBCC**プロパティに出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="972ab-119">Each value in this property corresponds to the attendee in the **dispidNonSendableBCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="972ab-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="972ab-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="972ab-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="972ab-121">Protocol specifications</span></span>

<span data-ttu-id="972ab-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="972ab-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="972ab-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="972ab-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="972ab-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="972ab-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="972ab-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="972ab-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="972ab-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="972ab-126">Header files</span></span>

<span data-ttu-id="972ab-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="972ab-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="972ab-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="972ab-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="972ab-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="972ab-129">See also</span></span>



[<span data-ttu-id="972ab-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="972ab-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="972ab-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="972ab-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="972ab-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="972ab-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="972ab-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="972ab-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

