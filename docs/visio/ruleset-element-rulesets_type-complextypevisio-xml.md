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
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="f8600-103">ルールセットの要素 (RuleSets_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="f8600-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f8600-104">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="f8600-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8600-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f8600-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8600-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="f8600-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f8600-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="f8600-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f8600-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="f8600-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f8600-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f8600-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f8600-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f8600-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f8600-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="f8600-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f8600-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="f8600-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8600-113">定義</span><span class="sxs-lookup"><span data-stu-id="f8600-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f8600-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f8600-114">Elements and attributes</span></span>

<span data-ttu-id="f8600-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8600-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f8600-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f8600-116">Parent elements</span></span>

|<span data-ttu-id="f8600-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f8600-117">**Element**</span></span>|<span data-ttu-id="f8600-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f8600-118">**Type**</span></span>|<span data-ttu-id="f8600-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8600-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f8600-120">ルールセット</span><span class="sxs-lookup"><span data-stu-id="f8600-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8600-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="f8600-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f8600-122">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f8600-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8600-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f8600-123">Child elements</span></span>

|<span data-ttu-id="f8600-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="f8600-124">**Element**</span></span>|<span data-ttu-id="f8600-125">**型**</span><span class="sxs-lookup"><span data-stu-id="f8600-125">**Type**</span></span>|<span data-ttu-id="f8600-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8600-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f8600-127">Rule</span><span class="sxs-lookup"><span data-stu-id="f8600-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8600-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="f8600-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f8600-129">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="f8600-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="f8600-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="f8600-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f8600-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="f8600-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f8600-132">ルール ・ セットのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f8600-133">属性</span><span class="sxs-lookup"><span data-stu-id="f8600-133">Attributes</span></span>

|<span data-ttu-id="f8600-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="f8600-134">**Attribute**</span></span>|<span data-ttu-id="f8600-135">**型**</span><span class="sxs-lookup"><span data-stu-id="f8600-135">**Type**</span></span>|<span data-ttu-id="f8600-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="f8600-136">**Required**</span></span>|<span data-ttu-id="f8600-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="f8600-137">**Description**</span></span>|<span data-ttu-id="f8600-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="f8600-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8600-139">説明</span><span class="sxs-lookup"><span data-stu-id="f8600-139">Description</span></span>  <br/> |<span data-ttu-id="f8600-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f8600-140">xsd:string</span></span>  <br/> |<span data-ttu-id="f8600-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="f8600-141">optional</span></span>  <br/> |<span data-ttu-id="f8600-142">検証ルール セットのユーザー インターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="f8600-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f8600-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="f8600-144">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8600-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f8600-145">Enabled</span><span class="sxs-lookup"><span data-stu-id="f8600-145">Enabled</span></span>  <br/> |<span data-ttu-id="f8600-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f8600-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f8600-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="f8600-147">optional</span></span>  <br/> |<span data-ttu-id="f8600-148">現在のドキュメントの検証が発生したときに指定された検証規則セットに規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="f8600-149">既定では True です。</span><span class="sxs-lookup"><span data-stu-id="f8600-149">Default is True.</span></span>  <br/> |<span data-ttu-id="f8600-150">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8600-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f8600-151">ID</span><span class="sxs-lookup"><span data-stu-id="f8600-151">ID</span></span>  <br/> |<span data-ttu-id="f8600-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f8600-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8600-153">必須</span><span class="sxs-lookup"><span data-stu-id="f8600-153">required</span></span>  <br/> |<span data-ttu-id="f8600-154">検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f8600-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8600-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8600-156">名前</span><span class="sxs-lookup"><span data-stu-id="f8600-156">Name</span></span>  <br/> |<span data-ttu-id="f8600-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f8600-157">xsd:string</span></span>  <br/> |<span data-ttu-id="f8600-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="f8600-158">optional</span></span>  <br/> |<span data-ttu-id="f8600-159">ローカル検証ルール セットの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="f8600-160">NameU 属性の値を既定値です。</span><span class="sxs-lookup"><span data-stu-id="f8600-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="f8600-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8600-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f8600-162">NameU</span><span class="sxs-lookup"><span data-stu-id="f8600-162">NameU</span></span>  <br/> |<span data-ttu-id="f8600-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f8600-163">xsd:string</span></span>  <br/> |<span data-ttu-id="f8600-164">必須</span><span class="sxs-lookup"><span data-stu-id="f8600-164">required</span></span>  <br/> |<span data-ttu-id="f8600-165">検証ルール セットの汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8600-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="f8600-166">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8600-166">Values of the xsd:string type.</span></span>  <br/> |
   

