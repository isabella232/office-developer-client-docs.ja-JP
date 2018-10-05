---
title: Window_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 340326213de4029201d21e627ed4b27c53b33d1e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400587"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="30e10-102">Window_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="30e10-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="30e10-103">型情報</span><span class="sxs-lookup"><span data-stu-id="30e10-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30e10-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="30e10-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="30e10-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="30e10-105">**Schema file**</span></span> <br/> |<span data-ttu-id="30e10-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="30e10-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="30e10-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="30e10-107">**Extension base**</span></span> <br/> |<span data-ttu-id="30e10-108">なし</span><span class="sxs-lookup"><span data-stu-id="30e10-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30e10-109">定義</span><span class="sxs-lookup"><span data-stu-id="30e10-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="30e10-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="30e10-110">Elements and attributes</span></span>

<span data-ttu-id="30e10-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30e10-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="30e10-112">子要素</span><span class="sxs-lookup"><span data-stu-id="30e10-112">Child elements</span></span>

|<span data-ttu-id="30e10-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="30e10-113">**Element**</span></span>|<span data-ttu-id="30e10-114">**型**</span><span class="sxs-lookup"><span data-stu-id="30e10-114">**Type**</span></span>|<span data-ttu-id="30e10-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="30e10-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30e10-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="30e10-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="30e10-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="30e10-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="30e10-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="30e10-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="30e10-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="30e10-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="30e10-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="30e10-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="30e10-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="30e10-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="30e10-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="30e10-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="30e10-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30e10-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="30e10-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="30e10-142">属性</span><span class="sxs-lookup"><span data-stu-id="30e10-142">Attributes</span></span>

|<span data-ttu-id="30e10-143">**属性**</span><span class="sxs-lookup"><span data-stu-id="30e10-143">**Attribute**</span></span>|<span data-ttu-id="30e10-144">**型**</span><span class="sxs-lookup"><span data-stu-id="30e10-144">**Type**</span></span>|<span data-ttu-id="30e10-145">**必須**</span><span class="sxs-lookup"><span data-stu-id="30e10-145">**Required**</span></span>|<span data-ttu-id="30e10-146">**説明**</span><span class="sxs-lookup"><span data-stu-id="30e10-146">**Description**</span></span>|<span data-ttu-id="30e10-147">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="30e10-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="30e10-148">Container</span><span class="sxs-lookup"><span data-stu-id="30e10-148">Container</span></span>  <br/> |<span data-ttu-id="30e10-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-150">optional</span></span>  <br/> ||<span data-ttu-id="30e10-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="30e10-152">ContainerType</span></span>  <br/> |<span data-ttu-id="30e10-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="30e10-153">xsd:token</span></span>  <br/> |<span data-ttu-id="30e10-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-154">optional</span></span>  <br/> ||<span data-ttu-id="30e10-155">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="30e10-156">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="30e10-156">Document</span></span>  <br/> |<span data-ttu-id="30e10-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="30e10-157">xsd:string</span></span>  <br/> |<span data-ttu-id="30e10-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-158">optional</span></span>  <br/> ||<span data-ttu-id="30e10-159">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="30e10-160">ID</span><span class="sxs-lookup"><span data-stu-id="30e10-160">ID</span></span>  <br/> |<span data-ttu-id="30e10-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-162">必須</span><span class="sxs-lookup"><span data-stu-id="30e10-162">required</span></span>  <br/> ||<span data-ttu-id="30e10-163">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-164">Master</span><span class="sxs-lookup"><span data-stu-id="30e10-164">Master</span></span>  <br/> |<span data-ttu-id="30e10-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-166">optional</span></span>  <br/> ||<span data-ttu-id="30e10-167">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-168">Page オブジェクト</span><span class="sxs-lookup"><span data-stu-id="30e10-168">Page</span></span>  <br/> |<span data-ttu-id="30e10-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-170">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-170">optional</span></span>  <br/> ||<span data-ttu-id="30e10-171">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="30e10-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="30e10-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-174">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-174">optional</span></span>  <br/> ||<span data-ttu-id="30e10-175">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="30e10-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="30e10-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="30e10-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="30e10-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-178">optional</span></span>  <br/> ||<span data-ttu-id="30e10-179">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="30e10-180">シート</span><span class="sxs-lookup"><span data-stu-id="30e10-180">Sheet</span></span>  <br/> |<span data-ttu-id="30e10-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-182">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-182">optional</span></span>  <br/> ||<span data-ttu-id="30e10-183">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="30e10-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="30e10-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="30e10-185">xsd:double</span></span>  <br/> |<span data-ttu-id="30e10-186">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-186">optional</span></span>  <br/> ||<span data-ttu-id="30e10-187">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="30e10-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="30e10-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="30e10-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="30e10-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="30e10-189">xsd:double</span></span>  <br/> |<span data-ttu-id="30e10-190">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-190">optional</span></span>  <br/> ||<span data-ttu-id="30e10-191">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="30e10-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="30e10-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="30e10-192">ViewScale</span></span>  <br/> |<span data-ttu-id="30e10-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="30e10-193">xsd:double</span></span>  <br/> |<span data-ttu-id="30e10-194">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-194">optional</span></span>  <br/> ||<span data-ttu-id="30e10-195">Xsd:double 型の値です。</span><span class="sxs-lookup"><span data-stu-id="30e10-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="30e10-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="30e10-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="30e10-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-198">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-198">optional</span></span>  <br/> ||<span data-ttu-id="30e10-199">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="30e10-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="30e10-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="30e10-201">xsd:short</span></span>  <br/> |<span data-ttu-id="30e10-202">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-202">optional</span></span>  <br/> ||<span data-ttu-id="30e10-203">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="30e10-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="30e10-204">WindowState</span></span>  <br/> |<span data-ttu-id="30e10-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-206">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-206">optional</span></span>  <br/> ||<span data-ttu-id="30e10-207">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="30e10-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="30e10-208">WindowTop</span></span>  <br/> |<span data-ttu-id="30e10-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="30e10-209">xsd:short</span></span>  <br/> |<span data-ttu-id="30e10-210">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-210">optional</span></span>  <br/> ||<span data-ttu-id="30e10-211">Xsd:short の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="30e10-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="30e10-212">WindowType</span></span>  <br/> |<span data-ttu-id="30e10-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="30e10-213">xsd:token</span></span>  <br/> |<span data-ttu-id="30e10-214">必須</span><span class="sxs-lookup"><span data-stu-id="30e10-214">required</span></span>  <br/> ||<span data-ttu-id="30e10-215">Xsd:token の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="30e10-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="30e10-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="30e10-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="30e10-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="30e10-218">省略可能</span><span class="sxs-lookup"><span data-stu-id="30e10-218">optional</span></span>  <br/> ||<span data-ttu-id="30e10-219">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="30e10-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

