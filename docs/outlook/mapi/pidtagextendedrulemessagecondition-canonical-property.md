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
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401658"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="d9cdf-103">PidTagExtendedRuleMessageCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9cdf-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="d9cdf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9cdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9cdf-105">拡張ルールの条件の内で含まれている任意の名前付きプロパティに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9cdf-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d9cdf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9cdf-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="d9cdf-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="d9cdf-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d9cdf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9cdf-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="d9cdf-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="d9cdf-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d9cdf-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9cdf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d9cdf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d9cdf-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d9cdf-112">Area:</span></span>  <br/> |<span data-ttu-id="d9cdf-113">ルール</span><span class="sxs-lookup"><span data-stu-id="d9cdf-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9cdf-114">備考</span><span class="sxs-lookup"><span data-stu-id="d9cdf-114">Remarks</span></span>

<span data-ttu-id="d9cdf-115">このプロパティは、FAI メッセージを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="d9cdf-116">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) と同じ役目を果たしますが、使用する名前付きプロパティに関する追加情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="d9cdf-117">この条件のプロパティの値の任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="d9cdf-118">このバイナリのプロパティの形式については、 [[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9cdf-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d9cdf-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9cdf-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d9cdf-120">Protocol specifications</span></span>

<span data-ttu-id="d9cdf-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9cdf-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9cdf-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9cdf-123">[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9cdf-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9cdf-124">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9cdf-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d9cdf-125">Header files</span></span>

<span data-ttu-id="d9cdf-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9cdf-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9cdf-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9cdf-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d9cdf-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d9cdf-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9cdf-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9cdf-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9cdf-130">See also</span></span>



[<span data-ttu-id="d9cdf-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9cdf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9cdf-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9cdf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9cdf-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9cdf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9cdf-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9cdf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

