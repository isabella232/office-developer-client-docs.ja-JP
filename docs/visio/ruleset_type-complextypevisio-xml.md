---
title: RuleSet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: 3d8279b2995bcdf75f67fc7f65709dc3dab49642
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393622"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="beea3-102">RuleSet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="beea3-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="beea3-103">型情報</span><span class="sxs-lookup"><span data-stu-id="beea3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beea3-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="beea3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="beea3-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="beea3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="beea3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="beea3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="beea3-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="beea3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="beea3-108">なし</span><span class="sxs-lookup"><span data-stu-id="beea3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="beea3-109">定義</span><span class="sxs-lookup"><span data-stu-id="beea3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="beea3-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="beea3-110">Elements and attributes</span></span>

<span data-ttu-id="beea3-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="beea3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="beea3-112">子要素</span><span class="sxs-lookup"><span data-stu-id="beea3-112">Child elements</span></span>

|<span data-ttu-id="beea3-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="beea3-113">**Element**</span></span>|<span data-ttu-id="beea3-114">**型**</span><span class="sxs-lookup"><span data-stu-id="beea3-114">**Type**</span></span>|<span data-ttu-id="beea3-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="beea3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="beea3-116">Rule</span><span class="sxs-lookup"><span data-stu-id="beea3-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="beea3-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="beea3-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="beea3-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="beea3-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="beea3-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="beea3-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="beea3-120">属性</span><span class="sxs-lookup"><span data-stu-id="beea3-120">Attributes</span></span>

|<span data-ttu-id="beea3-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="beea3-121">**Attribute**</span></span>|<span data-ttu-id="beea3-122">**型**</span><span class="sxs-lookup"><span data-stu-id="beea3-122">**Type**</span></span>|<span data-ttu-id="beea3-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="beea3-123">**Required**</span></span>|<span data-ttu-id="beea3-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="beea3-124">**Description**</span></span>|<span data-ttu-id="beea3-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="beea3-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="beea3-126">説明</span><span class="sxs-lookup"><span data-stu-id="beea3-126">Description</span></span>  <br/> |<span data-ttu-id="beea3-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="beea3-127">xsd:string</span></span>  <br/> |<span data-ttu-id="beea3-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="beea3-128">optional</span></span>  <br/> ||<span data-ttu-id="beea3-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beea3-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="beea3-130">有効</span><span class="sxs-lookup"><span data-stu-id="beea3-130">Enabled</span></span>  <br/> |<span data-ttu-id="beea3-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="beea3-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="beea3-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="beea3-132">optional</span></span>  <br/> ||<span data-ttu-id="beea3-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beea3-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="beea3-134">ID</span><span class="sxs-lookup"><span data-stu-id="beea3-134">ID</span></span>  <br/> |<span data-ttu-id="beea3-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="beea3-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="beea3-136">必須</span><span class="sxs-lookup"><span data-stu-id="beea3-136">required</span></span>  <br/> ||<span data-ttu-id="beea3-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beea3-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="beea3-138">名前</span><span class="sxs-lookup"><span data-stu-id="beea3-138">Name</span></span>  <br/> |<span data-ttu-id="beea3-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="beea3-139">xsd:string</span></span>  <br/> |<span data-ttu-id="beea3-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="beea3-140">optional</span></span>  <br/> ||<span data-ttu-id="beea3-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beea3-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="beea3-142">NameU</span><span class="sxs-lookup"><span data-stu-id="beea3-142">NameU</span></span>  <br/> |<span data-ttu-id="beea3-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="beea3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="beea3-144">必須</span><span class="sxs-lookup"><span data-stu-id="beea3-144">required</span></span>  <br/> ||<span data-ttu-id="beea3-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="beea3-145">Values of the xsd:string type.</span></span>  <br/> |
   

