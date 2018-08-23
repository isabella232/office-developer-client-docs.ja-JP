---
title: PidTagSensitivity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f30a5848e07de03e61d3a63188aa7b608504ff24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573734"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="b9167-103">PidTagSensitivity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9167-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="b9167-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9167-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9167-105">メッセージの秘密度のメッセージの送信者の意見を示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9167-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9167-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b9167-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9167-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="b9167-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="b9167-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b9167-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9167-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="b9167-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="b9167-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b9167-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9167-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b9167-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b9167-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b9167-112">Area:</span></span>  <br/> |<span data-ttu-id="b9167-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="b9167-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9167-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b9167-114">Remarks</span></span>

<span data-ttu-id="b9167-115">メッセージ オブジェクトがこのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9167-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="b9167-116">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b9167-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b9167-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="b9167-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="b9167-118">メッセージには、特別な区別はありません。</span><span class="sxs-lookup"><span data-stu-id="b9167-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="b9167-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="b9167-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="b9167-120">メッセージは個人用です。</span><span class="sxs-lookup"><span data-stu-id="b9167-120">The message is personal.</span></span>
    
<span data-ttu-id="b9167-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="b9167-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="b9167-122">専用のメッセージです。</span><span class="sxs-lookup"><span data-stu-id="b9167-122">The message is private.</span></span>
    
<span data-ttu-id="b9167-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="b9167-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="b9167-124">メッセージには、会社の機密情報が指定されます。</span><span class="sxs-lookup"><span data-stu-id="b9167-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b9167-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b9167-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9167-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b9167-126">Protocol specifications</span></span>

<span data-ttu-id="b9167-127">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9167-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9167-128">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9167-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9167-129">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9167-129">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9167-130">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="b9167-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9167-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b9167-131">Header files</span></span>

<span data-ttu-id="b9167-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9167-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9167-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9167-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9167-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9167-134">Mapitags.h</span></span>
  
> <span data-ttu-id="b9167-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b9167-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9167-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9167-136">See also</span></span>



[<span data-ttu-id="b9167-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9167-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9167-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9167-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9167-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b9167-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9167-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b9167-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

