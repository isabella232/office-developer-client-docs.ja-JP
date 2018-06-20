---
title: PidLidNonSendToTrackStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 45d8512d48a1908d81e78b87c5975ab2da8c6c80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802057"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a><span data-ttu-id="db7b6-103">PidLidNonSendToTrackStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="db7b6-103">PidLidNonSendToTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="db7b6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db7b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db7b6-105">**DispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) のプロパティに記載されている各出席者の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db7b6-105">Contains the value for each attendee listed in the **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db7b6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="db7b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db7b6-107">dispidNonSendToTrackStatus</span><span class="sxs-lookup"><span data-stu-id="db7b6-107">dispidNonSendToTrackStatus</span></span>  <br/> |
|<span data-ttu-id="db7b6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-108">Property set:</span></span>  <br/> |<span data-ttu-id="db7b6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="db7b6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="db7b6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="db7b6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="db7b6-111">0x00008543</span><span class="sxs-lookup"><span data-stu-id="db7b6-111">0x00008543</span></span>  <br/> |
|<span data-ttu-id="db7b6-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-112">Data type:</span></span>  <br/> |<span data-ttu-id="db7b6-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="db7b6-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="db7b6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="db7b6-114">Area:</span></span>  <br/> |<span data-ttu-id="db7b6-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="db7b6-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db7b6-116">備考</span><span class="sxs-lookup"><span data-stu-id="db7b6-116">Remarks</span></span>

<span data-ttu-id="db7b6-117">**DispidNonSendableTo**プロパティが設定されている場合にのみ、このプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="db7b6-117">This property is required only when the **dispidNonSendableTo** property is set.</span></span> <span data-ttu-id="db7b6-118">このプロパティの値の数は、 **dispidNonSendableTo**内の値の数に等しくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="db7b6-118">The number of values in this property must equal the number of values in **dispidNonSendableTo**.</span></span> <span data-ttu-id="db7b6-119">このプロパティでは、各 PT_LONG 値は、同じインデックス位置にある**dispidNonSendableTo**プロパティに出席者に対応します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableTo** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="db7b6-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="db7b6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db7b6-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="db7b6-121">Protocol specifications</span></span>

<span data-ttu-id="db7b6-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db7b6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db7b6-123">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db7b6-124">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db7b6-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db7b6-125">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db7b6-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="db7b6-126">Header files</span></span>

<span data-ttu-id="db7b6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db7b6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="db7b6-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="db7b6-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db7b6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="db7b6-129">See also</span></span>



[<span data-ttu-id="db7b6-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="db7b6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db7b6-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="db7b6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db7b6-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="db7b6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db7b6-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="db7b6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

