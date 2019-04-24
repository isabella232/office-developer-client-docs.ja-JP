---
title: ForeignData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346012"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="cbb16-102">ForeignData_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cbb16-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cbb16-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cbb16-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbb16-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cbb16-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cbb16-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cbb16-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cbb16-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="cbb16-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cbb16-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cbb16-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cbb16-108">なし</span><span class="sxs-lookup"><span data-stu-id="cbb16-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cbb16-109">定義</span><span class="sxs-lookup"><span data-stu-id="cbb16-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cbb16-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cbb16-110">Elements and attributes</span></span>

<span data-ttu-id="cbb16-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbb16-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cbb16-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cbb16-112">Child elements</span></span>

|<span data-ttu-id="cbb16-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cbb16-113">**Element**</span></span>|<span data-ttu-id="cbb16-114">**型**</span><span class="sxs-lookup"><span data-stu-id="cbb16-114">**Type**</span></span>|<span data-ttu-id="cbb16-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="cbb16-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cbb16-116">Rel</span><span class="sxs-lookup"><span data-stu-id="cbb16-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cbb16-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="cbb16-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cbb16-118">属性</span><span class="sxs-lookup"><span data-stu-id="cbb16-118">Attributes</span></span>

|<span data-ttu-id="cbb16-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="cbb16-119">**Attribute**</span></span>|<span data-ttu-id="cbb16-120">**型**</span><span class="sxs-lookup"><span data-stu-id="cbb16-120">**Type**</span></span>|<span data-ttu-id="cbb16-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="cbb16-121">**Required**</span></span>|<span data-ttu-id="cbb16-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="cbb16-122">**Description**</span></span>|<span data-ttu-id="cbb16-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="cbb16-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cbb16-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="cbb16-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="cbb16-125">xsd: double</span><span class="sxs-lookup"><span data-stu-id="cbb16-125">xsd:double</span></span>  <br/> |<span data-ttu-id="cbb16-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-126">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-127">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="cbb16-128">CompressionType</span></span>  <br/> |<span data-ttu-id="cbb16-129">xsd: token</span><span class="sxs-lookup"><span data-stu-id="cbb16-129">xsd:token</span></span>  <br/> |<span data-ttu-id="cbb16-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-130">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-131">xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="cbb16-132">ExtentX</span></span>  <br/> |<span data-ttu-id="cbb16-133">xsd: double</span><span class="sxs-lookup"><span data-stu-id="cbb16-133">xsd:double</span></span>  <br/> |<span data-ttu-id="cbb16-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-134">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-135">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="cbb16-136">ExtentY</span></span>  <br/> |<span data-ttu-id="cbb16-137">xsd: double</span><span class="sxs-lookup"><span data-stu-id="cbb16-137">xsd:double</span></span>  <br/> |<span data-ttu-id="cbb16-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-138">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-139">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="cbb16-140">ForeignType</span></span>  <br/> |<span data-ttu-id="cbb16-141">xsd: token</span><span class="sxs-lookup"><span data-stu-id="cbb16-141">xsd:token</span></span>  <br/> |<span data-ttu-id="cbb16-142">必須</span><span class="sxs-lookup"><span data-stu-id="cbb16-142">required</span></span>  <br/> ||<span data-ttu-id="cbb16-143">xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-144">mappingmode</span><span class="sxs-lookup"><span data-stu-id="cbb16-144">MappingMode</span></span>  <br/> |<span data-ttu-id="cbb16-145">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="cbb16-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cbb16-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-146">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-147">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="cbb16-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="cbb16-149">xsd: double</span><span class="sxs-lookup"><span data-stu-id="cbb16-149">xsd:double</span></span>  <br/> |<span data-ttu-id="cbb16-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-150">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-151">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="cbb16-152">ObjectType</span></span>  <br/> |<span data-ttu-id="cbb16-153">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="cbb16-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cbb16-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-154">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-155">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-156">objectwidth</span><span class="sxs-lookup"><span data-stu-id="cbb16-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="cbb16-157">xsd: double</span><span class="sxs-lookup"><span data-stu-id="cbb16-157">xsd:double</span></span>  <br/> |<span data-ttu-id="cbb16-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-158">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-159">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="cbb16-160">showasicon</span><span class="sxs-lookup"><span data-stu-id="cbb16-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="cbb16-161">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="cbb16-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cbb16-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="cbb16-162">optional</span></span>  <br/> ||<span data-ttu-id="cbb16-163">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="cbb16-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

