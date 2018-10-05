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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389597"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="4b99e-103">PidTagRuleCondition 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b99e-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="4b99e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b99e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b99e-105">ルールを評価するときに使用する条件。</span><span class="sxs-lookup"><span data-stu-id="4b99e-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b99e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4b99e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b99e-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="4b99e-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="4b99e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4b99e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b99e-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="4b99e-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="4b99e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4b99e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b99e-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="4b99e-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="4b99e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4b99e-112">Area:</span></span>  <br/> |<span data-ttu-id="4b99e-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="4b99e-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b99e-114">備考</span><span class="sxs-lookup"><span data-stu-id="4b99e-114">Remarks</span></span>

<span data-ttu-id="4b99e-115">条件が**制限**として表され、**プロパティ値**のバッファーには、 [[MS OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定されているパッケージ**の制限**の構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b99e-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4b99e-116">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="4b99e-116">MFCMAPI reference</span></span>

<span data-ttu-id="4b99e-117">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b99e-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4b99e-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="4b99e-118">**File**</span></span>|<span data-ttu-id="4b99e-119">**関数**</span><span class="sxs-lookup"><span data-stu-id="4b99e-119">**Function**</span></span>|<span data-ttu-id="4b99e-120">**コメント**</span><span class="sxs-lookup"><span data-stu-id="4b99e-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b99e-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="4b99e-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="4b99e-122">PropCopyMore、HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="4b99e-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="4b99e-123">これらの関数は、別のプロパティにコピーするために**PT_SRESTRICTION**プロパティを解析する方法をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="4b99e-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4b99e-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4b99e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b99e-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4b99e-125">Protocol specifications</span></span>

<span data-ttu-id="4b99e-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b99e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b99e-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b99e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b99e-128">[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b99e-128">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b99e-129">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="4b99e-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="4b99e-130">[[MS OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b99e-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b99e-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="4b99e-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b99e-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4b99e-132">Header files</span></span>

<span data-ttu-id="4b99e-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b99e-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b99e-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b99e-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b99e-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4b99e-135">Mapitags.h</span></span>
  
> <span data-ttu-id="4b99e-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b99e-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b99e-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b99e-137">See also</span></span>



[<span data-ttu-id="4b99e-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b99e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b99e-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4b99e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b99e-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4b99e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b99e-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4b99e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

