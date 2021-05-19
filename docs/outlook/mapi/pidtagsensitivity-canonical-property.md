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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342505"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="8e553-103">PidTagSensitivity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e553-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="8e553-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e553-105">メッセージの送信者のメッセージの感度に関する意見を示す値を含む。</span><span class="sxs-lookup"><span data-stu-id="8e553-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e553-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8e553-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e553-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="8e553-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="8e553-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8e553-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e553-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="8e553-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="8e553-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8e553-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e553-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8e553-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8e553-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8e553-112">Area:</span></span>  <br/> |<span data-ttu-id="8e553-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="8e553-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e553-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8e553-114">Remarks</span></span>

<span data-ttu-id="8e553-115">メッセージ オブジェクトでこのプロパティを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e553-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="8e553-116">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8e553-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="8e553-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="8e553-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="8e553-118">メッセージに特別な区別はありません。</span><span class="sxs-lookup"><span data-stu-id="8e553-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="8e553-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="8e553-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="8e553-120">メッセージは個人用です。</span><span class="sxs-lookup"><span data-stu-id="8e553-120">The message is personal.</span></span>
    
<span data-ttu-id="8e553-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="8e553-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="8e553-122">メッセージはプライベートです。</span><span class="sxs-lookup"><span data-stu-id="8e553-122">The message is private.</span></span>
    
<span data-ttu-id="8e553-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="8e553-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="8e553-124">メッセージは、会社の機密として指定されます。</span><span class="sxs-lookup"><span data-stu-id="8e553-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8e553-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8e553-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e553-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8e553-126">Protocol specifications</span></span>

<span data-ttu-id="8e553-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e553-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e553-128">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="8e553-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e553-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e553-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e553-130">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8e553-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e553-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8e553-131">Header files</span></span>

<span data-ttu-id="8e553-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e553-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e553-133">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8e553-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e553-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8e553-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8e553-135">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8e553-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e553-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e553-136">See also</span></span>



[<span data-ttu-id="8e553-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8e553-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e553-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e553-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e553-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8e553-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e553-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8e553-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

