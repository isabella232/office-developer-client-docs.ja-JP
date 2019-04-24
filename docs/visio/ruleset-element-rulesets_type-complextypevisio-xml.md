---
title: ルールセット要素 (RuleSets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: 1組のダイアグラム検証ルールを表します。
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318915"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="20540-103">ルールセット要素 (RuleSets_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="20540-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="20540-104">1組のダイアグラム検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="20540-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20540-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="20540-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20540-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="20540-106">**Element type**</span></span> <br/> |[<span data-ttu-id="20540-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="20540-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="20540-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20540-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="20540-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="20540-109">**Schema file**</span></span> <br/> |<span data-ttu-id="20540-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="20540-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="20540-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="20540-111">**Document parts**</span></span> <br/> |<span data-ttu-id="20540-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="20540-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20540-113">定義</span><span class="sxs-lookup"><span data-stu-id="20540-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20540-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="20540-114">Elements and attributes</span></span>

<span data-ttu-id="20540-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="20540-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="20540-116">親要素</span><span class="sxs-lookup"><span data-stu-id="20540-116">Parent elements</span></span>

|<span data-ttu-id="20540-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="20540-117">**Element**</span></span>|<span data-ttu-id="20540-118">**型**</span><span class="sxs-lookup"><span data-stu-id="20540-118">**Type**</span></span>|<span data-ttu-id="20540-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="20540-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20540-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="20540-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20540-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="20540-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20540-122">文書内\*\*\*\* の各入力規則のルールセット要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="20540-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20540-123">子要素</span><span class="sxs-lookup"><span data-stu-id="20540-123">Child elements</span></span>

|<span data-ttu-id="20540-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="20540-124">**Element**</span></span>|<span data-ttu-id="20540-125">**型**</span><span class="sxs-lookup"><span data-stu-id="20540-125">**Type**</span></span>|<span data-ttu-id="20540-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="20540-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20540-127">Rule</span><span class="sxs-lookup"><span data-stu-id="20540-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20540-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="20540-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20540-129">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="20540-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="20540-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="20540-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="20540-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="20540-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20540-132">ルールセットのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="20540-133">属性</span><span class="sxs-lookup"><span data-stu-id="20540-133">Attributes</span></span>

|<span data-ttu-id="20540-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="20540-134">**Attribute**</span></span>|<span data-ttu-id="20540-135">**型**</span><span class="sxs-lookup"><span data-stu-id="20540-135">**Type**</span></span>|<span data-ttu-id="20540-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="20540-136">**Required**</span></span>|<span data-ttu-id="20540-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="20540-137">**Description**</span></span>|<span data-ttu-id="20540-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="20540-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20540-139">説明</span><span class="sxs-lookup"><span data-stu-id="20540-139">Description</span></span>  <br/> |<span data-ttu-id="20540-140">xsd: string</span><span class="sxs-lookup"><span data-stu-id="20540-140">xsd:string</span></span>  <br/> |<span data-ttu-id="20540-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="20540-141">optional</span></span>  <br/> |<span data-ttu-id="20540-142">入力規則セットのユーザーインターフェイスに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="20540-143">既定値は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="20540-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="20540-144">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="20540-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20540-145">有効</span><span class="sxs-lookup"><span data-stu-id="20540-145">Enabled</span></span>  <br/> |<span data-ttu-id="20540-146">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="20540-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="20540-147">省略可能</span><span class="sxs-lookup"><span data-stu-id="20540-147">optional</span></span>  <br/> |<span data-ttu-id="20540-148">現在の文書に対して検証がトリガーされたときに、指定した入力規則セットの規則をチェックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="20540-149">既定値は True です。</span><span class="sxs-lookup"><span data-stu-id="20540-149">Default is True.</span></span>  <br/> |<span data-ttu-id="20540-150">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="20540-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="20540-151">ID</span><span class="sxs-lookup"><span data-stu-id="20540-151">ID</span></span>  <br/> |<span data-ttu-id="20540-152">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="20540-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20540-153">必須</span><span class="sxs-lookup"><span data-stu-id="20540-153">required</span></span>  <br/> |<span data-ttu-id="20540-154">入力規則セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="20540-155">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="20540-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20540-156">名前</span><span class="sxs-lookup"><span data-stu-id="20540-156">Name</span></span>  <br/> |<span data-ttu-id="20540-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="20540-157">xsd:string</span></span>  <br/> |<span data-ttu-id="20540-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="20540-158">optional</span></span>  <br/> |<span data-ttu-id="20540-159">入力規則セットのローカル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="20540-160">既定値は NameU attribute 値です。</span><span class="sxs-lookup"><span data-stu-id="20540-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="20540-161">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="20540-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20540-162">NameU</span><span class="sxs-lookup"><span data-stu-id="20540-162">NameU</span></span>  <br/> |<span data-ttu-id="20540-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="20540-163">xsd:string</span></span>  <br/> |<span data-ttu-id="20540-164">必須</span><span class="sxs-lookup"><span data-stu-id="20540-164">required</span></span>  <br/> |<span data-ttu-id="20540-165">入力規則セットの汎用名を指定します。</span><span class="sxs-lookup"><span data-stu-id="20540-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="20540-166">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="20540-166">Values of the xsd:string type.</span></span>  <br/> |
   

