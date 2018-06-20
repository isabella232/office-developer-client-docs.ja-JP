---
title: DocumentSettings_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 93623133e7d7fd096e063f0d9d5227d65dcc4736
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805276"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="50b8c-102">DocumentSettings_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="50b8c-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="50b8c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="50b8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50b8c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="50b8c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="50b8c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="50b8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="50b8c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="50b8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="50b8c-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="50b8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="50b8c-108">なし</span><span class="sxs-lookup"><span data-stu-id="50b8c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50b8c-109">定義</span><span class="sxs-lookup"><span data-stu-id="50b8c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="50b8c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="50b8c-110">Elements and attributes</span></span>

<span data-ttu-id="50b8c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="50b8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="50b8c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="50b8c-112">Child elements</span></span>

|<span data-ttu-id="50b8c-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="50b8c-113">**Element**</span></span>|<span data-ttu-id="50b8c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="50b8c-114">**Type**</span></span>|<span data-ttu-id="50b8c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="50b8c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50b8c-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="50b8c-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="50b8c-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="50b8c-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="50b8c-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="50b8c-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="50b8c-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="50b8c-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="50b8c-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="50b8c-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="50b8c-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="50b8c-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="50b8c-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="50b8c-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50b8c-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="50b8c-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="50b8c-140">属性</span><span class="sxs-lookup"><span data-stu-id="50b8c-140">Attributes</span></span>

|<span data-ttu-id="50b8c-141">**属性**</span><span class="sxs-lookup"><span data-stu-id="50b8c-141">**Attribute**</span></span>|<span data-ttu-id="50b8c-142">**型**</span><span class="sxs-lookup"><span data-stu-id="50b8c-142">**Type**</span></span>|<span data-ttu-id="50b8c-143">**必須**</span><span class="sxs-lookup"><span data-stu-id="50b8c-143">**Required**</span></span>|<span data-ttu-id="50b8c-144">**説明**</span><span class="sxs-lookup"><span data-stu-id="50b8c-144">**Description**</span></span>|<span data-ttu-id="50b8c-145">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="50b8c-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="50b8c-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="50b8c-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="50b8c-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50b8c-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50b8c-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="50b8c-148">optional</span></span>  <br/> ||<span data-ttu-id="50b8c-149">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="50b8c-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="50b8c-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="50b8c-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="50b8c-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50b8c-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50b8c-152">省略可能</span><span class="sxs-lookup"><span data-stu-id="50b8c-152">optional</span></span>  <br/> ||<span data-ttu-id="50b8c-153">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="50b8c-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="50b8c-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="50b8c-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="50b8c-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50b8c-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50b8c-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="50b8c-156">optional</span></span>  <br/> ||<span data-ttu-id="50b8c-157">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="50b8c-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="50b8c-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="50b8c-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="50b8c-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50b8c-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50b8c-160">省略可能</span><span class="sxs-lookup"><span data-stu-id="50b8c-160">optional</span></span>  <br/> ||<span data-ttu-id="50b8c-161">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="50b8c-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="50b8c-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="50b8c-162">TopPage</span></span>  <br/> |<span data-ttu-id="50b8c-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="50b8c-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="50b8c-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="50b8c-164">optional</span></span>  <br/> ||<span data-ttu-id="50b8c-165">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="50b8c-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

