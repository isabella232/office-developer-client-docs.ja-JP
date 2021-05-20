---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539864"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="bdb28-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bdb28-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bdb28-103">型情報</span><span class="sxs-lookup"><span data-stu-id="bdb28-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdb28-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bdb28-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bdb28-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bdb28-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bdb28-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bdb28-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bdb28-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bdb28-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bdb28-108">なし</span><span class="sxs-lookup"><span data-stu-id="bdb28-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bdb28-109">定義</span><span class="sxs-lookup"><span data-stu-id="bdb28-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bdb28-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bdb28-110">Elements and attributes</span></span>

<span data-ttu-id="bdb28-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdb28-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bdb28-112">子要素</span><span class="sxs-lookup"><span data-stu-id="bdb28-112">Child elements</span></span>

|<span data-ttu-id="bdb28-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdb28-113">**Element**</span></span>|<span data-ttu-id="bdb28-114">**型**</span><span class="sxs-lookup"><span data-stu-id="bdb28-114">**Type**</span></span>|<span data-ttu-id="bdb28-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="bdb28-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bdb28-116">Rel</span><span class="sxs-lookup"><span data-stu-id="bdb28-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bdb28-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="bdb28-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bdb28-118">属性</span><span class="sxs-lookup"><span data-stu-id="bdb28-118">Attributes</span></span>

|<span data-ttu-id="bdb28-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="bdb28-119">**Attribute**</span></span>|<span data-ttu-id="bdb28-120">**型**</span><span class="sxs-lookup"><span data-stu-id="bdb28-120">**Type**</span></span>|<span data-ttu-id="bdb28-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="bdb28-121">**Required**</span></span>|<span data-ttu-id="bdb28-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="bdb28-122">**Description**</span></span>|<span data-ttu-id="bdb28-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bdb28-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bdb28-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="bdb28-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="bdb28-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="bdb28-125">xsd:double</span></span>  <br/> |<span data-ttu-id="bdb28-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-126">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-127">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="bdb28-128">CompressionType</span></span>  <br/> |<span data-ttu-id="bdb28-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="bdb28-129">xsd:token</span></span>  <br/> |<span data-ttu-id="bdb28-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-130">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-131">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="bdb28-132">ExtentX</span></span>  <br/> |<span data-ttu-id="bdb28-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="bdb28-133">xsd:double</span></span>  <br/> |<span data-ttu-id="bdb28-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-134">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-135">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="bdb28-136">ExtentY</span></span>  <br/> |<span data-ttu-id="bdb28-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="bdb28-137">xsd:double</span></span>  <br/> |<span data-ttu-id="bdb28-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-138">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-139">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="bdb28-140">ForeignType</span></span>  <br/> |<span data-ttu-id="bdb28-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="bdb28-141">xsd:token</span></span>  <br/> |<span data-ttu-id="bdb28-142">必須</span><span class="sxs-lookup"><span data-stu-id="bdb28-142">required</span></span>  <br/> ||<span data-ttu-id="bdb28-143">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="bdb28-144">MappingMode</span></span>  <br/> |<span data-ttu-id="bdb28-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb28-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb28-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-146">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-147">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="bdb28-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="bdb28-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="bdb28-149">xsd:double</span></span>  <br/> |<span data-ttu-id="bdb28-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-150">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-151">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="bdb28-152">ObjectType</span></span>  <br/> |<span data-ttu-id="bdb28-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bdb28-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bdb28-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-154">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-155">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="bdb28-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="bdb28-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="bdb28-157">xsd:double</span></span>  <br/> |<span data-ttu-id="bdb28-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-158">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-159">xsd:double 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="bdb28-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="bdb28-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="bdb28-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="bdb28-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bdb28-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="bdb28-162">optional</span></span>  <br/> ||<span data-ttu-id="bdb28-163">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="bdb28-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

