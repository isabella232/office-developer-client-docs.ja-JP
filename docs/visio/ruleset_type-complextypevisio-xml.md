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
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="612ed-102">RuleSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="612ed-102">RuleSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="612ed-103">型情報</span><span class="sxs-lookup"><span data-stu-id="612ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="612ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="612ed-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="612ed-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="612ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="612ed-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="612ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="612ed-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="612ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="612ed-108">None</span><span class="sxs-lookup"><span data-stu-id="612ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="612ed-109">定義</span><span class="sxs-lookup"><span data-stu-id="612ed-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="612ed-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="612ed-110">Elements and attributes</span></span>

<span data-ttu-id="612ed-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="612ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="612ed-112">子要素</span><span class="sxs-lookup"><span data-stu-id="612ed-112">Child elements</span></span>

|<span data-ttu-id="612ed-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="612ed-113">**Element**</span></span>|<span data-ttu-id="612ed-114">**型**</span><span class="sxs-lookup"><span data-stu-id="612ed-114">**Type**</span></span>|<span data-ttu-id="612ed-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="612ed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="612ed-116">Rule</span><span class="sxs-lookup"><span data-stu-id="612ed-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="612ed-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="612ed-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="612ed-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="612ed-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="612ed-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="612ed-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="612ed-120">属性</span><span class="sxs-lookup"><span data-stu-id="612ed-120">Attributes</span></span>

|<span data-ttu-id="612ed-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="612ed-121">**Attribute**</span></span>|<span data-ttu-id="612ed-122">**型**</span><span class="sxs-lookup"><span data-stu-id="612ed-122">**Type**</span></span>|<span data-ttu-id="612ed-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="612ed-123">**Required**</span></span>|<span data-ttu-id="612ed-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="612ed-124">**Description**</span></span>|<span data-ttu-id="612ed-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="612ed-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="612ed-126">説明</span><span class="sxs-lookup"><span data-stu-id="612ed-126">Description</span></span>  <br/> |<span data-ttu-id="612ed-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="612ed-127">xsd:string</span></span>  <br/> |<span data-ttu-id="612ed-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="612ed-128">optional</span></span>  <br/> ||<span data-ttu-id="612ed-129">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="612ed-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="612ed-130">有効</span><span class="sxs-lookup"><span data-stu-id="612ed-130">Enabled</span></span>  <br/> |<span data-ttu-id="612ed-131">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="612ed-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="612ed-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="612ed-132">optional</span></span>  <br/> ||<span data-ttu-id="612ed-133">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="612ed-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="612ed-134">ID</span><span class="sxs-lookup"><span data-stu-id="612ed-134">ID</span></span>  <br/> |<span data-ttu-id="612ed-135">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="612ed-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="612ed-136">必須</span><span class="sxs-lookup"><span data-stu-id="612ed-136">required</span></span>  <br/> ||<span data-ttu-id="612ed-137">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="612ed-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="612ed-138">名前</span><span class="sxs-lookup"><span data-stu-id="612ed-138">Name</span></span>  <br/> |<span data-ttu-id="612ed-139">xsd: string</span><span class="sxs-lookup"><span data-stu-id="612ed-139">xsd:string</span></span>  <br/> |<span data-ttu-id="612ed-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="612ed-140">optional</span></span>  <br/> ||<span data-ttu-id="612ed-141">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="612ed-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="612ed-142">NameU</span><span class="sxs-lookup"><span data-stu-id="612ed-142">NameU</span></span>  <br/> |<span data-ttu-id="612ed-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="612ed-143">xsd:string</span></span>  <br/> |<span data-ttu-id="612ed-144">必須</span><span class="sxs-lookup"><span data-stu-id="612ed-144">required</span></span>  <br/> ||<span data-ttu-id="612ed-145">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="612ed-145">Values of the xsd:string type.</span></span>  <br/> |
   

