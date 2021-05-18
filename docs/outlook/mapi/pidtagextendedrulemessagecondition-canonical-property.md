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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316332"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a><span data-ttu-id="bf65e-103">PidTagExtendedRuleMessageCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf65e-103">PidTagExtendedRuleMessageCondition Canonical Property</span></span>

  
  
<span data-ttu-id="bf65e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf65e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf65e-105">拡張ルール条件の内部に含まれる名前付きプロパティに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bf65e-105">Contains information about any named properties that are contained inside of extended rule conditions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf65e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bf65e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf65e-107">PR_EXTENDED_RULE_MSG_CONDITION</span><span class="sxs-lookup"><span data-stu-id="bf65e-107">PR_EXTENDED_RULE_MSG_CONDITION</span></span>  <br/> |
|<span data-ttu-id="bf65e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bf65e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf65e-109">0x0E9A</span><span class="sxs-lookup"><span data-stu-id="bf65e-109">0x0E9A</span></span>  <br/> |
|<span data-ttu-id="bf65e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bf65e-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf65e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bf65e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bf65e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bf65e-112">Area:</span></span>  <br/> |<span data-ttu-id="bf65e-113">ルール</span><span class="sxs-lookup"><span data-stu-id="bf65e-113">Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf65e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bf65e-114">Remarks</span></span>

<span data-ttu-id="bf65e-115">このプロパティは、FAI メッセージで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf65e-115">This property must be set on an FAI message.</span></span> <span data-ttu-id="bf65e-116">このプロパティは、PR_RULE_CONDITION **(** [PidTagRuleCondition)](pidtagrulecondition-canonical-property.md)と同じ目的を提供しますが、使用される名前付きプロパティに関する追加情報が含まれている。</span><span class="sxs-lookup"><span data-stu-id="bf65e-116">It serves the same purpose as **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)), but contains additional information about the named properties used.</span></span> <span data-ttu-id="bf65e-117">この条件プロパティ値の任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf65e-117">All string values contained in any part of this condition property value must be in Unicode format.</span></span>
  
<span data-ttu-id="bf65e-118">このバイナリ プロパティの形式については [、「[MS-OXORULE] 」を参照してください](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="bf65e-118">For information about the format of this binary property, see [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bf65e-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bf65e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf65e-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bf65e-120">Protocol specifications</span></span>

<span data-ttu-id="bf65e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf65e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf65e-122">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="bf65e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf65e-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf65e-123">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf65e-124">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="bf65e-124">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf65e-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bf65e-125">Header files</span></span>

<span data-ttu-id="bf65e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf65e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf65e-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bf65e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf65e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bf65e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="bf65e-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="bf65e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf65e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf65e-130">See also</span></span>



[<span data-ttu-id="bf65e-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bf65e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf65e-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bf65e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf65e-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf65e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf65e-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bf65e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

