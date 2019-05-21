---
title: RuleSet 要素 (RuleSets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: 図の検証ルール セットを表します。
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318915"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="63c1e-103">RuleSet 要素 (RuleSets_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="63c1e-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="63c1e-104">図の検証ルール セットを表します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-104">Represents one set of diagram validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63c1e-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="63c1e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63c1e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="63c1e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="63c1e-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="63c1e-107">RuleSet_Type complexType</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="63c1e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63c1e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="63c1e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="63c1e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="63c1e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="63c1e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="63c1e-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="63c1e-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="63c1e-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="63c1e-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63c1e-113">定義</span><span class="sxs-lookup"><span data-stu-id="63c1e-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63c1e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="63c1e-114">Elements and attributes</span></span>

<span data-ttu-id="63c1e-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63c1e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="63c1e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="63c1e-116">Parent elements</span></span>

|<span data-ttu-id="63c1e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="63c1e-117">**Element**</span></span>|<span data-ttu-id="63c1e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="63c1e-118">**Type**</span></span>|<span data-ttu-id="63c1e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="63c1e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63c1e-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="63c1e-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63c1e-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="63c1e-121">RuleSets_Type complexType</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63c1e-122">ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="63c1e-122">Includes a  ValidationRuleSet  object for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63c1e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="63c1e-123">Child elements</span></span>

|<span data-ttu-id="63c1e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="63c1e-124">**Element**</span></span>|<span data-ttu-id="63c1e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="63c1e-125">**Type**</span></span>|<span data-ttu-id="63c1e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="63c1e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63c1e-127">Rule</span><span class="sxs-lookup"><span data-stu-id="63c1e-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63c1e-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="63c1e-128">RuleType</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63c1e-129">図の検証ルールセット内の1つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="63c1e-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="63c1e-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63c1e-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="63c1e-131">RuleSetFlags_Type complexType</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63c1e-132">ルールセット プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="63c1e-133">属性</span><span class="sxs-lookup"><span data-stu-id="63c1e-133">Attributes</span></span>

|<span data-ttu-id="63c1e-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="63c1e-134">**Attribute**</span></span>|<span data-ttu-id="63c1e-135">**型**</span><span class="sxs-lookup"><span data-stu-id="63c1e-135">**Type**</span></span>|<span data-ttu-id="63c1e-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="63c1e-136">**Required**</span></span>|<span data-ttu-id="63c1e-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="63c1e-137">**Description**</span></span>|<span data-ttu-id="63c1e-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="63c1e-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63c1e-139">説明</span><span class="sxs-lookup"><span data-stu-id="63c1e-139">Description</span></span>  <br/> |<span data-ttu-id="63c1e-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="63c1e-140">xsd:string</span></span>  <br/> |<span data-ttu-id="63c1e-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="63c1e-141">optional</span></span>  <br/> |<span data-ttu-id="63c1e-142">検証ルールセットのユーザーインターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="63c1e-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="63c1e-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="63c1e-144">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="63c1e-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="63c1e-145">有効</span><span class="sxs-lookup"><span data-stu-id="63c1e-145">Enabled</span></span>  <br/> |<span data-ttu-id="63c1e-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="63c1e-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="63c1e-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="63c1e-147">optional</span></span>  <br/> |<span data-ttu-id="63c1e-148">現在のドキュメントで検証が実行される時に、指定された検証ルールセットの規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-148">Determines whether the rules in the  specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="63c1e-149">既定値は True です。</span><span class="sxs-lookup"><span data-stu-id="63c1e-149">Default is True.</span></span>  <br/> |<span data-ttu-id="63c1e-150">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="63c1e-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="63c1e-151">ID</span><span class="sxs-lookup"><span data-stu-id="63c1e-151">ID</span></span>  <br/> |<span data-ttu-id="63c1e-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63c1e-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63c1e-153">必須</span><span class="sxs-lookup"><span data-stu-id="63c1e-153">required</span></span>  <br/> |<span data-ttu-id="63c1e-154">検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="63c1e-155">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="63c1e-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63c1e-156">名前</span><span class="sxs-lookup"><span data-stu-id="63c1e-156">Name</span></span>  <br/> |<span data-ttu-id="63c1e-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="63c1e-157">xsd:string</span></span>  <br/> |<span data-ttu-id="63c1e-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="63c1e-158">optional</span></span>  <br/> |<span data-ttu-id="63c1e-159">検証ルール セットの局所名を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="63c1e-160">既定値は NameU 属性値です。</span><span class="sxs-lookup"><span data-stu-id="63c1e-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="63c1e-161">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="63c1e-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="63c1e-162">NameU</span><span class="sxs-lookup"><span data-stu-id="63c1e-162">NameU</span></span>  <br/> |<span data-ttu-id="63c1e-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="63c1e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="63c1e-164">必須</span><span class="sxs-lookup"><span data-stu-id="63c1e-164">required</span></span>  <br/> |<span data-ttu-id="63c1e-165">検証ルール セットのユニバーサル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c1e-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="63c1e-166">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="63c1e-166">Values of the xsd:string type.</span></span>  <br/> |
   

