---
title: ForeignData_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384158"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="a95d8-102">ForeignData_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a95d8-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a95d8-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a95d8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a95d8-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a95d8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a95d8-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a95d8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a95d8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a95d8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a95d8-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a95d8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a95d8-108">なし</span><span class="sxs-lookup"><span data-stu-id="a95d8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a95d8-109">定義</span><span class="sxs-lookup"><span data-stu-id="a95d8-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a95d8-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a95d8-110">Elements and attributes</span></span>

<span data-ttu-id="a95d8-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a95d8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a95d8-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a95d8-112">Child elements</span></span>

|<span data-ttu-id="a95d8-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="a95d8-113">**Element**</span></span>|<span data-ttu-id="a95d8-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a95d8-114">**Type**</span></span>|<span data-ttu-id="a95d8-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a95d8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a95d8-116">Rel</span><span class="sxs-lookup"><span data-stu-id="a95d8-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a95d8-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a95d8-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a95d8-118">属性</span><span class="sxs-lookup"><span data-stu-id="a95d8-118">Attributes</span></span>

|<span data-ttu-id="a95d8-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="a95d8-119">**Attribute**</span></span>|<span data-ttu-id="a95d8-120">**型**</span><span class="sxs-lookup"><span data-stu-id="a95d8-120">**Type**</span></span>|<span data-ttu-id="a95d8-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="a95d8-121">**Required**</span></span>|<span data-ttu-id="a95d8-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="a95d8-122">**Description**</span></span>|<span data-ttu-id="a95d8-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a95d8-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a95d8-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="a95d8-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="a95d8-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="a95d8-125">xsd:double</span></span>  <br/> |<span data-ttu-id="a95d8-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-126">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-127">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="a95d8-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="a95d8-128">CompressionType</span></span>  <br/> |<span data-ttu-id="a95d8-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="a95d8-129">xsd:token</span></span>  <br/> |<span data-ttu-id="a95d8-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-130">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-131">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95d8-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="a95d8-132">ExtentX</span></span>  <br/> |<span data-ttu-id="a95d8-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="a95d8-133">xsd:double</span></span>  <br/> |<span data-ttu-id="a95d8-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-134">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-135">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="a95d8-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="a95d8-136">ExtentY</span></span>  <br/> |<span data-ttu-id="a95d8-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="a95d8-137">xsd:double</span></span>  <br/> |<span data-ttu-id="a95d8-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-138">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-139">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="a95d8-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="a95d8-140">ForeignType</span></span>  <br/> |<span data-ttu-id="a95d8-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="a95d8-141">xsd:token</span></span>  <br/> |<span data-ttu-id="a95d8-142">必須</span><span class="sxs-lookup"><span data-stu-id="a95d8-142">required</span></span>  <br/> ||<span data-ttu-id="a95d8-143">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95d8-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="a95d8-144">MappingMode</span></span>  <br/> |<span data-ttu-id="a95d8-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a95d8-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a95d8-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-146">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-147">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95d8-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="a95d8-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="a95d8-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="a95d8-149">xsd:double</span></span>  <br/> |<span data-ttu-id="a95d8-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-150">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-151">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="a95d8-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="a95d8-152">ObjectType</span></span>  <br/> |<span data-ttu-id="a95d8-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a95d8-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a95d8-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-154">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95d8-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="a95d8-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="a95d8-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="a95d8-157">xsd:double</span></span>  <br/> |<span data-ttu-id="a95d8-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-158">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-159">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="a95d8-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a95d8-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="a95d8-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="a95d8-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a95d8-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a95d8-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="a95d8-162">optional</span></span>  <br/> ||<span data-ttu-id="a95d8-163">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a95d8-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

