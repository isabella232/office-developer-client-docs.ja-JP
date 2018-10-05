---
title: Rule_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: 9af47c47137e51f7189dd3f845d7bd8f35297f0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393510"
---
# <a name="ruletype-complextype-visio-xml"></a><span data-ttu-id="ad328-102">Rule_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ad328-102">Rule_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ad328-103">型情報</span><span class="sxs-lookup"><span data-stu-id="ad328-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad328-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ad328-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ad328-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad328-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ad328-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ad328-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ad328-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="ad328-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ad328-108">なし</span><span class="sxs-lookup"><span data-stu-id="ad328-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad328-109">定義</span><span class="sxs-lookup"><span data-stu-id="ad328-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ad328-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ad328-110">Elements and attributes</span></span>

<span data-ttu-id="ad328-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad328-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ad328-112">子要素</span><span class="sxs-lookup"><span data-stu-id="ad328-112">Child elements</span></span>

|<span data-ttu-id="ad328-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="ad328-113">**Element**</span></span>|<span data-ttu-id="ad328-114">**型**</span><span class="sxs-lookup"><span data-stu-id="ad328-114">**Type**</span></span>|<span data-ttu-id="ad328-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad328-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad328-116">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="ad328-116">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad328-117">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="ad328-117">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ad328-118">RuleTest</span><span class="sxs-lookup"><span data-stu-id="ad328-118">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad328-119">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="ad328-119">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ad328-120">属性</span><span class="sxs-lookup"><span data-stu-id="ad328-120">Attributes</span></span>

|<span data-ttu-id="ad328-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="ad328-121">**Attribute**</span></span>|<span data-ttu-id="ad328-122">**型**</span><span class="sxs-lookup"><span data-stu-id="ad328-122">**Type**</span></span>|<span data-ttu-id="ad328-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="ad328-123">**Required**</span></span>|<span data-ttu-id="ad328-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad328-124">**Description**</span></span>|<span data-ttu-id="ad328-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="ad328-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad328-126">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="ad328-126">Category</span></span>  <br/> |<span data-ttu-id="ad328-127">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad328-127">xsd:string</span></span>  <br/> |<span data-ttu-id="ad328-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad328-128">optional</span></span>  <br/> ||<span data-ttu-id="ad328-129">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad328-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad328-130">説明</span><span class="sxs-lookup"><span data-stu-id="ad328-130">Description</span></span>  <br/> |<span data-ttu-id="ad328-131">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad328-131">xsd:string</span></span>  <br/> |<span data-ttu-id="ad328-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad328-132">optional</span></span>  <br/> ||<span data-ttu-id="ad328-133">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad328-133">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad328-134">ID</span><span class="sxs-lookup"><span data-stu-id="ad328-134">ID</span></span>  <br/> |<span data-ttu-id="ad328-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad328-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad328-136">必須</span><span class="sxs-lookup"><span data-stu-id="ad328-136">required</span></span>  <br/> ||<span data-ttu-id="ad328-137">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad328-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ad328-138">無視</span><span class="sxs-lookup"><span data-stu-id="ad328-138">Ignored</span></span>  <br/> |<span data-ttu-id="ad328-139">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ad328-139">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ad328-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad328-140">optional</span></span>  <br/> ||<span data-ttu-id="ad328-141">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad328-141">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ad328-142">NameU</span><span class="sxs-lookup"><span data-stu-id="ad328-142">NameU</span></span>  <br/> |<span data-ttu-id="ad328-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ad328-143">xsd:string</span></span>  <br/> |<span data-ttu-id="ad328-144">必須</span><span class="sxs-lookup"><span data-stu-id="ad328-144">required</span></span>  <br/> ||<span data-ttu-id="ad328-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad328-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ad328-146">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="ad328-146">RuleTarget</span></span>  <br/> |<span data-ttu-id="ad328-147">xsd:int</span><span class="sxs-lookup"><span data-stu-id="ad328-147">xsd:int</span></span>  <br/> |<span data-ttu-id="ad328-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="ad328-148">optional</span></span>  <br/> ||<span data-ttu-id="ad328-149">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="ad328-149">Values of the xsd:int type.</span></span>  <br/> |
   

