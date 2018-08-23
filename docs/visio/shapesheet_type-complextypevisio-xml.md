---
title: ShapeSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806425"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="03b7f-102">ShapeSheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="03b7f-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="03b7f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="03b7f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03b7f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="03b7f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="03b7f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="03b7f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="03b7f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="03b7f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="03b7f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="03b7f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="03b7f-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="03b7f-109">定義</span><span class="sxs-lookup"><span data-stu-id="03b7f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="03b7f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="03b7f-110">Elements and attributes</span></span>

<span data-ttu-id="03b7f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="03b7f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="03b7f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="03b7f-112">Child elements</span></span>

|<span data-ttu-id="03b7f-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="03b7f-113">**Element**</span></span>|<span data-ttu-id="03b7f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="03b7f-114">**Type**</span></span>|<span data-ttu-id="03b7f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="03b7f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="03b7f-116">Data1</span><span class="sxs-lookup"><span data-stu-id="03b7f-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="03b7f-118">Data2</span><span class="sxs-lookup"><span data-stu-id="03b7f-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="03b7f-120">Data3</span><span class="sxs-lookup"><span data-stu-id="03b7f-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="03b7f-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="03b7f-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="03b7f-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="03b7f-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="03b7f-126">Text</span><span class="sxs-lookup"><span data-stu-id="03b7f-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03b7f-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="03b7f-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="03b7f-128">属性</span><span class="sxs-lookup"><span data-stu-id="03b7f-128">Attributes</span></span>

|<span data-ttu-id="03b7f-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="03b7f-129">**Attribute**</span></span>|<span data-ttu-id="03b7f-130">**型**</span><span class="sxs-lookup"><span data-stu-id="03b7f-130">**Type**</span></span>|<span data-ttu-id="03b7f-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="03b7f-131">**Required**</span></span>|<span data-ttu-id="03b7f-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="03b7f-132">**Description**</span></span>|<span data-ttu-id="03b7f-133">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="03b7f-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="03b7f-134">Del</span><span class="sxs-lookup"><span data-stu-id="03b7f-134">Del</span></span>  <br/> |<span data-ttu-id="03b7f-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="03b7f-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="03b7f-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-136">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-137">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-138">ID</span><span class="sxs-lookup"><span data-stu-id="03b7f-138">ID</span></span>  <br/> |<span data-ttu-id="03b7f-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="03b7f-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03b7f-140">必須</span><span class="sxs-lookup"><span data-stu-id="03b7f-140">required</span></span>  <br/> ||<span data-ttu-id="03b7f-141">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="03b7f-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="03b7f-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="03b7f-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="03b7f-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-144">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-145">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="03b7f-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="03b7f-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="03b7f-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="03b7f-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-148">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-149">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-150">Master</span><span class="sxs-lookup"><span data-stu-id="03b7f-150">Master</span></span>  <br/> |<span data-ttu-id="03b7f-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="03b7f-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03b7f-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-152">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-153">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="03b7f-154">MasterShape</span></span>  <br/> |<span data-ttu-id="03b7f-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="03b7f-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03b7f-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-156">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-157">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-158">名前</span><span class="sxs-lookup"><span data-stu-id="03b7f-158">Name</span></span>  <br/> |<span data-ttu-id="03b7f-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="03b7f-159">xsd:string</span></span>  <br/> |<span data-ttu-id="03b7f-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-160">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-161">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-162">NameU</span><span class="sxs-lookup"><span data-stu-id="03b7f-162">NameU</span></span>  <br/> |<span data-ttu-id="03b7f-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="03b7f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="03b7f-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-164">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-165">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="03b7f-166">OriginalID</span></span>  <br/> |<span data-ttu-id="03b7f-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="03b7f-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03b7f-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-168">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-169">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-170">型</span><span class="sxs-lookup"><span data-stu-id="03b7f-170">Type</span></span>  <br/> |<span data-ttu-id="03b7f-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="03b7f-171">xsd:token</span></span>  <br/> |<span data-ttu-id="03b7f-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-172">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-173">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="03b7f-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="03b7f-174">UniqueID</span></span>  <br/> |<span data-ttu-id="03b7f-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="03b7f-175">xsd:string</span></span>  <br/> |<span data-ttu-id="03b7f-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="03b7f-176">optional</span></span>  <br/> ||<span data-ttu-id="03b7f-177">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03b7f-177">Values of the xsd:string type.</span></span>  <br/> |
   

