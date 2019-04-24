---
title: PidTagRuleCondition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleCondition
api_type:
- COM
ms.assetid: 8a11e846-c62f-4c06-876f-94623d50cc3b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b513bc5ff6b95b26a96e36a4d04a49737cf6216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359508"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="c3e14-103">PidTagRuleCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3e14-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="c3e14-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3e14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3e14-105">ルールを評価するときに使用する条件を示します。</span><span class="sxs-lookup"><span data-stu-id="c3e14-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3e14-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c3e14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c3e14-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="c3e14-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="c3e14-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c3e14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c3e14-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="c3e14-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="c3e14-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c3e14-110">Data type:</span></span>  <br/> |<span data-ttu-id="c3e14-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="c3e14-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="c3e14-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c3e14-112">Area:</span></span>  <br/> |<span data-ttu-id="c3e14-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="c3e14-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3e14-114">解説</span><span class="sxs-lookup"><span data-stu-id="c3e14-114">Remarks</span></span>

<span data-ttu-id="c3e14-115">条件は**制限**として表され、 **PropertyValue**バッファーには、 [[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定されたようにパッケージ化された**制限**構造が格納されます。</span><span class="sxs-lookup"><span data-stu-id="c3e14-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c3e14-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c3e14-116">MFCMAPI reference</span></span>

<span data-ttu-id="c3e14-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3e14-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c3e14-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c3e14-118">**File**</span></span>|<span data-ttu-id="c3e14-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="c3e14-119">**Function**</span></span>|<span data-ttu-id="c3e14-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c3e14-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c3e14-121">importprocs</span><span class="sxs-lookup"><span data-stu-id="c3e14-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="c3e14-122">propcopymore、hrcopyrestriction</span><span class="sxs-lookup"><span data-stu-id="c3e14-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="c3e14-123">これらの関数は、別のプロパティにコピーする目的で**PT_SRESTRICTION**プロパティを解析する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c3e14-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c3e14-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c3e14-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c3e14-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c3e14-125">Protocol specifications</span></span>

<span data-ttu-id="c3e14-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3e14-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3e14-127">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3e14-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c3e14-128">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3e14-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3e14-129">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="c3e14-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="c3e14-130">[[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c3e14-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c3e14-131">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="c3e14-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c3e14-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c3e14-132">Header files</span></span>

<span data-ttu-id="c3e14-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3e14-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c3e14-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3e14-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c3e14-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c3e14-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c3e14-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3e14-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3e14-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3e14-137">See also</span></span>



[<span data-ttu-id="c3e14-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c3e14-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c3e14-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c3e14-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c3e14-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3e14-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c3e14-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c3e14-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

