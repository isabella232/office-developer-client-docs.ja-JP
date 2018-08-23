---
title: PidTagExtendedRuleMessageCondition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 92008a387bb0130207af012df209a3aa6881d40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593173"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="e9c1d-103">PidTagExtendedRuleMessageCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9c1d-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="e9c1d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9c1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9c1d-105">拡張ルールの条件の内で含まれている任意の名前付きプロパティに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9c1d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e9c1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9c1d-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="e9c1d-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="e9c1d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e9c1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9c1d-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="e9c1d-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="e9c1d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e9c1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9c1d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9c1d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9c1d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e9c1d-112">Area:</span></span>  <br/> |<span data-ttu-id="e9c1d-113">Rules</span><span class="sxs-lookup"><span data-stu-id="e9c1d-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9c1d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e9c1d-114">Remarks</span></span>

<span data-ttu-id="e9c1d-115">このプロパティは、FAI メッセージを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="e9c1d-116">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) と同じ役目を果たしますが、使用する名前付きプロパティに関する追加情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="e9c1d-117">この条件のプロパティの値の任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="e9c1d-118">このバイナリのプロパティの形式については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-118">For information about the format of this binary property, see [[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9c1d-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e9c1d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9c1d-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e9c1d-120">Protocol specifications</span></span>

<span data-ttu-id="e9c1d-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9c1d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9c1d-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9c1d-123">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9c1d-123">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9c1d-124">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9c1d-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e9c1d-125">Header files</span></span>

<span data-ttu-id="e9c1d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9c1d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9c1d-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9c1d-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9c1d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e9c1d-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9c1d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9c1d-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9c1d-130">See also</span></span>



[<span data-ttu-id="e9c1d-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9c1d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9c1d-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e9c1d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9c1d-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9c1d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9c1d-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e9c1d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

