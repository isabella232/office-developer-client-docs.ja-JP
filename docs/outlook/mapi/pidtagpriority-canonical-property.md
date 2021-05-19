---
title: PidTagPriority 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339432"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="1f3f4-103">PidTagPriority 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f3f4-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="1f3f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f3f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f3f4-105">メッセージの相対的な優先度を格納します。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f3f4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1f3f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f3f4-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="1f3f4-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="1f3f4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1f3f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f3f4-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="1f3f4-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="1f3f4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1f3f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f3f4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f3f4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f3f4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1f3f4-112">Area:</span></span>  <br/> |<span data-ttu-id="1f3f4-113">メール</span><span class="sxs-lookup"><span data-stu-id="1f3f4-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f3f4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1f3f4-114">Remarks</span></span>

<span data-ttu-id="1f3f4-115">このプロパティと **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) プロパティは混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="1f3f4-116">重要度はユーザーに値を示し、優先度はメッセージをメッセージング システム ソフトウェアによって送信する順序または速度を示します。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="1f3f4-117">優先度が高いほど、通常はコストが高くなります。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="1f3f4-118">重要度が高いほど、通常、ユーザー インターフェイスによって別の表示に関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="1f3f4-119">レポート メッセージの優先度は、報告される元のメッセージの優先度と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="1f3f4-120">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="1f3f4-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="1f3f4-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="1f3f4-122">メッセージは緊急ではありません。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-122">The message is not urgent.</span></span>
    
<span data-ttu-id="1f3f4-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="1f3f4-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="1f3f4-124">メッセージの優先度は通常です。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-124">The message has normal priority.</span></span>
    
<span data-ttu-id="1f3f4-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="1f3f4-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="1f3f4-126">メッセージは緊急です。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1f3f4-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1f3f4-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f3f4-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1f3f4-128">Protocol specifications</span></span>

<span data-ttu-id="1f3f4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f3f4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f3f4-130">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f3f4-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f3f4-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f3f4-132">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f3f4-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1f3f4-133">Header files</span></span>

<span data-ttu-id="1f3f4-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f3f4-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f3f4-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f3f4-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f3f4-136">Mapitags.h</span></span>
  
> <span data-ttu-id="1f3f4-137">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1f3f4-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f3f4-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f3f4-138">See also</span></span>



[<span data-ttu-id="1f3f4-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1f3f4-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f3f4-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f3f4-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f3f4-141">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1f3f4-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f3f4-142">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1f3f4-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

