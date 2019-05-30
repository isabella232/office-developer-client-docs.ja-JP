---
title: Window_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538453"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="d5a18-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d5a18-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d5a18-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d5a18-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5a18-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5a18-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5a18-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d5a18-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5a18-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="d5a18-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5a18-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d5a18-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5a18-108">None</span><span class="sxs-lookup"><span data-stu-id="d5a18-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5a18-109">定義</span><span class="sxs-lookup"><span data-stu-id="d5a18-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
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
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5a18-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d5a18-110">Elements and attributes</span></span>

<span data-ttu-id="d5a18-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5a18-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5a18-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d5a18-112">Child elements</span></span>

|<span data-ttu-id="d5a18-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5a18-113">**Element**</span></span>|<span data-ttu-id="d5a18-114">**型**</span><span class="sxs-lookup"><span data-stu-id="d5a18-114">**Type**</span></span>|<span data-ttu-id="d5a18-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5a18-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5a18-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="d5a18-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="d5a18-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="d5a18-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="d5a18-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="d5a18-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="d5a18-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="d5a18-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="d5a18-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="d5a18-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="d5a18-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="d5a18-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="d5a18-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d5a18-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="d5a18-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5a18-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="d5a18-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d5a18-142">属性</span><span class="sxs-lookup"><span data-stu-id="d5a18-142">Attributes</span></span>

|<span data-ttu-id="d5a18-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="d5a18-143">**Attribute**</span></span>|<span data-ttu-id="d5a18-144">**型**</span><span class="sxs-lookup"><span data-stu-id="d5a18-144">**Type**</span></span>|<span data-ttu-id="d5a18-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="d5a18-145">**Required**</span></span>|<span data-ttu-id="d5a18-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5a18-146">**Description**</span></span>|<span data-ttu-id="d5a18-147">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d5a18-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5a18-148">Container</span><span class="sxs-lookup"><span data-stu-id="d5a18-148">Container</span></span>  <br/> |<span data-ttu-id="d5a18-149">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-150">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-151">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="d5a18-152">ContainerType</span></span>  <br/> |<span data-ttu-id="d5a18-153">xsd: token</span><span class="sxs-lookup"><span data-stu-id="d5a18-153">xsd:token</span></span>  <br/> |<span data-ttu-id="d5a18-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-154">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-155">Xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-156">Document</span><span class="sxs-lookup"><span data-stu-id="d5a18-156">Document</span></span>  <br/> |<span data-ttu-id="d5a18-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d5a18-157">xsd:string</span></span>  <br/> |<span data-ttu-id="d5a18-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-158">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-159">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-160">ID</span><span class="sxs-lookup"><span data-stu-id="d5a18-160">ID</span></span>  <br/> |<span data-ttu-id="d5a18-161">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-162">必須</span><span class="sxs-lookup"><span data-stu-id="d5a18-162">required</span></span>  <br/> ||<span data-ttu-id="d5a18-163">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-164">Master</span><span class="sxs-lookup"><span data-stu-id="d5a18-164">Master</span></span>  <br/> |<span data-ttu-id="d5a18-165">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-166">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-167">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-168">Page</span><span class="sxs-lookup"><span data-stu-id="d5a18-168">Page</span></span>  <br/> |<span data-ttu-id="d5a18-169">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-170">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-171">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="d5a18-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="d5a18-173">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-174">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-175">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-176">該当</span><span class="sxs-lookup"><span data-stu-id="d5a18-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="d5a18-177">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d5a18-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d5a18-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-178">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-179">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="d5a18-180">Sheet</span></span>  <br/> |<span data-ttu-id="d5a18-181">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-182">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-183">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="d5a18-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="d5a18-185">xsd: double</span><span class="sxs-lookup"><span data-stu-id="d5a18-185">xsd:double</span></span>  <br/> |<span data-ttu-id="d5a18-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-186">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-187">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-188">View中央 y</span><span class="sxs-lookup"><span data-stu-id="d5a18-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="d5a18-189">xsd: double</span><span class="sxs-lookup"><span data-stu-id="d5a18-189">xsd:double</span></span>  <br/> |<span data-ttu-id="d5a18-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-190">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-191">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="d5a18-192">ViewScale</span></span>  <br/> |<span data-ttu-id="d5a18-193">xsd: double</span><span class="sxs-lookup"><span data-stu-id="d5a18-193">xsd:double</span></span>  <br/> |<span data-ttu-id="d5a18-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-194">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-195">Xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="d5a18-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="d5a18-197">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-198">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-199">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="d5a18-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="d5a18-201">xsd: short</span><span class="sxs-lookup"><span data-stu-id="d5a18-201">xsd:short</span></span>  <br/> |<span data-ttu-id="d5a18-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-202">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-203">Xsd: short 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="d5a18-204">WindowState</span></span>  <br/> |<span data-ttu-id="d5a18-205">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-206">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-207">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="d5a18-208">WindowTop</span></span>  <br/> |<span data-ttu-id="d5a18-209">xsd: short</span><span class="sxs-lookup"><span data-stu-id="d5a18-209">xsd:short</span></span>  <br/> |<span data-ttu-id="d5a18-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-210">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-211">Xsd: short 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="d5a18-212">WindowType</span></span>  <br/> |<span data-ttu-id="d5a18-213">xsd: token</span><span class="sxs-lookup"><span data-stu-id="d5a18-213">xsd:token</span></span>  <br/> |<span data-ttu-id="d5a18-214">必須</span><span class="sxs-lookup"><span data-stu-id="d5a18-214">required</span></span>  <br/> ||<span data-ttu-id="d5a18-215">Xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="d5a18-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="d5a18-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="d5a18-217">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d5a18-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5a18-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5a18-218">optional</span></span>  <br/> ||<span data-ttu-id="d5a18-219">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d5a18-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

