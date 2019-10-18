---
title: RuleSet 要素 (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: 図の検証ルール セットの 1 つを表します。
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541639"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="f97fb-103">RuleSet 要素 (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f97fb-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f97fb-104">図の検証ルール セットの 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-104">Represents one set of diagram validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f97fb-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="f97fb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f97fb-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f97fb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f97fb-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="f97fb-107">RuleSet_Type complexType</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f97fb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f97fb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f97fb-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f97fb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f97fb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f97fb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f97fb-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="f97fb-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="f97fb-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="f97fb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f97fb-113">定義</span><span class="sxs-lookup"><span data-stu-id="f97fb-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f97fb-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f97fb-114">Elements and attributes</span></span>

<span data-ttu-id="f97fb-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f97fb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f97fb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f97fb-116">Parent elements</span></span>

|<span data-ttu-id="f97fb-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f97fb-117">**Element**</span></span>|<span data-ttu-id="f97fb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f97fb-118">**Type**</span></span>|<span data-ttu-id="f97fb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f97fb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f97fb-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="f97fb-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f97fb-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="f97fb-121">RuleSets_Type complexType</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f97fb-122">ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f97fb-122">Includes a  ValidationRuleSet  object for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f97fb-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f97fb-123">Child elements</span></span>

|<span data-ttu-id="f97fb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f97fb-124">**Element**</span></span>|<span data-ttu-id="f97fb-125">**型**</span><span class="sxs-lookup"><span data-stu-id="f97fb-125">**Type**</span></span>|<span data-ttu-id="f97fb-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="f97fb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f97fb-127">Rule</span><span class="sxs-lookup"><span data-stu-id="f97fb-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f97fb-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="f97fb-128">RuleType</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f97fb-129">図の検証ルールセット内の1つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="f97fb-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="f97fb-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f97fb-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="f97fb-131">RuleSetFlags_Type complexType</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f97fb-132">ルールセット プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f97fb-133">属性</span><span class="sxs-lookup"><span data-stu-id="f97fb-133">Attributes</span></span>

|<span data-ttu-id="f97fb-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="f97fb-134">**Attribute**</span></span>|<span data-ttu-id="f97fb-135">**型**</span><span class="sxs-lookup"><span data-stu-id="f97fb-135">**Type**</span></span>|<span data-ttu-id="f97fb-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="f97fb-136">**Required**</span></span>|<span data-ttu-id="f97fb-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="f97fb-137">**Description**</span></span>|<span data-ttu-id="f97fb-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="f97fb-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f97fb-139">説明</span><span class="sxs-lookup"><span data-stu-id="f97fb-139">Description</span></span>  <br/> |<span data-ttu-id="f97fb-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f97fb-140">xsd:string</span></span>  <br/> |<span data-ttu-id="f97fb-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="f97fb-141">optional</span></span>  <br/> |<span data-ttu-id="f97fb-142">検証ルールセットのユーザーインターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="f97fb-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f97fb-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="f97fb-144">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f97fb-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f97fb-145">有効</span><span class="sxs-lookup"><span data-stu-id="f97fb-145">Enabled</span></span>  <br/> |<span data-ttu-id="f97fb-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f97fb-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f97fb-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="f97fb-147">optional</span></span>  <br/> |<span data-ttu-id="f97fb-148">現在のドキュメントで検証が実行される時に、指定された検証ルールセットの規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-148">Determines whether the rules in the  specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="f97fb-149">既定値は True です。</span><span class="sxs-lookup"><span data-stu-id="f97fb-149">Default is True.</span></span>  <br/> |<span data-ttu-id="f97fb-150">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="f97fb-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f97fb-151">ID</span><span class="sxs-lookup"><span data-stu-id="f97fb-151">ID</span></span>  <br/> |<span data-ttu-id="f97fb-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f97fb-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f97fb-153">必須</span><span class="sxs-lookup"><span data-stu-id="f97fb-153">required</span></span>  <br/> |<span data-ttu-id="f97fb-154">検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f97fb-155">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="f97fb-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f97fb-156">名前</span><span class="sxs-lookup"><span data-stu-id="f97fb-156">Name</span></span>  <br/> |<span data-ttu-id="f97fb-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f97fb-157">xsd:string</span></span>  <br/> |<span data-ttu-id="f97fb-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="f97fb-158">optional</span></span>  <br/> |<span data-ttu-id="f97fb-159">検証ルール セットの局所名を指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="f97fb-160">既定値は NameU 属性値です。</span><span class="sxs-lookup"><span data-stu-id="f97fb-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="f97fb-161">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f97fb-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f97fb-162">NameU</span><span class="sxs-lookup"><span data-stu-id="f97fb-162">NameU</span></span>  <br/> |<span data-ttu-id="f97fb-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f97fb-163">xsd:string</span></span>  <br/> |<span data-ttu-id="f97fb-164">必須</span><span class="sxs-lookup"><span data-stu-id="f97fb-164">required</span></span>  <br/> |<span data-ttu-id="f97fb-165">検証ルール セットのユニバーサル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="f97fb-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f97fb-166">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f97fb-166">Values of the xsd:string type.</span></span>  <br/> |
   

