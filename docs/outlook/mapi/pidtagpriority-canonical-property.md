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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385453"
---
# <a name="pidtagpriority-canonical-property"></a><span data-ttu-id="b46a0-103">PidTagPriority 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b46a0-103">PidTagPriority Canonical Property</span></span>

  
  
<span data-ttu-id="b46a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b46a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b46a0-105">メッセージの相対的な優先順位が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b46a0-105">Contains the relative priority of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b46a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b46a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b46a0-107">PR_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="b46a0-107">PR_PRIORITY</span></span>  <br/> |
|<span data-ttu-id="b46a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b46a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b46a0-109">0x0026</span><span class="sxs-lookup"><span data-stu-id="b46a0-109">0x0026</span></span>  <br/> |
|<span data-ttu-id="b46a0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b46a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="b46a0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b46a0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b46a0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b46a0-112">Area:</span></span>  <br/> |<span data-ttu-id="b46a0-113">メール</span><span class="sxs-lookup"><span data-stu-id="b46a0-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b46a0-114">備考</span><span class="sxs-lookup"><span data-stu-id="b46a0-114">Remarks</span></span>

<span data-ttu-id="b46a0-115">このプロパティは、 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) は混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="b46a0-115">This property and the **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="b46a0-116">重要性は、優先順位は、順序や速度のメッセージがメッセージング システムのソフトウェアが送信することを示します。 ユーザーに値を示します。</span><span class="sxs-lookup"><span data-stu-id="b46a0-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="b46a0-117">高い優先度は、通常より高いコストを示します。</span><span class="sxs-lookup"><span data-stu-id="b46a0-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="b46a0-118">重要度が高く通常は、ユーザー インターフェイスで別のディスプレイに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="b46a0-118">Higher importance usually is associated with a different display by the user interface.</span></span>
  
<span data-ttu-id="b46a0-119">レポート メッセージの優先度は、報告されている元のメッセージの優先順位と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b46a0-119">The priority of a report message should be the same as the priority of the original message being reported.</span></span>
  
<span data-ttu-id="b46a0-120">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b46a0-120">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="b46a0-121">PRIO_NONURGENT</span><span class="sxs-lookup"><span data-stu-id="b46a0-121">PRIO_NONURGENT</span></span> 
  
> <span data-ttu-id="b46a0-122">メッセージが緊急ではありません。</span><span class="sxs-lookup"><span data-stu-id="b46a0-122">The message is not urgent.</span></span>
    
<span data-ttu-id="b46a0-123">PRIO_NORMAL</span><span class="sxs-lookup"><span data-stu-id="b46a0-123">PRIO_NORMAL</span></span> 
  
> <span data-ttu-id="b46a0-124">メッセージには、通常の優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="b46a0-124">The message has normal priority.</span></span>
    
<span data-ttu-id="b46a0-125">PRIO_URGENT</span><span class="sxs-lookup"><span data-stu-id="b46a0-125">PRIO_URGENT</span></span> 
  
> <span data-ttu-id="b46a0-126">メッセージは、緊急です。</span><span class="sxs-lookup"><span data-stu-id="b46a0-126">The message is urgent.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b46a0-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b46a0-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b46a0-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b46a0-128">Protocol specifications</span></span>

<span data-ttu-id="b46a0-129">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b46a0-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b46a0-130">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b46a0-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b46a0-131">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b46a0-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b46a0-132">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="b46a0-132">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b46a0-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b46a0-133">Header files</span></span>

<span data-ttu-id="b46a0-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b46a0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b46a0-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b46a0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b46a0-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b46a0-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b46a0-137">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b46a0-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b46a0-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="b46a0-138">See also</span></span>



[<span data-ttu-id="b46a0-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b46a0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b46a0-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b46a0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b46a0-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b46a0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b46a0-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b46a0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

