---
title: RuleSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 5d3d29ee7ae48c344afcdce3faf5e26d5f564501
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541625"
---
# <a name="ruleset_type-complextype-visio-xml"></a><span data-ttu-id="1b86d-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1b86d-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1b86d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1b86d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b86d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b86d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b86d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b86d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b86d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1b86d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b86d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1b86d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b86d-108">なし</span><span class="sxs-lookup"><span data-stu-id="1b86d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b86d-109">定義</span><span class="sxs-lookup"><span data-stu-id="1b86d-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSet_Type">
          
          <xs:sequence>
    <xs:element name="RuleSetFlags"  type="RuleSetFlags_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rule"  type="Rule_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b86d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b86d-110">Elements and attributes</span></span>

<span data-ttu-id="1b86d-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b86d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b86d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1b86d-112">Child elements</span></span>

|<span data-ttu-id="1b86d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b86d-113">**Element**</span></span>|<span data-ttu-id="1b86d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1b86d-114">**Type**</span></span>|<span data-ttu-id="1b86d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b86d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b86d-116">Rule</span><span class="sxs-lookup"><span data-stu-id="1b86d-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b86d-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="1b86d-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1b86d-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="1b86d-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b86d-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="1b86d-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1b86d-120">属性</span><span class="sxs-lookup"><span data-stu-id="1b86d-120">Attributes</span></span>

|<span data-ttu-id="1b86d-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b86d-121">**Attribute**</span></span>|<span data-ttu-id="1b86d-122">**型**</span><span class="sxs-lookup"><span data-stu-id="1b86d-122">**Type**</span></span>|<span data-ttu-id="1b86d-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="1b86d-123">**Required**</span></span>|<span data-ttu-id="1b86d-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b86d-124">**Description**</span></span>|<span data-ttu-id="1b86d-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1b86d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b86d-126">説明</span><span class="sxs-lookup"><span data-stu-id="1b86d-126">Description</span></span>  <br/> |<span data-ttu-id="1b86d-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b86d-127">xsd:string</span></span>  <br/> |<span data-ttu-id="1b86d-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b86d-128">optional</span></span>  <br/> ||<span data-ttu-id="1b86d-129">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b86d-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b86d-130">有効</span><span class="sxs-lookup"><span data-stu-id="1b86d-130">Enabled</span></span>  <br/> |<span data-ttu-id="1b86d-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1b86d-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b86d-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b86d-132">optional</span></span>  <br/> ||<span data-ttu-id="1b86d-133">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b86d-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1b86d-134">ID</span><span class="sxs-lookup"><span data-stu-id="1b86d-134">ID</span></span>  <br/> |<span data-ttu-id="1b86d-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b86d-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b86d-136">必須</span><span class="sxs-lookup"><span data-stu-id="1b86d-136">required</span></span>  <br/> ||<span data-ttu-id="1b86d-137">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b86d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b86d-138">名前</span><span class="sxs-lookup"><span data-stu-id="1b86d-138">Name</span></span>  <br/> |<span data-ttu-id="1b86d-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b86d-139">xsd:string</span></span>  <br/> |<span data-ttu-id="1b86d-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b86d-140">optional</span></span>  <br/> ||<span data-ttu-id="1b86d-141">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b86d-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b86d-142">NameU</span><span class="sxs-lookup"><span data-stu-id="1b86d-142">NameU</span></span>  <br/> |<span data-ttu-id="1b86d-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b86d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1b86d-144">必須</span><span class="sxs-lookup"><span data-stu-id="1b86d-144">required</span></span>  <br/> ||<span data-ttu-id="1b86d-145">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b86d-145">Values of the xsd:string type.</span></span>  <br/> |
   

