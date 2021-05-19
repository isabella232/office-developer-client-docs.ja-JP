---
title: Rule 要素 (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルールセット内の1つの検証ルールを表します。
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541709"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a><span data-ttu-id="9102b-103">Rule 要素 (RuleSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9102b-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="9102b-104">図の検証ルールセット内の1つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="9102b-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9102b-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="9102b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9102b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9102b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9102b-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9102b-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9102b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9102b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9102b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9102b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9102b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9102b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9102b-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="9102b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9102b-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="9102b-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9102b-113">定義</span><span class="sxs-lookup"><span data-stu-id="9102b-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9102b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9102b-114">Elements and attributes</span></span>

<span data-ttu-id="9102b-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9102b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9102b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9102b-116">Parent elements</span></span>

|<span data-ttu-id="9102b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9102b-117">**Element**</span></span>|<span data-ttu-id="9102b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9102b-118">**Type**</span></span>|<span data-ttu-id="9102b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9102b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9102b-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="9102b-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9102b-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9102b-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9102b-122">図の検証ルール セットの 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="9102b-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9102b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9102b-123">Child elements</span></span>

|<span data-ttu-id="9102b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9102b-124">**Element**</span></span>|<span data-ttu-id="9102b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9102b-125">**Type**</span></span>|<span data-ttu-id="9102b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9102b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9102b-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="9102b-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9102b-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="9102b-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9102b-129">検証ルールをターゲット オブジェクトに適用するかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="9102b-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="9102b-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9102b-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="9102b-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9102b-132">ターゲット オブジェクトが検証ルールを満たすかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9102b-133">属性</span><span class="sxs-lookup"><span data-stu-id="9102b-133">Attributes</span></span>

|<span data-ttu-id="9102b-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="9102b-134">**Attribute**</span></span>|<span data-ttu-id="9102b-135">**型**</span><span class="sxs-lookup"><span data-stu-id="9102b-135">**Type**</span></span>|<span data-ttu-id="9102b-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="9102b-136">**Required**</span></span>|<span data-ttu-id="9102b-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="9102b-137">**Description**</span></span>|<span data-ttu-id="9102b-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9102b-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9102b-139">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="9102b-139">Category</span></span>  <br/> |<span data-ttu-id="9102b-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9102b-140">xsd:string</span></span>  <br/> |<span data-ttu-id="9102b-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="9102b-141">optional</span></span>  <br/> |<span data-ttu-id="9102b-142">[問題] ウィンドウの [カテゴリ] **列** に表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="9102b-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9102b-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="9102b-144">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9102b-145">説明</span><span class="sxs-lookup"><span data-stu-id="9102b-145">Description</span></span>  <br/> |<span data-ttu-id="9102b-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9102b-146">xsd:string</span></span>  <br/> |<span data-ttu-id="9102b-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="9102b-147">optional</span></span>  <br/> |<span data-ttu-id="9102b-148">ユーザー インターフェイスに表示される検証ルールの説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="9102b-149">既定値は "不明" です。</span><span class="sxs-lookup"><span data-stu-id="9102b-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="9102b-150">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9102b-151">ID</span><span class="sxs-lookup"><span data-stu-id="9102b-151">ID</span></span>  <br/> |<span data-ttu-id="9102b-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9102b-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9102b-153">必須</span><span class="sxs-lookup"><span data-stu-id="9102b-153">required</span></span>  <br/> |<span data-ttu-id="9102b-154">検証ルールの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="9102b-155">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9102b-156">無視</span><span class="sxs-lookup"><span data-stu-id="9102b-156">Ignored</span></span>  <br/> |<span data-ttu-id="9102b-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9102b-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9102b-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="9102b-158">optional</span></span>  <br/> |<span data-ttu-id="9102b-159">検証ルールが現在無視されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="9102b-160">既定値は False です。</span><span class="sxs-lookup"><span data-stu-id="9102b-160">Default is False.</span></span>  <br/> |<span data-ttu-id="9102b-161">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9102b-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9102b-162">NameU</span></span>  <br/> |<span data-ttu-id="9102b-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9102b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9102b-164">必須</span><span class="sxs-lookup"><span data-stu-id="9102b-164">required</span></span>  <br/> |<span data-ttu-id="9102b-165">検証ルールの汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="9102b-166">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9102b-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="9102b-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="9102b-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="9102b-168">xsd:int</span></span>  <br/> |<span data-ttu-id="9102b-169">省略可能</span><span class="sxs-lookup"><span data-stu-id="9102b-169">optional</span></span>  <br/> |<span data-ttu-id="9102b-170">検証ルールが適用されるオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="9102b-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="9102b-171">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="9102b-171">Values of the xsd:int type.</span></span>  <br/> |
   

