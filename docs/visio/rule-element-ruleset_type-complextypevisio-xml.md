---
title: (RuleSet_Type の複合型) のルールの要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: 図の検証ルール セットに含まれる 1 つの検証ルールを表します。
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806311"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="b149c-103">(RuleSet_Type の複合型) のルールの要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b149c-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b149c-104">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="b149c-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b149c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b149c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b149c-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="b149c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b149c-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="b149c-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b149c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b149c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b149c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b149c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b149c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b149c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b149c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b149c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b149c-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="b149c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b149c-113">定義</span><span class="sxs-lookup"><span data-stu-id="b149c-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b149c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b149c-114">Elements and attributes</span></span>

<span data-ttu-id="b149c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b149c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b149c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b149c-116">Parent elements</span></span>

|<span data-ttu-id="b149c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b149c-117">**Element**</span></span>|<span data-ttu-id="b149c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b149c-118">**Type**</span></span>|<span data-ttu-id="b149c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b149c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b149c-120">ルールセット</span><span class="sxs-lookup"><span data-stu-id="b149c-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b149c-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="b149c-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b149c-122">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="b149c-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b149c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b149c-123">Child elements</span></span>

|<span data-ttu-id="b149c-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="b149c-124">**Element**</span></span>|<span data-ttu-id="b149c-125">**型**</span><span class="sxs-lookup"><span data-stu-id="b149c-125">**Type**</span></span>|<span data-ttu-id="b149c-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="b149c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b149c-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="b149c-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b149c-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="b149c-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b149c-129">対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="b149c-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="b149c-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b149c-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="b149c-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b149c-132">対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b149c-133">属性</span><span class="sxs-lookup"><span data-stu-id="b149c-133">Attributes</span></span>

|<span data-ttu-id="b149c-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="b149c-134">**Attribute**</span></span>|<span data-ttu-id="b149c-135">**型**</span><span class="sxs-lookup"><span data-stu-id="b149c-135">**Type**</span></span>|<span data-ttu-id="b149c-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="b149c-136">**Required**</span></span>|<span data-ttu-id="b149c-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="b149c-137">**Description**</span></span>|<span data-ttu-id="b149c-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b149c-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b149c-139">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="b149c-139">Category</span></span>  <br/> |<span data-ttu-id="b149c-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b149c-140">xsd:string</span></span>  <br/> |<span data-ttu-id="b149c-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="b149c-141">optional</span></span>  <br/> |<span data-ttu-id="b149c-142">問題ウィンドウの [**カテゴリ**] 列に表示するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="b149c-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b149c-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="b149c-144">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b149c-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b149c-145">説明</span><span class="sxs-lookup"><span data-stu-id="b149c-145">Description</span></span>  <br/> |<span data-ttu-id="b149c-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b149c-146">xsd:string</span></span>  <br/> |<span data-ttu-id="b149c-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="b149c-147">optional</span></span>  <br/> |<span data-ttu-id="b149c-148">ユーザー インターフェイスに表示される入力規則の説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="b149c-149">既定では「不明」です。</span><span class="sxs-lookup"><span data-stu-id="b149c-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="b149c-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b149c-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b149c-151">ID</span><span class="sxs-lookup"><span data-stu-id="b149c-151">ID</span></span>  <br/> |<span data-ttu-id="b149c-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b149c-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b149c-153">必須</span><span class="sxs-lookup"><span data-stu-id="b149c-153">required</span></span>  <br/> |<span data-ttu-id="b149c-154">検証ルールの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="b149c-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b149c-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b149c-156">無視</span><span class="sxs-lookup"><span data-stu-id="b149c-156">Ignored</span></span>  <br/> |<span data-ttu-id="b149c-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="b149c-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b149c-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="b149c-158">optional</span></span>  <br/> |<span data-ttu-id="b149c-159">入力規則が現在無視するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="b149c-160">既定では False です。</span><span class="sxs-lookup"><span data-stu-id="b149c-160">Default is False.</span></span>  <br/> |<span data-ttu-id="b149c-161">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b149c-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b149c-162">NameU</span><span class="sxs-lookup"><span data-stu-id="b149c-162">NameU</span></span>  <br/> |<span data-ttu-id="b149c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b149c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="b149c-164">必須</span><span class="sxs-lookup"><span data-stu-id="b149c-164">required</span></span>  <br/> |<span data-ttu-id="b149c-165">入力規則の汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="b149c-166">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b149c-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b149c-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="b149c-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="b149c-168">xsd:int</span><span class="sxs-lookup"><span data-stu-id="b149c-168">xsd:int</span></span>  <br/> |<span data-ttu-id="b149c-169">省略可能</span><span class="sxs-lookup"><span data-stu-id="b149c-169">optional</span></span>  <br/> |<span data-ttu-id="b149c-170">検証規則を適用するオブジェクトの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="b149c-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="b149c-171">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="b149c-171">Values of the xsd:int type.</span></span>  <br/> |
   

