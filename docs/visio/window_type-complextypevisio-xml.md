---
title: Window_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806793"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="19734-102">Window_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="19734-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="19734-103">型情報</span><span class="sxs-lookup"><span data-stu-id="19734-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19734-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="19734-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19734-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="19734-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19734-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="19734-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19734-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="19734-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19734-108">なし</span><span class="sxs-lookup"><span data-stu-id="19734-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19734-109">定義</span><span class="sxs-lookup"><span data-stu-id="19734-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19734-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="19734-110">Elements and attributes</span></span>

<span data-ttu-id="19734-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="19734-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19734-112">子要素</span><span class="sxs-lookup"><span data-stu-id="19734-112">Child elements</span></span>

|<span data-ttu-id="19734-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="19734-113">**Element**</span></span>|<span data-ttu-id="19734-114">**型**</span><span class="sxs-lookup"><span data-stu-id="19734-114">**Type**</span></span>|<span data-ttu-id="19734-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="19734-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19734-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="19734-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="19734-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="19734-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="19734-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="19734-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="19734-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="19734-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="19734-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="19734-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="19734-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="19734-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="19734-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="19734-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="19734-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="19734-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="19734-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="19734-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="19734-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="19734-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="19734-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="19734-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="19734-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="19734-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="19734-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19734-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="19734-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19734-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="19734-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="19734-142">属性</span><span class="sxs-lookup"><span data-stu-id="19734-142">Attributes</span></span>

|<span data-ttu-id="19734-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="19734-143">**Attribute**</span></span>|<span data-ttu-id="19734-144">**型**</span><span class="sxs-lookup"><span data-stu-id="19734-144">**Type**</span></span>|<span data-ttu-id="19734-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="19734-145">**Required**</span></span>|<span data-ttu-id="19734-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="19734-146">**Description**</span></span>|<span data-ttu-id="19734-147">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="19734-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19734-148">Container</span><span class="sxs-lookup"><span data-stu-id="19734-148">Container</span></span>  <br/> |<span data-ttu-id="19734-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-150">optional</span></span>  <br/> ||<span data-ttu-id="19734-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="19734-152">ContainerType</span></span>  <br/> |<span data-ttu-id="19734-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="19734-153">xsd:token</span></span>  <br/> |<span data-ttu-id="19734-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-154">optional</span></span>  <br/> ||<span data-ttu-id="19734-155">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="19734-156">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="19734-156">Document</span></span>  <br/> |<span data-ttu-id="19734-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19734-157">xsd:string</span></span>  <br/> |<span data-ttu-id="19734-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-158">optional</span></span>  <br/> ||<span data-ttu-id="19734-159">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19734-160">ID</span><span class="sxs-lookup"><span data-stu-id="19734-160">ID</span></span>  <br/> |<span data-ttu-id="19734-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-162">必須</span><span class="sxs-lookup"><span data-stu-id="19734-162">required</span></span>  <br/> ||<span data-ttu-id="19734-163">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-164">Master</span><span class="sxs-lookup"><span data-stu-id="19734-164">Master</span></span>  <br/> |<span data-ttu-id="19734-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-166">optional</span></span>  <br/> ||<span data-ttu-id="19734-167">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-168">Page オブジェクト</span><span class="sxs-lookup"><span data-stu-id="19734-168">Page</span></span>  <br/> |<span data-ttu-id="19734-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-170">optional</span></span>  <br/> ||<span data-ttu-id="19734-171">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="19734-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="19734-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-174">optional</span></span>  <br/> ||<span data-ttu-id="19734-175">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="19734-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="19734-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19734-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19734-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-178">optional</span></span>  <br/> ||<span data-ttu-id="19734-179">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19734-180">シート</span><span class="sxs-lookup"><span data-stu-id="19734-180">Sheet</span></span>  <br/> |<span data-ttu-id="19734-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-182">optional</span></span>  <br/> ||<span data-ttu-id="19734-183">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="19734-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="19734-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19734-185">xsd:double</span></span>  <br/> |<span data-ttu-id="19734-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-186">optional</span></span>  <br/> ||<span data-ttu-id="19734-187">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="19734-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="19734-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="19734-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="19734-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19734-189">xsd:double</span></span>  <br/> |<span data-ttu-id="19734-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-190">optional</span></span>  <br/> ||<span data-ttu-id="19734-191">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="19734-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="19734-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="19734-192">ViewScale</span></span>  <br/> |<span data-ttu-id="19734-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19734-193">xsd:double</span></span>  <br/> |<span data-ttu-id="19734-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-194">optional</span></span>  <br/> ||<span data-ttu-id="19734-195">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="19734-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="19734-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="19734-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="19734-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-198">optional</span></span>  <br/> ||<span data-ttu-id="19734-199">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="19734-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="19734-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="19734-201">xsd:short</span></span>  <br/> |<span data-ttu-id="19734-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-202">optional</span></span>  <br/> ||<span data-ttu-id="19734-203">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="19734-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="19734-204">WindowState</span></span>  <br/> |<span data-ttu-id="19734-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-206">optional</span></span>  <br/> ||<span data-ttu-id="19734-207">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19734-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="19734-208">WindowTop</span></span>  <br/> |<span data-ttu-id="19734-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="19734-209">xsd:short</span></span>  <br/> |<span data-ttu-id="19734-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-210">optional</span></span>  <br/> ||<span data-ttu-id="19734-211">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="19734-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="19734-212">WindowType</span></span>  <br/> |<span data-ttu-id="19734-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="19734-213">xsd:token</span></span>  <br/> |<span data-ttu-id="19734-214">必須</span><span class="sxs-lookup"><span data-stu-id="19734-214">required</span></span>  <br/> ||<span data-ttu-id="19734-215">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="19734-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="19734-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="19734-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19734-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19734-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="19734-218">optional</span></span>  <br/> ||<span data-ttu-id="19734-219">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="19734-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

