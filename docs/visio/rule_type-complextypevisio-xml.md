---
title: Rule_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283423"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="26622-102">Rule_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="26622-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="26622-103">型情報</span><span class="sxs-lookup"><span data-stu-id="26622-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26622-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26622-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="26622-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="26622-105">**Schema file**</span></span> <br/> |<span data-ttu-id="26622-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="26622-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="26622-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="26622-107">**Extension base**</span></span> <br/> |<span data-ttu-id="26622-108">なし</span><span class="sxs-lookup"><span data-stu-id="26622-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26622-109">定義</span><span class="sxs-lookup"><span data-stu-id="26622-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="26622-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="26622-110">Elements and attributes</span></span>

<span data-ttu-id="26622-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26622-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="26622-112">子要素</span><span class="sxs-lookup"><span data-stu-id="26622-112">Child elements</span></span>

|<span data-ttu-id="26622-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26622-113">**Element**</span></span>|<span data-ttu-id="26622-114">**型**</span><span class="sxs-lookup"><span data-stu-id="26622-114">**Type**</span></span>|<span data-ttu-id="26622-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="26622-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26622-116">rulefilter</span><span class="sxs-lookup"><span data-stu-id="26622-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26622-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="26622-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="26622-118">ルール</span><span class="sxs-lookup"><span data-stu-id="26622-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26622-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="26622-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="26622-120">属性</span><span class="sxs-lookup"><span data-stu-id="26622-120">Attributes</span></span>

|<span data-ttu-id="26622-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="26622-121">**Attribute**</span></span>|<span data-ttu-id="26622-122">**型**</span><span class="sxs-lookup"><span data-stu-id="26622-122">**Type**</span></span>|<span data-ttu-id="26622-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="26622-123">**Required**</span></span>|<span data-ttu-id="26622-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="26622-124">**Description**</span></span>|<span data-ttu-id="26622-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="26622-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26622-126">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="26622-126">Category</span></span>  <br/> |<span data-ttu-id="26622-127">xsd: string</span><span class="sxs-lookup"><span data-stu-id="26622-127">xsd:string</span></span>  <br/> |<span data-ttu-id="26622-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="26622-128">optional</span></span>  <br/> ||<span data-ttu-id="26622-129">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="26622-130">説明</span><span class="sxs-lookup"><span data-stu-id="26622-130">Description</span></span>  <br/> |<span data-ttu-id="26622-131">xsd: string</span><span class="sxs-lookup"><span data-stu-id="26622-131">xsd:string</span></span>  <br/> |<span data-ttu-id="26622-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="26622-132">optional</span></span>  <br/> ||<span data-ttu-id="26622-133">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="26622-134">ID</span><span class="sxs-lookup"><span data-stu-id="26622-134">ID</span></span>  <br/> |<span data-ttu-id="26622-135">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="26622-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="26622-136">必須</span><span class="sxs-lookup"><span data-stu-id="26622-136">required</span></span>  <br/> ||<span data-ttu-id="26622-137">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="26622-138">Ignored</span><span class="sxs-lookup"><span data-stu-id="26622-138">Ignored</span></span>  <br/> |<span data-ttu-id="26622-139">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="26622-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="26622-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="26622-140">optional</span></span>  <br/> ||<span data-ttu-id="26622-141">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="26622-142">NameU</span><span class="sxs-lookup"><span data-stu-id="26622-142">NameU</span></span>  <br/> |<span data-ttu-id="26622-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="26622-143">xsd:string</span></span>  <br/> |<span data-ttu-id="26622-144">必須</span><span class="sxs-lookup"><span data-stu-id="26622-144">required</span></span>  <br/> ||<span data-ttu-id="26622-145">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="26622-146">ruletarget</span><span class="sxs-lookup"><span data-stu-id="26622-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="26622-147">xsd: int</span><span class="sxs-lookup"><span data-stu-id="26622-147">xsd:int</span></span>  <br/> |<span data-ttu-id="26622-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="26622-148">optional</span></span>  <br/> ||<span data-ttu-id="26622-149">xsd: int 型の値。</span><span class="sxs-lookup"><span data-stu-id="26622-149">Values of the xsd:int type.</span></span>  <br/> |
   

