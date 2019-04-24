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
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342505"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="0d985-103">PidTagSensitivity 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d985-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="0d985-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d985-105">メッセージの送信者によるメッセージの秘密度を示す値を格納します。</span><span class="sxs-lookup"><span data-stu-id="0d985-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d985-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0d985-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d985-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="0d985-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="0d985-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0d985-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d985-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="0d985-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="0d985-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0d985-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d985-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0d985-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0d985-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0d985-112">Area:</span></span>  <br/> |<span data-ttu-id="0d985-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="0d985-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d985-114">解説</span><span class="sxs-lookup"><span data-stu-id="0d985-114">Remarks</span></span>

<span data-ttu-id="0d985-115">このプロパティは、メッセージオブジェクトに公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0d985-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="0d985-116">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0d985-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="0d985-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="0d985-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="0d985-118">メッセージには特別な秘密度がありません。</span><span class="sxs-lookup"><span data-stu-id="0d985-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="0d985-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="0d985-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="0d985-120">メッセージが個人である。</span><span class="sxs-lookup"><span data-stu-id="0d985-120">The message is personal.</span></span>
    
<span data-ttu-id="0d985-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="0d985-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="0d985-122">メッセージはプライベートです。</span><span class="sxs-lookup"><span data-stu-id="0d985-122">The message is private.</span></span>
    
<span data-ttu-id="0d985-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="0d985-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="0d985-124">このメッセージは会社の機密と指定されています。</span><span class="sxs-lookup"><span data-stu-id="0d985-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0d985-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0d985-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d985-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0d985-126">Protocol specifications</span></span>

<span data-ttu-id="0d985-127">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d985-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d985-128">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d985-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d985-129">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d985-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d985-130">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="0d985-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d985-131">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0d985-131">Header files</span></span>

<span data-ttu-id="0d985-132">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d985-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d985-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d985-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d985-134">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0d985-134">Mapitags.h</span></span>
  
> <span data-ttu-id="0d985-135">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d985-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d985-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d985-136">See also</span></span>



[<span data-ttu-id="0d985-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0d985-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d985-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d985-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d985-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0d985-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d985-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0d985-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

