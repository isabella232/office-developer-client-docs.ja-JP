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
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="5af14-102">Window_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="5af14-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5af14-103">型情報</span><span class="sxs-lookup"><span data-stu-id="5af14-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5af14-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5af14-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5af14-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5af14-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5af14-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5af14-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5af14-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="5af14-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5af14-108">なし</span><span class="sxs-lookup"><span data-stu-id="5af14-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5af14-109">定義</span><span class="sxs-lookup"><span data-stu-id="5af14-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5af14-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5af14-110">Elements and attributes</span></span>

<span data-ttu-id="5af14-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5af14-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5af14-112">子要素</span><span class="sxs-lookup"><span data-stu-id="5af14-112">Child elements</span></span>

|<span data-ttu-id="5af14-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="5af14-113">**Element**</span></span>|<span data-ttu-id="5af14-114">**型**</span><span class="sxs-lookup"><span data-stu-id="5af14-114">**Type**</span></span>|<span data-ttu-id="5af14-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="5af14-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5af14-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="5af14-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="5af14-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="5af14-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="5af14-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="5af14-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="5af14-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="5af14-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="5af14-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="5af14-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="5af14-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="5af14-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="5af14-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5af14-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="5af14-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af14-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="5af14-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5af14-142">属性</span><span class="sxs-lookup"><span data-stu-id="5af14-142">Attributes</span></span>

|<span data-ttu-id="5af14-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="5af14-143">**Attribute**</span></span>|<span data-ttu-id="5af14-144">**型**</span><span class="sxs-lookup"><span data-stu-id="5af14-144">**Type**</span></span>|<span data-ttu-id="5af14-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="5af14-145">**Required**</span></span>|<span data-ttu-id="5af14-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="5af14-146">**Description**</span></span>|<span data-ttu-id="5af14-147">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="5af14-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5af14-148">Container</span><span class="sxs-lookup"><span data-stu-id="5af14-148">Container</span></span>  <br/> |<span data-ttu-id="5af14-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-150">optional</span></span>  <br/> ||<span data-ttu-id="5af14-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="5af14-152">ContainerType</span></span>  <br/> |<span data-ttu-id="5af14-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="5af14-153">xsd:token</span></span>  <br/> |<span data-ttu-id="5af14-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-154">optional</span></span>  <br/> ||<span data-ttu-id="5af14-155">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="5af14-156">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="5af14-156">Document</span></span>  <br/> |<span data-ttu-id="5af14-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5af14-157">xsd:string</span></span>  <br/> |<span data-ttu-id="5af14-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-158">optional</span></span>  <br/> ||<span data-ttu-id="5af14-159">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5af14-160">ID</span><span class="sxs-lookup"><span data-stu-id="5af14-160">ID</span></span>  <br/> |<span data-ttu-id="5af14-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-162">必須</span><span class="sxs-lookup"><span data-stu-id="5af14-162">required</span></span>  <br/> ||<span data-ttu-id="5af14-163">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-164">Master</span><span class="sxs-lookup"><span data-stu-id="5af14-164">Master</span></span>  <br/> |<span data-ttu-id="5af14-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-166">optional</span></span>  <br/> ||<span data-ttu-id="5af14-167">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-168">Page オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5af14-168">Page</span></span>  <br/> |<span data-ttu-id="5af14-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-170">optional</span></span>  <br/> ||<span data-ttu-id="5af14-171">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="5af14-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="5af14-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-174">optional</span></span>  <br/> ||<span data-ttu-id="5af14-175">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="5af14-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="5af14-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="5af14-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5af14-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-178">optional</span></span>  <br/> ||<span data-ttu-id="5af14-179">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5af14-180">シート</span><span class="sxs-lookup"><span data-stu-id="5af14-180">Sheet</span></span>  <br/> |<span data-ttu-id="5af14-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-182">optional</span></span>  <br/> ||<span data-ttu-id="5af14-183">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="5af14-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="5af14-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5af14-185">xsd:double</span></span>  <br/> |<span data-ttu-id="5af14-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-186">optional</span></span>  <br/> ||<span data-ttu-id="5af14-187">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="5af14-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="5af14-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="5af14-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="5af14-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5af14-189">xsd:double</span></span>  <br/> |<span data-ttu-id="5af14-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-190">optional</span></span>  <br/> ||<span data-ttu-id="5af14-191">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="5af14-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="5af14-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="5af14-192">ViewScale</span></span>  <br/> |<span data-ttu-id="5af14-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="5af14-193">xsd:double</span></span>  <br/> |<span data-ttu-id="5af14-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-194">optional</span></span>  <br/> ||<span data-ttu-id="5af14-195">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="5af14-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="5af14-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="5af14-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="5af14-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-198">optional</span></span>  <br/> ||<span data-ttu-id="5af14-199">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="5af14-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="5af14-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="5af14-201">xsd:short</span></span>  <br/> |<span data-ttu-id="5af14-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-202">optional</span></span>  <br/> ||<span data-ttu-id="5af14-203">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="5af14-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="5af14-204">WindowState</span></span>  <br/> |<span data-ttu-id="5af14-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-206">optional</span></span>  <br/> ||<span data-ttu-id="5af14-207">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5af14-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="5af14-208">WindowTop</span></span>  <br/> |<span data-ttu-id="5af14-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="5af14-209">xsd:short</span></span>  <br/> |<span data-ttu-id="5af14-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-210">optional</span></span>  <br/> ||<span data-ttu-id="5af14-211">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="5af14-212">サービス クラス</span><span class="sxs-lookup"><span data-stu-id="5af14-212">WindowType</span></span>  <br/> |<span data-ttu-id="5af14-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="5af14-213">xsd:token</span></span>  <br/> |<span data-ttu-id="5af14-214">必須</span><span class="sxs-lookup"><span data-stu-id="5af14-214">required</span></span>  <br/> ||<span data-ttu-id="5af14-215">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="5af14-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="5af14-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="5af14-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5af14-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5af14-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="5af14-218">optional</span></span>  <br/> ||<span data-ttu-id="5af14-219">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5af14-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

