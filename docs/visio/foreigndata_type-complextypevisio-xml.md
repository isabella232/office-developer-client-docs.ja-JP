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
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="36cdd-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="36cdd-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="36cdd-103">型情報</span><span class="sxs-lookup"><span data-stu-id="36cdd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36cdd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="36cdd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="36cdd-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="36cdd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="36cdd-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="36cdd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="36cdd-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="36cdd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="36cdd-108">None</span><span class="sxs-lookup"><span data-stu-id="36cdd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="36cdd-109">定義</span><span class="sxs-lookup"><span data-stu-id="36cdd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="36cdd-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="36cdd-110">Elements and attributes</span></span>

<span data-ttu-id="36cdd-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36cdd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="36cdd-112">子要素</span><span class="sxs-lookup"><span data-stu-id="36cdd-112">Child elements</span></span>

|<span data-ttu-id="36cdd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="36cdd-113">**Element**</span></span>|<span data-ttu-id="36cdd-114">**型**</span><span class="sxs-lookup"><span data-stu-id="36cdd-114">**Type**</span></span>|<span data-ttu-id="36cdd-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="36cdd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="36cdd-116">Rel</span><span class="sxs-lookup"><span data-stu-id="36cdd-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="36cdd-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="36cdd-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="36cdd-118">属性</span><span class="sxs-lookup"><span data-stu-id="36cdd-118">Attributes</span></span>

|<span data-ttu-id="36cdd-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="36cdd-119">**Attribute**</span></span>|<span data-ttu-id="36cdd-120">**型**</span><span class="sxs-lookup"><span data-stu-id="36cdd-120">**Type**</span></span>|<span data-ttu-id="36cdd-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="36cdd-121">**Required**</span></span>|<span data-ttu-id="36cdd-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="36cdd-122">**Description**</span></span>|<span data-ttu-id="36cdd-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="36cdd-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="36cdd-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="36cdd-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="36cdd-125">xsd: double</span><span class="sxs-lookup"><span data-stu-id="36cdd-125">xsd:double</span></span>  <br/> |<span data-ttu-id="36cdd-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-126">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-127">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="36cdd-128">CompressionType</span></span>  <br/> |<span data-ttu-id="36cdd-129">xsd: token</span><span class="sxs-lookup"><span data-stu-id="36cdd-129">xsd:token</span></span>  <br/> |<span data-ttu-id="36cdd-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-130">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-131">Xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="36cdd-132">ExtentX</span></span>  <br/> |<span data-ttu-id="36cdd-133">xsd: double</span><span class="sxs-lookup"><span data-stu-id="36cdd-133">xsd:double</span></span>  <br/> |<span data-ttu-id="36cdd-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-134">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-135">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="36cdd-136">ExtentY</span></span>  <br/> |<span data-ttu-id="36cdd-137">xsd: double</span><span class="sxs-lookup"><span data-stu-id="36cdd-137">xsd:double</span></span>  <br/> |<span data-ttu-id="36cdd-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-138">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-139">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="36cdd-140">ForeignType</span></span>  <br/> |<span data-ttu-id="36cdd-141">xsd: token</span><span class="sxs-lookup"><span data-stu-id="36cdd-141">xsd:token</span></span>  <br/> |<span data-ttu-id="36cdd-142">必須</span><span class="sxs-lookup"><span data-stu-id="36cdd-142">required</span></span>  <br/> ||<span data-ttu-id="36cdd-143">Xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="36cdd-144">MappingMode</span></span>  <br/> |<span data-ttu-id="36cdd-145">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="36cdd-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="36cdd-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-146">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-147">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="36cdd-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="36cdd-149">xsd: double</span><span class="sxs-lookup"><span data-stu-id="36cdd-149">xsd:double</span></span>  <br/> |<span data-ttu-id="36cdd-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-150">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-151">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="36cdd-152">ObjectType</span></span>  <br/> |<span data-ttu-id="36cdd-153">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="36cdd-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="36cdd-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-154">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-155">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="36cdd-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="36cdd-157">xsd: double</span><span class="sxs-lookup"><span data-stu-id="36cdd-157">xsd:double</span></span>  <br/> |<span data-ttu-id="36cdd-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-158">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-159">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="36cdd-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="36cdd-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="36cdd-161">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="36cdd-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="36cdd-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="36cdd-162">optional</span></span>  <br/> ||<span data-ttu-id="36cdd-163">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="36cdd-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

