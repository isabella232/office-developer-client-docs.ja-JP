---
title: ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: ダイアグラムの検証ルールの 1 つのセットを表します。
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806331"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="dae9a-103">ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="dae9a-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dae9a-104">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dae9a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="dae9a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dae9a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="dae9a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dae9a-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="dae9a-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dae9a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="dae9a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dae9a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dae9a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dae9a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dae9a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dae9a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="dae9a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dae9a-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="dae9a-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dae9a-113">定義</span><span class="sxs-lookup"><span data-stu-id="dae9a-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dae9a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dae9a-114">Elements and attributes</span></span>

<span data-ttu-id="dae9a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dae9a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dae9a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dae9a-116">Parent elements</span></span>

|<span data-ttu-id="dae9a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dae9a-117">**Element**</span></span>|<span data-ttu-id="dae9a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dae9a-118">**Type**</span></span>|<span data-ttu-id="dae9a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dae9a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dae9a-120">ルールセット</span><span class="sxs-lookup"><span data-stu-id="dae9a-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dae9a-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="dae9a-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dae9a-122">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dae9a-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dae9a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dae9a-123">Child elements</span></span>

|<span data-ttu-id="dae9a-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="dae9a-124">**Element**</span></span>|<span data-ttu-id="dae9a-125">**型**</span><span class="sxs-lookup"><span data-stu-id="dae9a-125">**Type**</span></span>|<span data-ttu-id="dae9a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="dae9a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dae9a-127">Rule</span><span class="sxs-lookup"><span data-stu-id="dae9a-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dae9a-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="dae9a-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dae9a-129">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="dae9a-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="dae9a-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dae9a-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="dae9a-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dae9a-132">ルール ・ セットのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dae9a-133">属性</span><span class="sxs-lookup"><span data-stu-id="dae9a-133">Attributes</span></span>

|<span data-ttu-id="dae9a-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="dae9a-134">**Attribute**</span></span>|<span data-ttu-id="dae9a-135">**型**</span><span class="sxs-lookup"><span data-stu-id="dae9a-135">**Type**</span></span>|<span data-ttu-id="dae9a-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="dae9a-136">**Required**</span></span>|<span data-ttu-id="dae9a-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="dae9a-137">**Description**</span></span>|<span data-ttu-id="dae9a-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="dae9a-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dae9a-139">説明</span><span class="sxs-lookup"><span data-stu-id="dae9a-139">Description</span></span>  <br/> |<span data-ttu-id="dae9a-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dae9a-140">xsd:string</span></span>  <br/> |<span data-ttu-id="dae9a-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="dae9a-141">optional</span></span>  <br/> |<span data-ttu-id="dae9a-142">検証ルール セットのユーザー インターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="dae9a-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="dae9a-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="dae9a-144">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dae9a-145">有効</span><span class="sxs-lookup"><span data-stu-id="dae9a-145">Enabled</span></span>  <br/> |<span data-ttu-id="dae9a-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="dae9a-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dae9a-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="dae9a-147">optional</span></span>  <br/> |<span data-ttu-id="dae9a-148">現在のドキュメントの検証が発生したときに指定された検証規則セットに規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="dae9a-149">既定では true を指定 します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-149">Default is True.</span></span>  <br/> |<span data-ttu-id="dae9a-150">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dae9a-151">ID</span><span class="sxs-lookup"><span data-stu-id="dae9a-151">ID</span></span>  <br/> |<span data-ttu-id="dae9a-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dae9a-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dae9a-153">必須</span><span class="sxs-lookup"><span data-stu-id="dae9a-153">required</span></span>  <br/> |<span data-ttu-id="dae9a-154">検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="dae9a-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dae9a-156">名前</span><span class="sxs-lookup"><span data-stu-id="dae9a-156">Name</span></span>  <br/> |<span data-ttu-id="dae9a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dae9a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="dae9a-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="dae9a-158">optional</span></span>  <br/> |<span data-ttu-id="dae9a-159">ローカル検証ルール セットの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="dae9a-160">NameU 属性の値を既定値です。</span><span class="sxs-lookup"><span data-stu-id="dae9a-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="dae9a-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="dae9a-162">NameU</span><span class="sxs-lookup"><span data-stu-id="dae9a-162">NameU</span></span>  <br/> |<span data-ttu-id="dae9a-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dae9a-163">xsd:string</span></span>  <br/> |<span data-ttu-id="dae9a-164">必須</span><span class="sxs-lookup"><span data-stu-id="dae9a-164">required</span></span>  <br/> |<span data-ttu-id="dae9a-165">検証ルール セットの汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="dae9a-166">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dae9a-166">Values of the xsd:string type.</span></span>  <br/> |
   

