---
title: ShapeSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542059"
---
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="a91c0-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a91c0-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a91c0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a91c0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a91c0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a91c0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a91c0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a91c0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a91c0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a91c0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a91c0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a91c0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a91c0-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a91c0-109">定義</span><span class="sxs-lookup"><span data-stu-id="a91c0-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a91c0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a91c0-110">Elements and attributes</span></span>

<span data-ttu-id="a91c0-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a91c0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a91c0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a91c0-112">Child elements</span></span>

|<span data-ttu-id="a91c0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a91c0-113">**Element**</span></span>|<span data-ttu-id="a91c0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="a91c0-114">**Type**</span></span>|<span data-ttu-id="a91c0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a91c0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a91c0-116">Data1</span><span class="sxs-lookup"><span data-stu-id="a91c0-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a91c0-118">Data2</span><span class="sxs-lookup"><span data-stu-id="a91c0-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a91c0-120">Data3</span><span class="sxs-lookup"><span data-stu-id="a91c0-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a91c0-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="a91c0-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a91c0-124">図形</span><span class="sxs-lookup"><span data-stu-id="a91c0-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a91c0-126">Text</span><span class="sxs-lookup"><span data-stu-id="a91c0-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a91c0-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="a91c0-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a91c0-128">属性</span><span class="sxs-lookup"><span data-stu-id="a91c0-128">Attributes</span></span>

|<span data-ttu-id="a91c0-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="a91c0-129">**Attribute**</span></span>|<span data-ttu-id="a91c0-130">**型**</span><span class="sxs-lookup"><span data-stu-id="a91c0-130">**Type**</span></span>|<span data-ttu-id="a91c0-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="a91c0-131">**Required**</span></span>|<span data-ttu-id="a91c0-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="a91c0-132">**Description**</span></span>|<span data-ttu-id="a91c0-133">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a91c0-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a91c0-134">Del</span><span class="sxs-lookup"><span data-stu-id="a91c0-134">Del</span></span>  <br/> |<span data-ttu-id="a91c0-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a91c0-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a91c0-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-136">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-137">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-138">ID</span><span class="sxs-lookup"><span data-stu-id="a91c0-138">ID</span></span>  <br/> |<span data-ttu-id="a91c0-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a91c0-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a91c0-140">必須</span><span class="sxs-lookup"><span data-stu-id="a91c0-140">required</span></span>  <br/> ||<span data-ttu-id="a91c0-141">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a91c0-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="a91c0-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a91c0-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a91c0-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-144">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-145">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a91c0-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a91c0-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a91c0-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a91c0-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-148">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-149">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-150">Master</span><span class="sxs-lookup"><span data-stu-id="a91c0-150">Master</span></span>  <br/> |<span data-ttu-id="a91c0-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a91c0-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a91c0-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-152">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-153">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="a91c0-154">MasterShape</span></span>  <br/> |<span data-ttu-id="a91c0-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a91c0-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a91c0-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-156">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-157">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-158">名前</span><span class="sxs-lookup"><span data-stu-id="a91c0-158">Name</span></span>  <br/> |<span data-ttu-id="a91c0-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a91c0-159">xsd:string</span></span>  <br/> |<span data-ttu-id="a91c0-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-160">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-161">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-162">NameU</span><span class="sxs-lookup"><span data-stu-id="a91c0-162">NameU</span></span>  <br/> |<span data-ttu-id="a91c0-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a91c0-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a91c0-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-164">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-165">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="a91c0-166">OriginalID</span></span>  <br/> |<span data-ttu-id="a91c0-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a91c0-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a91c0-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-168">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-169">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-170">型</span><span class="sxs-lookup"><span data-stu-id="a91c0-170">Type</span></span>  <br/> |<span data-ttu-id="a91c0-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="a91c0-171">xsd:token</span></span>  <br/> |<span data-ttu-id="a91c0-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-172">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-173">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a91c0-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="a91c0-174">UniqueID</span></span>  <br/> |<span data-ttu-id="a91c0-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a91c0-175">xsd:string</span></span>  <br/> |<span data-ttu-id="a91c0-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="a91c0-176">optional</span></span>  <br/> ||<span data-ttu-id="a91c0-177">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a91c0-177">Values of the xsd:string type.</span></span>  <br/> |
   

