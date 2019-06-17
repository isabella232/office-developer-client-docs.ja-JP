---
title: Rule 要素 (RuleSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルール セットに含まれる 1 つの検証ルールを表します。
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541709"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="8de39-103">Rule 要素 (RuleSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8de39-103">Rule element (RuleSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8de39-104">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="8de39-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8de39-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8de39-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8de39-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8de39-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8de39-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="8de39-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8de39-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8de39-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8de39-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8de39-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8de39-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8de39-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8de39-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8de39-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8de39-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="8de39-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8de39-113">定義</span><span class="sxs-lookup"><span data-stu-id="8de39-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8de39-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8de39-114">Elements and attributes</span></span>

<span data-ttu-id="8de39-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8de39-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8de39-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8de39-116">Parent elements</span></span>

|<span data-ttu-id="8de39-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8de39-117">**Element**</span></span>|<span data-ttu-id="8de39-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8de39-118">**Type**</span></span>|<span data-ttu-id="8de39-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8de39-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8de39-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="8de39-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8de39-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="8de39-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8de39-122">1組のダイアグラム検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="8de39-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8de39-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8de39-123">Child elements</span></span>

|<span data-ttu-id="8de39-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8de39-124">**Element**</span></span>|<span data-ttu-id="8de39-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8de39-125">**Type**</span></span>|<span data-ttu-id="8de39-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8de39-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8de39-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="8de39-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8de39-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="8de39-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8de39-129">ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="8de39-130">ルール</span><span class="sxs-lookup"><span data-stu-id="8de39-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8de39-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="8de39-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8de39-132">ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8de39-133">属性</span><span class="sxs-lookup"><span data-stu-id="8de39-133">Attributes</span></span>

|<span data-ttu-id="8de39-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="8de39-134">**Attribute**</span></span>|<span data-ttu-id="8de39-135">**型**</span><span class="sxs-lookup"><span data-stu-id="8de39-135">**Type**</span></span>|<span data-ttu-id="8de39-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="8de39-136">**Required**</span></span>|<span data-ttu-id="8de39-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="8de39-137">**Description**</span></span>|<span data-ttu-id="8de39-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8de39-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8de39-139">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="8de39-139">Category</span></span>  <br/> |<span data-ttu-id="8de39-140">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8de39-140">xsd:string</span></span>  <br/> |<span data-ttu-id="8de39-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="8de39-141">optional</span></span>  <br/> |<span data-ttu-id="8de39-142">[問題] ウィンドウの [**カテゴリ**] 列に表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="8de39-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="8de39-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="8de39-144">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8de39-145">説明</span><span class="sxs-lookup"><span data-stu-id="8de39-145">Description</span></span>  <br/> |<span data-ttu-id="8de39-146">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8de39-146">xsd:string</span></span>  <br/> |<span data-ttu-id="8de39-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="8de39-147">optional</span></span>  <br/> |<span data-ttu-id="8de39-148">ユーザーインターフェイスに表示される入力規則の説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="8de39-149">既定値は "Unknown" です。</span><span class="sxs-lookup"><span data-stu-id="8de39-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="8de39-150">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8de39-151">ID</span><span class="sxs-lookup"><span data-stu-id="8de39-151">ID</span></span>  <br/> |<span data-ttu-id="8de39-152">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="8de39-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8de39-153">必須</span><span class="sxs-lookup"><span data-stu-id="8de39-153">required</span></span>  <br/> |<span data-ttu-id="8de39-154">入力規則の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="8de39-155">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8de39-156">Ignored</span><span class="sxs-lookup"><span data-stu-id="8de39-156">Ignored</span></span>  <br/> |<span data-ttu-id="8de39-157">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="8de39-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8de39-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="8de39-158">optional</span></span>  <br/> |<span data-ttu-id="8de39-159">検証ルールが現在無視されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="8de39-160">既定値は False です。</span><span class="sxs-lookup"><span data-stu-id="8de39-160">Default is False.</span></span>  <br/> |<span data-ttu-id="8de39-161">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8de39-162">NameU</span><span class="sxs-lookup"><span data-stu-id="8de39-162">NameU</span></span>  <br/> |<span data-ttu-id="8de39-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8de39-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8de39-164">必須</span><span class="sxs-lookup"><span data-stu-id="8de39-164">required</span></span>  <br/> |<span data-ttu-id="8de39-165">入力規則の汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="8de39-166">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8de39-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="8de39-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="8de39-168">xsd: int</span><span class="sxs-lookup"><span data-stu-id="8de39-168">xsd:int</span></span>  <br/> |<span data-ttu-id="8de39-169">省略可能</span><span class="sxs-lookup"><span data-stu-id="8de39-169">optional</span></span>  <br/> |<span data-ttu-id="8de39-170">入力規則を適用するオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="8de39-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="8de39-171">Xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="8de39-171">Values of the xsd:int type.</span></span>  <br/> |
   

