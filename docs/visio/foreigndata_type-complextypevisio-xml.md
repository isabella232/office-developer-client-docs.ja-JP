---
title: ForeignData_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805442"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="6db30-102">ForeignData_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6db30-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6db30-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6db30-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6db30-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6db30-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6db30-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6db30-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6db30-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6db30-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6db30-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="6db30-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6db30-108">なし</span><span class="sxs-lookup"><span data-stu-id="6db30-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6db30-109">定義</span><span class="sxs-lookup"><span data-stu-id="6db30-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6db30-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6db30-110">Elements and attributes</span></span>

<span data-ttu-id="6db30-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6db30-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6db30-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6db30-112">Child elements</span></span>

|<span data-ttu-id="6db30-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="6db30-113">**Element**</span></span>|<span data-ttu-id="6db30-114">**型**</span><span class="sxs-lookup"><span data-stu-id="6db30-114">**Type**</span></span>|<span data-ttu-id="6db30-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="6db30-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6db30-116">Rel</span><span class="sxs-lookup"><span data-stu-id="6db30-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6db30-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6db30-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6db30-118">属性</span><span class="sxs-lookup"><span data-stu-id="6db30-118">Attributes</span></span>

|<span data-ttu-id="6db30-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="6db30-119">**Attribute**</span></span>|<span data-ttu-id="6db30-120">**型**</span><span class="sxs-lookup"><span data-stu-id="6db30-120">**Type**</span></span>|<span data-ttu-id="6db30-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="6db30-121">**Required**</span></span>|<span data-ttu-id="6db30-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="6db30-122">**Description**</span></span>|<span data-ttu-id="6db30-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6db30-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6db30-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="6db30-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="6db30-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6db30-125">xsd:double</span></span>  <br/> |<span data-ttu-id="6db30-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-126">optional</span></span>  <br/> ||<span data-ttu-id="6db30-127">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6db30-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6db30-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="6db30-128">CompressionType</span></span>  <br/> |<span data-ttu-id="6db30-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6db30-129">xsd:token</span></span>  <br/> |<span data-ttu-id="6db30-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-130">optional</span></span>  <br/> ||<span data-ttu-id="6db30-131">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6db30-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6db30-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="6db30-132">ExtentX</span></span>  <br/> |<span data-ttu-id="6db30-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6db30-133">xsd:double</span></span>  <br/> |<span data-ttu-id="6db30-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-134">optional</span></span>  <br/> ||<span data-ttu-id="6db30-135">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6db30-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6db30-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="6db30-136">ExtentY</span></span>  <br/> |<span data-ttu-id="6db30-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6db30-137">xsd:double</span></span>  <br/> |<span data-ttu-id="6db30-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-138">optional</span></span>  <br/> ||<span data-ttu-id="6db30-139">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6db30-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6db30-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="6db30-140">ForeignType</span></span>  <br/> |<span data-ttu-id="6db30-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6db30-141">xsd:token</span></span>  <br/> |<span data-ttu-id="6db30-142">必須</span><span class="sxs-lookup"><span data-stu-id="6db30-142">required</span></span>  <br/> ||<span data-ttu-id="6db30-143">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6db30-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6db30-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="6db30-144">MappingMode</span></span>  <br/> |<span data-ttu-id="6db30-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6db30-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6db30-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-146">optional</span></span>  <br/> ||<span data-ttu-id="6db30-147">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6db30-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6db30-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="6db30-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="6db30-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6db30-149">xsd:double</span></span>  <br/> |<span data-ttu-id="6db30-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-150">optional</span></span>  <br/> ||<span data-ttu-id="6db30-151">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6db30-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6db30-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="6db30-152">ObjectType</span></span>  <br/> |<span data-ttu-id="6db30-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6db30-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6db30-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-154">optional</span></span>  <br/> ||<span data-ttu-id="6db30-155">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6db30-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6db30-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="6db30-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="6db30-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6db30-157">xsd:double</span></span>  <br/> |<span data-ttu-id="6db30-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-158">optional</span></span>  <br/> ||<span data-ttu-id="6db30-159">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="6db30-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6db30-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="6db30-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="6db30-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6db30-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6db30-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="6db30-162">optional</span></span>  <br/> ||<span data-ttu-id="6db30-163">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6db30-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

