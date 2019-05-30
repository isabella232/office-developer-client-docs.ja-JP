---
title: Rule 要素 (RuleSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルール セット内の1つの検証ルールを表します。
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358801"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="e31b3-103">Rule 要素 (RuleSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e31b3-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e31b3-104">図の検証ルール セット内の1つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e31b3-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="e31b3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e31b3-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e31b3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e31b3-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="e31b3-107">RuleType</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e31b3-108">**名詞空間**</span><span class="sxs-lookup"><span data-stu-id="e31b3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e31b3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e31b3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e31b3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e31b3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e31b3-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="e31b3-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="e31b3-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="e31b3-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e31b3-113">定義</span><span class="sxs-lookup"><span data-stu-id="e31b3-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e31b3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e31b3-114">Elements and attributes</span></span>

<span data-ttu-id="e31b3-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e31b3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e31b3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e31b3-116">Parent elements</span></span>

|<span data-ttu-id="e31b3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e31b3-117">**Element**</span></span>|<span data-ttu-id="e31b3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e31b3-118">**Type**</span></span>|<span data-ttu-id="e31b3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e31b3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e31b3-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="e31b3-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e31b3-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="e31b3-121">RuleSet_Type complexType</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e31b3-122">図の検証ルール セットの 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-122">Represents one set of diagram validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e31b3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e31b3-123">Child elements</span></span>

|<span data-ttu-id="e31b3-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e31b3-124">**Element**</span></span>|<span data-ttu-id="e31b3-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e31b3-125">**Type**</span></span>|<span data-ttu-id="e31b3-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e31b3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e31b3-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="e31b3-127">RuleFilter element</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e31b3-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="e31b3-128">RuleFilter_Type complexType</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e31b3-129">対象のオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-129">Gets or sets the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="e31b3-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="e31b3-130">RuleTest element</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e31b3-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="e31b3-131">RuleTest_Type complexType</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e31b3-132">対象のオブジェクトが検証ルールに準拠しているかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-132">Gets or sets the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e31b3-133">属性</span><span class="sxs-lookup"><span data-stu-id="e31b3-133">Attributes</span></span>

|<span data-ttu-id="e31b3-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="e31b3-134">**Attribute**</span></span>|<span data-ttu-id="e31b3-135">**型**</span><span class="sxs-lookup"><span data-stu-id="e31b3-135">**Type**</span></span>|<span data-ttu-id="e31b3-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="e31b3-136">**Required**</span></span>|<span data-ttu-id="e31b3-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="e31b3-137">**Description**</span></span>|<span data-ttu-id="e31b3-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e31b3-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e31b3-139">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="e31b3-139">Category</span></span>  <br/> |<span data-ttu-id="e31b3-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e31b3-140">xsd:string</span></span>  <br/> |<span data-ttu-id="e31b3-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="e31b3-141">optional</span></span>  <br/> |<span data-ttu-id="e31b3-142">[**問題**] ウィンドウの [カテゴリ] 列に表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-142">Represents the text displayed in the **Category** column of the  Issues window.</span></span> <span data-ttu-id="e31b3-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="e31b3-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="e31b3-144">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e31b3-145">説明</span><span class="sxs-lookup"><span data-stu-id="e31b3-145">Description</span></span>  <br/> |<span data-ttu-id="e31b3-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e31b3-146">xsd:string</span></span>  <br/> |<span data-ttu-id="e31b3-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="e31b3-147">optional</span></span>  <br/> |<span data-ttu-id="e31b3-148">ユーザーインターフェイスに表示される検証ルールの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-148">Specifies the description of the ValidationRuleSet object that appears in the user interface.</span></span> <span data-ttu-id="e31b3-149">既定値は "Unknown" です。</span><span class="sxs-lookup"><span data-stu-id="e31b3-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="e31b3-150">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e31b3-151">ID</span><span class="sxs-lookup"><span data-stu-id="e31b3-151">ID</span></span>  <br/> |<span data-ttu-id="e31b3-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e31b3-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e31b3-153">必須</span><span class="sxs-lookup"><span data-stu-id="e31b3-153">required</span></span>  <br/> |<span data-ttu-id="e31b3-154">検証ルールの一意識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-154">Specifies the unique identifier for the proxy.</span></span>  <br/> |<span data-ttu-id="e31b3-155">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e31b3-156">無視</span><span class="sxs-lookup"><span data-stu-id="e31b3-156">Ignored</span></span>  <br/> |<span data-ttu-id="e31b3-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e31b3-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e31b3-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="e31b3-158">optional</span></span>  <br/> |<span data-ttu-id="e31b3-159">検証ルールが現在無視されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-159">Determines whether the validation rule is currently ignored.</span></span> <span data-ttu-id="e31b3-160">既定値は False です。</span><span class="sxs-lookup"><span data-stu-id="e31b3-160">Default is False.</span></span>  <br/> |<span data-ttu-id="e31b3-161">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e31b3-162">NameU</span><span class="sxs-lookup"><span data-stu-id="e31b3-162">NameU</span></span>  <br/> |<span data-ttu-id="e31b3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e31b3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e31b3-164">必須</span><span class="sxs-lookup"><span data-stu-id="e31b3-164">required</span></span>  <br/> |<span data-ttu-id="e31b3-165">検証ルールのユニバーサル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-165">Specifies the name of the rule.</span></span>  <br/> |<span data-ttu-id="e31b3-166">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e31b3-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="e31b3-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="e31b3-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="e31b3-168">xsd:int</span></span>  <br/> |<span data-ttu-id="e31b3-169">省略可能</span><span class="sxs-lookup"><span data-stu-id="e31b3-169">optional</span></span>  <br/> |<span data-ttu-id="e31b3-170">検証ルールが適用されるオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="e31b3-170">Determines the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="e31b3-171">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="e31b3-171">Values of the xsd:int type.</span></span>  <br/> |
   

