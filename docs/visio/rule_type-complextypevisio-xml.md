---
title: Rule_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541716"
---
# <a name="rule_type-complextype-visio-xml"></a><span data-ttu-id="f70f4-102">Rule_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f70f4-102">Rule_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f70f4-103">型情報</span><span class="sxs-lookup"><span data-stu-id="f70f4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f70f4-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f70f4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f70f4-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f70f4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f70f4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f70f4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f70f4-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="f70f4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f70f4-108">なし</span><span class="sxs-lookup"><span data-stu-id="f70f4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f70f4-109">定義</span><span class="sxs-lookup"><span data-stu-id="f70f4-109">Definition</span></span>

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f70f4-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f70f4-110">Elements and attributes</span></span>

<span data-ttu-id="f70f4-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f70f4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f70f4-112">子要素</span><span class="sxs-lookup"><span data-stu-id="f70f4-112">Child elements</span></span>

|<span data-ttu-id="f70f4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f70f4-113">**Element**</span></span>|<span data-ttu-id="f70f4-114">**型**</span><span class="sxs-lookup"><span data-stu-id="f70f4-114">**Type**</span></span>|<span data-ttu-id="f70f4-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f70f4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f70f4-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="f70f4-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f70f4-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="f70f4-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f70f4-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="f70f4-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f70f4-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="f70f4-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f70f4-120">属性</span><span class="sxs-lookup"><span data-stu-id="f70f4-120">Attributes</span></span>

|<span data-ttu-id="f70f4-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="f70f4-121">**Attribute**</span></span>|<span data-ttu-id="f70f4-122">**型**</span><span class="sxs-lookup"><span data-stu-id="f70f4-122">**Type**</span></span>|<span data-ttu-id="f70f4-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="f70f4-123">**Required**</span></span>|<span data-ttu-id="f70f4-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="f70f4-124">**Description**</span></span>|<span data-ttu-id="f70f4-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="f70f4-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f70f4-126">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f70f4-126">Category</span></span>  <br/> |<span data-ttu-id="f70f4-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f70f4-127">xsd:string</span></span>  <br/> |<span data-ttu-id="f70f4-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="f70f4-128">optional</span></span>  <br/> ||<span data-ttu-id="f70f4-129">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f70f4-130">説明</span><span class="sxs-lookup"><span data-stu-id="f70f4-130">Description</span></span>  <br/> |<span data-ttu-id="f70f4-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f70f4-131">xsd:string</span></span>  <br/> |<span data-ttu-id="f70f4-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="f70f4-132">optional</span></span>  <br/> ||<span data-ttu-id="f70f4-133">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f70f4-134">ID</span><span class="sxs-lookup"><span data-stu-id="f70f4-134">ID</span></span>  <br/> |<span data-ttu-id="f70f4-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f70f4-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f70f4-136">必須</span><span class="sxs-lookup"><span data-stu-id="f70f4-136">required</span></span>  <br/> ||<span data-ttu-id="f70f4-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f70f4-138">無視</span><span class="sxs-lookup"><span data-stu-id="f70f4-138">Ignored</span></span>  <br/> |<span data-ttu-id="f70f4-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f70f4-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f70f4-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="f70f4-140">optional</span></span>  <br/> ||<span data-ttu-id="f70f4-141">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f70f4-142">NameU</span><span class="sxs-lookup"><span data-stu-id="f70f4-142">NameU</span></span>  <br/> |<span data-ttu-id="f70f4-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f70f4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="f70f4-144">必須</span><span class="sxs-lookup"><span data-stu-id="f70f4-144">required</span></span>  <br/> ||<span data-ttu-id="f70f4-145">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f70f4-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="f70f4-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="f70f4-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="f70f4-147">xsd:int</span></span>  <br/> |<span data-ttu-id="f70f4-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="f70f4-148">optional</span></span>  <br/> ||<span data-ttu-id="f70f4-149">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="f70f4-149">Values of the xsd:int type.</span></span>  <br/> |
   

