---
title: DocumentSettings_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 704591a2bf03f3eaf4d93b167475a8bae286da3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349036"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="45118-102">DocumentSettings_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="45118-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="45118-103">型情報</span><span class="sxs-lookup"><span data-stu-id="45118-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45118-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="45118-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="45118-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="45118-105">**Schema file**</span></span> <br/> |<span data-ttu-id="45118-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="45118-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="45118-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="45118-107">**Extension base**</span></span> <br/> |<span data-ttu-id="45118-108">なし</span><span class="sxs-lookup"><span data-stu-id="45118-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="45118-109">定義</span><span class="sxs-lookup"><span data-stu-id="45118-109">Definition</span></span>

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="45118-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="45118-110">Elements and attributes</span></span>

<span data-ttu-id="45118-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="45118-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="45118-112">子要素</span><span class="sxs-lookup"><span data-stu-id="45118-112">Child elements</span></span>

|<span data-ttu-id="45118-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="45118-113">**Element**</span></span>|<span data-ttu-id="45118-114">**型**</span><span class="sxs-lookup"><span data-stu-id="45118-114">**Type**</span></span>|<span data-ttu-id="45118-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="45118-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="45118-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="45118-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="45118-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="45118-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="45118-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="45118-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="45118-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="45118-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="45118-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="45118-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="45118-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="45118-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="45118-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="45118-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="45118-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="45118-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="45118-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="45118-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="45118-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="45118-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="45118-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="45118-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="45118-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="45118-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="45118-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="45118-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="45118-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="45118-140">属性</span><span class="sxs-lookup"><span data-stu-id="45118-140">Attributes</span></span>

|<span data-ttu-id="45118-141">**属性**</span><span class="sxs-lookup"><span data-stu-id="45118-141">**Attribute**</span></span>|<span data-ttu-id="45118-142">**型**</span><span class="sxs-lookup"><span data-stu-id="45118-142">**Type**</span></span>|<span data-ttu-id="45118-143">**必須**</span><span class="sxs-lookup"><span data-stu-id="45118-143">**Required**</span></span>|<span data-ttu-id="45118-144">**説明**</span><span class="sxs-lookup"><span data-stu-id="45118-144">**Description**</span></span>|<span data-ttu-id="45118-145">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="45118-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="45118-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="45118-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="45118-147">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="45118-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45118-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="45118-148">optional</span></span>  <br/> ||<span data-ttu-id="45118-149">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="45118-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45118-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="45118-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="45118-151">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="45118-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45118-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="45118-152">optional</span></span>  <br/> ||<span data-ttu-id="45118-153">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="45118-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45118-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="45118-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="45118-155">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="45118-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45118-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="45118-156">optional</span></span>  <br/> ||<span data-ttu-id="45118-157">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="45118-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45118-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="45118-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="45118-159">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="45118-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45118-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="45118-160">optional</span></span>  <br/> ||<span data-ttu-id="45118-161">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="45118-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="45118-162">toppage</span><span class="sxs-lookup"><span data-stu-id="45118-162">TopPage</span></span>  <br/> |<span data-ttu-id="45118-163">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="45118-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="45118-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="45118-164">optional</span></span>  <br/> ||<span data-ttu-id="45118-165">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="45118-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

