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
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="d824d-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d824d-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d824d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d824d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d824d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d824d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d824d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d824d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d824d-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="d824d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d824d-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d824d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d824d-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d824d-109">定義</span><span class="sxs-lookup"><span data-stu-id="d824d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d824d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d824d-110">Elements and attributes</span></span>

<span data-ttu-id="d824d-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d824d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d824d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d824d-112">Child elements</span></span>

|<span data-ttu-id="d824d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d824d-113">**Element**</span></span>|<span data-ttu-id="d824d-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d824d-114">**Type**</span></span>|<span data-ttu-id="d824d-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d824d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d824d-116">Data1</span><span class="sxs-lookup"><span data-stu-id="d824d-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d824d-118">Data2</span><span class="sxs-lookup"><span data-stu-id="d824d-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d824d-120">Data3</span><span class="sxs-lookup"><span data-stu-id="d824d-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d824d-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="d824d-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d824d-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="d824d-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d824d-126">Text</span><span class="sxs-lookup"><span data-stu-id="d824d-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d824d-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="d824d-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d824d-128">属性</span><span class="sxs-lookup"><span data-stu-id="d824d-128">Attributes</span></span>

|<span data-ttu-id="d824d-129">**属性**</span><span class="sxs-lookup"><span data-stu-id="d824d-129">**Attribute**</span></span>|<span data-ttu-id="d824d-130">**型**</span><span class="sxs-lookup"><span data-stu-id="d824d-130">**Type**</span></span>|<span data-ttu-id="d824d-131">**必須**</span><span class="sxs-lookup"><span data-stu-id="d824d-131">**Required**</span></span>|<span data-ttu-id="d824d-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="d824d-132">**Description**</span></span>|<span data-ttu-id="d824d-133">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d824d-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d824d-134">Del</span><span class="sxs-lookup"><span data-stu-id="d824d-134">Del</span></span>  <br/> |<span data-ttu-id="d824d-135">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d824d-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d824d-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-136">optional</span></span>  <br/> ||<span data-ttu-id="d824d-137">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d824d-138">ID</span><span class="sxs-lookup"><span data-stu-id="d824d-138">ID</span></span>  <br/> |<span data-ttu-id="d824d-139">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d824d-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d824d-140">必須</span><span class="sxs-lookup"><span data-stu-id="d824d-140">required</span></span>  <br/> ||<span data-ttu-id="d824d-141">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d824d-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d824d-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="d824d-143">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d824d-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d824d-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-144">optional</span></span>  <br/> ||<span data-ttu-id="d824d-145">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d824d-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d824d-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d824d-147">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d824d-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d824d-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-148">optional</span></span>  <br/> ||<span data-ttu-id="d824d-149">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d824d-150">Master</span><span class="sxs-lookup"><span data-stu-id="d824d-150">Master</span></span>  <br/> |<span data-ttu-id="d824d-151">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d824d-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d824d-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-152">optional</span></span>  <br/> ||<span data-ttu-id="d824d-153">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d824d-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="d824d-154">MasterShape</span></span>  <br/> |<span data-ttu-id="d824d-155">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d824d-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d824d-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-156">optional</span></span>  <br/> ||<span data-ttu-id="d824d-157">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d824d-158">名前</span><span class="sxs-lookup"><span data-stu-id="d824d-158">Name</span></span>  <br/> |<span data-ttu-id="d824d-159">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d824d-159">xsd:string</span></span>  <br/> |<span data-ttu-id="d824d-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-160">optional</span></span>  <br/> ||<span data-ttu-id="d824d-161">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d824d-162">NameU</span><span class="sxs-lookup"><span data-stu-id="d824d-162">NameU</span></span>  <br/> |<span data-ttu-id="d824d-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d824d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d824d-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-164">optional</span></span>  <br/> ||<span data-ttu-id="d824d-165">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d824d-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="d824d-166">OriginalID</span></span>  <br/> |<span data-ttu-id="d824d-167">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d824d-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d824d-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-168">optional</span></span>  <br/> ||<span data-ttu-id="d824d-169">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d824d-170">型</span><span class="sxs-lookup"><span data-stu-id="d824d-170">Type</span></span>  <br/> |<span data-ttu-id="d824d-171">xsd: token</span><span class="sxs-lookup"><span data-stu-id="d824d-171">xsd:token</span></span>  <br/> |<span data-ttu-id="d824d-172">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-172">optional</span></span>  <br/> ||<span data-ttu-id="d824d-173">Xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="d824d-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="d824d-174">UniqueID</span></span>  <br/> |<span data-ttu-id="d824d-175">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d824d-175">xsd:string</span></span>  <br/> |<span data-ttu-id="d824d-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="d824d-176">optional</span></span>  <br/> ||<span data-ttu-id="d824d-177">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d824d-177">Values of the xsd:string type.</span></span>  <br/> |
   

