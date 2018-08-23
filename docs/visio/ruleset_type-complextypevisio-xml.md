---
title: RuleSet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2fc66419-f299-8573-ec72-0ea5ff39a896
ms.openlocfilehash: dfb0d50cd1c39be9b98a880028b5c4b4dc597bc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806335"
---
# <a name="rulesettype-complextype-visio-xml"></a><span data-ttu-id="8cf8d-102">RuleSet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8cf8d-102">RuleSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8cf8d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="8cf8d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cf8d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8cf8d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8cf8d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8cf8d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8cf8d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8cf8d-108">なし</span><span class="sxs-lookup"><span data-stu-id="8cf8d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8cf8d-109">定義</span><span class="sxs-lookup"><span data-stu-id="8cf8d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8cf8d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8cf8d-110">Elements and attributes</span></span>

<span data-ttu-id="8cf8d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8cf8d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="8cf8d-112">Child elements</span></span>

|<span data-ttu-id="8cf8d-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-113">**Element**</span></span>|<span data-ttu-id="8cf8d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-114">**Type**</span></span>|<span data-ttu-id="8cf8d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8cf8d-116">Rule</span><span class="sxs-lookup"><span data-stu-id="8cf8d-116">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8cf8d-117">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="8cf8d-117">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8cf8d-118">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="8cf8d-118">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8cf8d-119">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="8cf8d-119">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8cf8d-120">属性</span><span class="sxs-lookup"><span data-stu-id="8cf8d-120">Attributes</span></span>

|<span data-ttu-id="8cf8d-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-121">**Attribute**</span></span>|<span data-ttu-id="8cf8d-122">**型**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-122">**Type**</span></span>|<span data-ttu-id="8cf8d-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-123">**Required**</span></span>|<span data-ttu-id="8cf8d-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-124">**Description**</span></span>|<span data-ttu-id="8cf8d-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="8cf8d-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8cf8d-126">説明</span><span class="sxs-lookup"><span data-stu-id="8cf8d-126">Description</span></span>  <br/> |<span data-ttu-id="8cf8d-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8cf8d-127">xsd:string</span></span>  <br/> |<span data-ttu-id="8cf8d-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="8cf8d-128">optional</span></span>  <br/> ||<span data-ttu-id="8cf8d-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8cf8d-130">有効</span><span class="sxs-lookup"><span data-stu-id="8cf8d-130">Enabled</span></span>  <br/> |<span data-ttu-id="8cf8d-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8cf8d-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8cf8d-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="8cf8d-132">optional</span></span>  <br/> ||<span data-ttu-id="8cf8d-133">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8cf8d-134">ID</span><span class="sxs-lookup"><span data-stu-id="8cf8d-134">ID</span></span>  <br/> |<span data-ttu-id="8cf8d-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8cf8d-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8cf8d-136">必須</span><span class="sxs-lookup"><span data-stu-id="8cf8d-136">required</span></span>  <br/> ||<span data-ttu-id="8cf8d-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8cf8d-138">名前</span><span class="sxs-lookup"><span data-stu-id="8cf8d-138">Name</span></span>  <br/> |<span data-ttu-id="8cf8d-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8cf8d-139">xsd:string</span></span>  <br/> |<span data-ttu-id="8cf8d-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="8cf8d-140">optional</span></span>  <br/> ||<span data-ttu-id="8cf8d-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8cf8d-142">NameU</span><span class="sxs-lookup"><span data-stu-id="8cf8d-142">NameU</span></span>  <br/> |<span data-ttu-id="8cf8d-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8cf8d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8cf8d-144">必須</span><span class="sxs-lookup"><span data-stu-id="8cf8d-144">required</span></span>  <br/> ||<span data-ttu-id="8cf8d-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cf8d-145">Values of the xsd:string type.</span></span>  <br/> |
   

