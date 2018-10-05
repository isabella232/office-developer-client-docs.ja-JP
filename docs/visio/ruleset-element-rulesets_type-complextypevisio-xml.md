---
title: ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: ダイアグラムの検証ルールの 1 つのセットを表します。
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387392"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="86c84-103">ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="86c84-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="86c84-104">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="86c84-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86c84-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="86c84-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86c84-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="86c84-106">**Element type**</span></span> <br/> |[<span data-ttu-id="86c84-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="86c84-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="86c84-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="86c84-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="86c84-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="86c84-109">**Schema file**</span></span> <br/> |<span data-ttu-id="86c84-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="86c84-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="86c84-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="86c84-111">**Document parts**</span></span> <br/> |<span data-ttu-id="86c84-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="86c84-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86c84-113">定義</span><span class="sxs-lookup"><span data-stu-id="86c84-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86c84-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="86c84-114">Elements and attributes</span></span>

<span data-ttu-id="86c84-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86c84-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="86c84-116">親要素</span><span class="sxs-lookup"><span data-stu-id="86c84-116">Parent elements</span></span>

|<span data-ttu-id="86c84-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="86c84-117">**Element**</span></span>|<span data-ttu-id="86c84-118">**型**</span><span class="sxs-lookup"><span data-stu-id="86c84-118">**Type**</span></span>|<span data-ttu-id="86c84-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="86c84-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86c84-120">ルールセット</span><span class="sxs-lookup"><span data-stu-id="86c84-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86c84-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="86c84-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86c84-122">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86c84-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86c84-123">子要素</span><span class="sxs-lookup"><span data-stu-id="86c84-123">Child elements</span></span>

|<span data-ttu-id="86c84-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="86c84-124">**Element**</span></span>|<span data-ttu-id="86c84-125">**型**</span><span class="sxs-lookup"><span data-stu-id="86c84-125">**Type**</span></span>|<span data-ttu-id="86c84-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="86c84-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86c84-127">Rule</span><span class="sxs-lookup"><span data-stu-id="86c84-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86c84-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="86c84-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86c84-129">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="86c84-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="86c84-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="86c84-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86c84-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="86c84-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86c84-132">ルール ・ セットのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="86c84-133">属性</span><span class="sxs-lookup"><span data-stu-id="86c84-133">Attributes</span></span>

|<span data-ttu-id="86c84-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="86c84-134">**Attribute**</span></span>|<span data-ttu-id="86c84-135">**型**</span><span class="sxs-lookup"><span data-stu-id="86c84-135">**Type**</span></span>|<span data-ttu-id="86c84-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="86c84-136">**Required**</span></span>|<span data-ttu-id="86c84-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="86c84-137">**Description**</span></span>|<span data-ttu-id="86c84-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="86c84-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="86c84-139">説明</span><span class="sxs-lookup"><span data-stu-id="86c84-139">Description</span></span>  <br/> |<span data-ttu-id="86c84-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86c84-140">xsd:string</span></span>  <br/> |<span data-ttu-id="86c84-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="86c84-141">optional</span></span>  <br/> |<span data-ttu-id="86c84-142">検証ルール セットのユーザー インターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="86c84-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="86c84-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="86c84-144">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c84-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86c84-145">有効</span><span class="sxs-lookup"><span data-stu-id="86c84-145">Enabled</span></span>  <br/> |<span data-ttu-id="86c84-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="86c84-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="86c84-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="86c84-147">optional</span></span>  <br/> |<span data-ttu-id="86c84-148">現在のドキュメントの検証が発生したときに指定された検証規則セットに規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="86c84-149">既定では true を指定 します。</span><span class="sxs-lookup"><span data-stu-id="86c84-149">Default is True.</span></span>  <br/> |<span data-ttu-id="86c84-150">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c84-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="86c84-151">ID</span><span class="sxs-lookup"><span data-stu-id="86c84-151">ID</span></span>  <br/> |<span data-ttu-id="86c84-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="86c84-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="86c84-153">必須</span><span class="sxs-lookup"><span data-stu-id="86c84-153">required</span></span>  <br/> |<span data-ttu-id="86c84-154">検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="86c84-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c84-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="86c84-156">名前</span><span class="sxs-lookup"><span data-stu-id="86c84-156">Name</span></span>  <br/> |<span data-ttu-id="86c84-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86c84-157">xsd:string</span></span>  <br/> |<span data-ttu-id="86c84-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="86c84-158">optional</span></span>  <br/> |<span data-ttu-id="86c84-159">ローカル検証ルール セットの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="86c84-160">NameU 属性の値を既定値です。</span><span class="sxs-lookup"><span data-stu-id="86c84-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="86c84-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c84-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86c84-162">NameU</span><span class="sxs-lookup"><span data-stu-id="86c84-162">NameU</span></span>  <br/> |<span data-ttu-id="86c84-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86c84-163">xsd:string</span></span>  <br/> |<span data-ttu-id="86c84-164">必須</span><span class="sxs-lookup"><span data-stu-id="86c84-164">required</span></span>  <br/> |<span data-ttu-id="86c84-165">検証ルール セットの汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="86c84-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="86c84-166">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c84-166">Values of the xsd:string type.</span></span>  <br/> |
   

