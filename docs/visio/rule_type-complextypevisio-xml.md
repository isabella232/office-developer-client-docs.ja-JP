---
title: Rule_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 380c59d659c820f0c5452ce37fa3616e1408a86c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806322"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="37d2b-102">Rule_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="37d2b-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="37d2b-103">型情報</span><span class="sxs-lookup"><span data-stu-id="37d2b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37d2b-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="37d2b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="37d2b-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="37d2b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="37d2b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="37d2b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="37d2b-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="37d2b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="37d2b-108">なし</span><span class="sxs-lookup"><span data-stu-id="37d2b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="37d2b-109">定義</span><span class="sxs-lookup"><span data-stu-id="37d2b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="37d2b-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="37d2b-110">Elements and attributes</span></span>

<span data-ttu-id="37d2b-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d2b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="37d2b-112">子要素</span><span class="sxs-lookup"><span data-stu-id="37d2b-112">Child elements</span></span>

|<span data-ttu-id="37d2b-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="37d2b-113">**Element**</span></span>|<span data-ttu-id="37d2b-114">**型**</span><span class="sxs-lookup"><span data-stu-id="37d2b-114">**Type**</span></span>|<span data-ttu-id="37d2b-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="37d2b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="37d2b-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="37d2b-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37d2b-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="37d2b-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="37d2b-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="37d2b-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="37d2b-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="37d2b-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="37d2b-120">属性</span><span class="sxs-lookup"><span data-stu-id="37d2b-120">Attributes</span></span>

|<span data-ttu-id="37d2b-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="37d2b-121">**Attribute**</span></span>|<span data-ttu-id="37d2b-122">**型**</span><span class="sxs-lookup"><span data-stu-id="37d2b-122">**Type**</span></span>|<span data-ttu-id="37d2b-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="37d2b-123">**Required**</span></span>|<span data-ttu-id="37d2b-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="37d2b-124">**Description**</span></span>|<span data-ttu-id="37d2b-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="37d2b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="37d2b-126">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="37d2b-126">Category</span></span>  <br/> |<span data-ttu-id="37d2b-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37d2b-127">xsd:string</span></span>  <br/> |<span data-ttu-id="37d2b-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="37d2b-128">optional</span></span>  <br/> ||<span data-ttu-id="37d2b-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d2b-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37d2b-130">説明</span><span class="sxs-lookup"><span data-stu-id="37d2b-130">Description</span></span>  <br/> |<span data-ttu-id="37d2b-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37d2b-131">xsd:string</span></span>  <br/> |<span data-ttu-id="37d2b-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="37d2b-132">optional</span></span>  <br/> ||<span data-ttu-id="37d2b-133">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d2b-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37d2b-134">ID</span><span class="sxs-lookup"><span data-stu-id="37d2b-134">ID</span></span>  <br/> |<span data-ttu-id="37d2b-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="37d2b-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="37d2b-136">必須</span><span class="sxs-lookup"><span data-stu-id="37d2b-136">required</span></span>  <br/> ||<span data-ttu-id="37d2b-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d2b-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="37d2b-138">無視</span><span class="sxs-lookup"><span data-stu-id="37d2b-138">Ignored</span></span>  <br/> |<span data-ttu-id="37d2b-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="37d2b-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="37d2b-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="37d2b-140">optional</span></span>  <br/> ||<span data-ttu-id="37d2b-141">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d2b-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="37d2b-142">NameU</span><span class="sxs-lookup"><span data-stu-id="37d2b-142">NameU</span></span>  <br/> |<span data-ttu-id="37d2b-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="37d2b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="37d2b-144">必須</span><span class="sxs-lookup"><span data-stu-id="37d2b-144">required</span></span>  <br/> ||<span data-ttu-id="37d2b-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d2b-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="37d2b-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="37d2b-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="37d2b-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="37d2b-147">xsd:int</span></span>  <br/> |<span data-ttu-id="37d2b-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="37d2b-148">optional</span></span>  <br/> ||<span data-ttu-id="37d2b-149">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="37d2b-149">Values of the xsd:int type.</span></span>  <br/> |
   

