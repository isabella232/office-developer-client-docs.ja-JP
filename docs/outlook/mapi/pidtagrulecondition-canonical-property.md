---
title: PidTagRuleCondition の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f4eae388d51b0428d508a675681fa4cd1d94e46f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803405"
---
# <a name="pidtagrulecondition-canonical-property"></a><span data-ttu-id="bd195-103">PidTagRuleCondition の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bd195-103">PidTagRuleCondition Canonical Property</span></span>

  
  
<span data-ttu-id="bd195-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd195-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd195-105">ルールを評価するときに使用する条件。</span><span class="sxs-lookup"><span data-stu-id="bd195-105">The condition used when you evaluate the rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd195-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bd195-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd195-107">PR_RULE_CONDITION</span><span class="sxs-lookup"><span data-stu-id="bd195-107">PR_RULE_CONDITION</span></span>  <br/> |
|<span data-ttu-id="bd195-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bd195-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bd195-109">0x6679</span><span class="sxs-lookup"><span data-stu-id="bd195-109">0x6679</span></span>  <br/> |
|<span data-ttu-id="bd195-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bd195-110">Data type:</span></span>  <br/> |<span data-ttu-id="bd195-111">PT_SRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="bd195-111">PT_SRESTRICTION</span></span>  <br/> |
|<span data-ttu-id="bd195-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bd195-112">Area:</span></span>  <br/> |<span data-ttu-id="bd195-113">サーバー側のルール</span><span class="sxs-lookup"><span data-stu-id="bd195-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd195-114">備考</span><span class="sxs-lookup"><span data-stu-id="bd195-114">Remarks</span></span>

<span data-ttu-id="bd195-115">条件が**制限**として表され、**プロパティ値**のバッファーには、 [[MS OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定されているパッケージ**の制限**の構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd195-115">The condition is expressed as a **Restriction** and the **PropertyValue** buffer contains the **Restriction** structure packaged as specified in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bd195-116">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="bd195-116">MFCMAPI reference</span></span>

<span data-ttu-id="bd195-117">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="bd195-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bd195-118">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="bd195-118">**File**</span></span>|<span data-ttu-id="bd195-119">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="bd195-119">**Function**</span></span>|<span data-ttu-id="bd195-120">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="bd195-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd195-121">ImportProcs.cpp</span><span class="sxs-lookup"><span data-stu-id="bd195-121">ImportProcs.cpp</span></span>  <br/> |<span data-ttu-id="bd195-122">PropCopyMore、HrCopyRestriction</span><span class="sxs-lookup"><span data-stu-id="bd195-122">PropCopyMore, HrCopyRestriction</span></span>  <br/> |<span data-ttu-id="bd195-123">これらの関数は、別のプロパティにコピーするために**PT_SRESTRICTION**プロパティを解析する方法をデモンストレーションします。</span><span class="sxs-lookup"><span data-stu-id="bd195-123">These functions demonstrate how to parse a **PT_SRESTRICTION** property for the purposes of copying to another property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bd195-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bd195-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd195-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bd195-125">Protocol specifications</span></span>

<span data-ttu-id="bd195-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd195-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd195-127">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd195-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd195-128">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd195-128">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd195-129">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="bd195-129">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="bd195-130">[[MS OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd195-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd195-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="bd195-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd195-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bd195-132">Header files</span></span>

<span data-ttu-id="bd195-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd195-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd195-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bd195-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="bd195-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bd195-135">Mapitags.h</span></span>
  
> <span data-ttu-id="bd195-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd195-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd195-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd195-137">See also</span></span>



[<span data-ttu-id="bd195-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd195-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd195-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bd195-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd195-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bd195-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd195-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bd195-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

