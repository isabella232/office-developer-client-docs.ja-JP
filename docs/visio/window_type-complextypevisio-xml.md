---
title: Window_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 340326213de4029201d21e627ed4b27c53b33d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339929"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="e0236-102">Window_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e0236-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e0236-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e0236-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0236-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0236-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0236-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e0236-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0236-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="e0236-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0236-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e0236-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0236-108">なし</span><span class="sxs-lookup"><span data-stu-id="e0236-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0236-109">定義</span><span class="sxs-lookup"><span data-stu-id="e0236-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e0236-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e0236-110">Elements and attributes</span></span>

<span data-ttu-id="e0236-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0236-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0236-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e0236-112">Child elements</span></span>

|<span data-ttu-id="e0236-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0236-113">**Element**</span></span>|<span data-ttu-id="e0236-114">**型**</span><span class="sxs-lookup"><span data-stu-id="e0236-114">**Type**</span></span>|<span data-ttu-id="e0236-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0236-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0236-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="e0236-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="e0236-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-120">showconnectionpoints</span><span class="sxs-lookup"><span data-stu-id="e0236-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="e0236-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="e0236-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="e0236-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="e0236-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="e0236-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="e0236-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="e0236-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="e0236-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="e0236-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0236-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="e0236-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0236-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="e0236-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0236-142">属性</span><span class="sxs-lookup"><span data-stu-id="e0236-142">Attributes</span></span>

|<span data-ttu-id="e0236-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="e0236-143">**Attribute**</span></span>|<span data-ttu-id="e0236-144">**型**</span><span class="sxs-lookup"><span data-stu-id="e0236-144">**Type**</span></span>|<span data-ttu-id="e0236-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="e0236-145">**Required**</span></span>|<span data-ttu-id="e0236-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0236-146">**Description**</span></span>|<span data-ttu-id="e0236-147">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e0236-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0236-148">Container</span><span class="sxs-lookup"><span data-stu-id="e0236-148">Container</span></span>  <br/> |<span data-ttu-id="e0236-149">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-150">optional</span></span>  <br/> ||<span data-ttu-id="e0236-151">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="e0236-152">ContainerType</span></span>  <br/> |<span data-ttu-id="e0236-153">xsd: token</span><span class="sxs-lookup"><span data-stu-id="e0236-153">xsd:token</span></span>  <br/> |<span data-ttu-id="e0236-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-154">optional</span></span>  <br/> ||<span data-ttu-id="e0236-155">xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e0236-156">Document</span><span class="sxs-lookup"><span data-stu-id="e0236-156">Document</span></span>  <br/> |<span data-ttu-id="e0236-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e0236-157">xsd:string</span></span>  <br/> |<span data-ttu-id="e0236-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-158">optional</span></span>  <br/> ||<span data-ttu-id="e0236-159">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0236-160">ID</span><span class="sxs-lookup"><span data-stu-id="e0236-160">ID</span></span>  <br/> |<span data-ttu-id="e0236-161">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-162">必須</span><span class="sxs-lookup"><span data-stu-id="e0236-162">required</span></span>  <br/> ||<span data-ttu-id="e0236-163">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-164">Master</span><span class="sxs-lookup"><span data-stu-id="e0236-164">Master</span></span>  <br/> |<span data-ttu-id="e0236-165">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-166">optional</span></span>  <br/> ||<span data-ttu-id="e0236-167">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-168">ページ</span><span class="sxs-lookup"><span data-stu-id="e0236-168">Page</span></span>  <br/> |<span data-ttu-id="e0236-169">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-170">optional</span></span>  <br/> ||<span data-ttu-id="e0236-171">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="e0236-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="e0236-173">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-174">optional</span></span>  <br/> ||<span data-ttu-id="e0236-175">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-176">該当</span><span class="sxs-lookup"><span data-stu-id="e0236-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="e0236-177">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="e0236-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0236-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-178">optional</span></span>  <br/> ||<span data-ttu-id="e0236-179">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0236-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="e0236-180">Sheet</span></span>  <br/> |<span data-ttu-id="e0236-181">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-182">optional</span></span>  <br/> ||<span data-ttu-id="e0236-183">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="e0236-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="e0236-185">xsd: double</span><span class="sxs-lookup"><span data-stu-id="e0236-185">xsd:double</span></span>  <br/> |<span data-ttu-id="e0236-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-186">optional</span></span>  <br/> ||<span data-ttu-id="e0236-187">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e0236-188">view中央 y</span><span class="sxs-lookup"><span data-stu-id="e0236-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="e0236-189">xsd: double</span><span class="sxs-lookup"><span data-stu-id="e0236-189">xsd:double</span></span>  <br/> |<span data-ttu-id="e0236-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-190">optional</span></span>  <br/> ||<span data-ttu-id="e0236-191">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e0236-192">viewscale</span><span class="sxs-lookup"><span data-stu-id="e0236-192">ViewScale</span></span>  <br/> |<span data-ttu-id="e0236-193">xsd: double</span><span class="sxs-lookup"><span data-stu-id="e0236-193">xsd:double</span></span>  <br/> |<span data-ttu-id="e0236-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-194">optional</span></span>  <br/> ||<span data-ttu-id="e0236-195">xsd: double 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="e0236-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="e0236-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="e0236-197">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-198">optional</span></span>  <br/> ||<span data-ttu-id="e0236-199">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="e0236-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="e0236-201">xsd: short</span><span class="sxs-lookup"><span data-stu-id="e0236-201">xsd:short</span></span>  <br/> |<span data-ttu-id="e0236-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-202">optional</span></span>  <br/> ||<span data-ttu-id="e0236-203">xsd: short 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="e0236-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="e0236-204">WindowState</span></span>  <br/> |<span data-ttu-id="e0236-205">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-206">optional</span></span>  <br/> ||<span data-ttu-id="e0236-207">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0236-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="e0236-208">WindowTop</span></span>  <br/> |<span data-ttu-id="e0236-209">xsd: short</span><span class="sxs-lookup"><span data-stu-id="e0236-209">xsd:short</span></span>  <br/> |<span data-ttu-id="e0236-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-210">optional</span></span>  <br/> ||<span data-ttu-id="e0236-211">xsd: short 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="e0236-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="e0236-212">WindowType</span></span>  <br/> |<span data-ttu-id="e0236-213">xsd: token</span><span class="sxs-lookup"><span data-stu-id="e0236-213">xsd:token</span></span>  <br/> |<span data-ttu-id="e0236-214">必須</span><span class="sxs-lookup"><span data-stu-id="e0236-214">required</span></span>  <br/> ||<span data-ttu-id="e0236-215">xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e0236-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="e0236-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="e0236-217">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="e0236-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0236-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="e0236-218">optional</span></span>  <br/> ||<span data-ttu-id="e0236-219">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="e0236-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

