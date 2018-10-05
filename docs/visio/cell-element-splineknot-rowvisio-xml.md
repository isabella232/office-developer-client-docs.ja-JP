---
title: セル要素 (SplineKnot 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。
ms.openlocfilehash: 1f2ddbcf7b750f2c2de983e16861070c7305fc3a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395120"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="8489e-103">セル要素 (SplineKnot 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="8489e-103">Cell element (SplineKnot Row) ('Visio XML')</span></span>

<span data-ttu-id="8489e-104">X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8489e-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8489e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8489e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8489e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8489e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8489e-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8489e-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8489e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8489e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8489e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8489e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8489e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8489e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8489e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8489e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8489e-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="8489e-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8489e-113">定義</span><span class="sxs-lookup"><span data-stu-id="8489e-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8489e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8489e-114">Elements and attributes</span></span>

<span data-ttu-id="8489e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8489e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8489e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8489e-116">Parent elements</span></span>

|<span data-ttu-id="8489e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8489e-117">**Element**</span></span>|<span data-ttu-id="8489e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8489e-118">**Type**</span></span>|<span data-ttu-id="8489e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8489e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8489e-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="8489e-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8489e-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="8489e-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8489e-122">X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8489e-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8489e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8489e-123">Child elements</span></span>

|<span data-ttu-id="8489e-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="8489e-124">**Element**</span></span>|<span data-ttu-id="8489e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8489e-125">**Type**</span></span>|<span data-ttu-id="8489e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8489e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8489e-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="8489e-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8489e-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="8489e-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8489e-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="8489e-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8489e-130">属性</span><span class="sxs-lookup"><span data-stu-id="8489e-130">Attributes</span></span>

|<span data-ttu-id="8489e-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="8489e-131">**Attribute**</span></span>|<span data-ttu-id="8489e-132">**型**</span><span class="sxs-lookup"><span data-stu-id="8489e-132">**Type**</span></span>|<span data-ttu-id="8489e-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="8489e-133">**Required**</span></span>|<span data-ttu-id="8489e-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="8489e-134">**Description**</span></span>|<span data-ttu-id="8489e-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="8489e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8489e-136">E</span><span class="sxs-lookup"><span data-stu-id="8489e-136">E</span></span>  <br/> |<span data-ttu-id="8489e-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8489e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8489e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="8489e-138">optional</span></span>  <br/> |<span data-ttu-id="8489e-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="8489e-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="8489e-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="8489e-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="8489e-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="8489e-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="8489e-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="8489e-142">F</span></span>  <br/> |<span data-ttu-id="8489e-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8489e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8489e-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="8489e-144">optional</span></span>  <br/> | <span data-ttu-id="8489e-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="8489e-145">Represents the element's formula.</span></span> <span data-ttu-id="8489e-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8489e-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="8489e-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="8489e-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="8489e-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="8489e-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="8489e-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="8489e-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="8489e-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="8489e-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="8489e-151">N</span><span class="sxs-lookup"><span data-stu-id="8489e-151">N</span></span>  <br/> |<span data-ttu-id="8489e-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8489e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8489e-153">必須</span><span class="sxs-lookup"><span data-stu-id="8489e-153">required</span></span>  <br/> |<span data-ttu-id="8489e-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="8489e-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="8489e-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="8489e-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="8489e-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8489e-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="8489e-157">U</span><span class="sxs-lookup"><span data-stu-id="8489e-157">U</span></span>  <br/> |<span data-ttu-id="8489e-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8489e-158">xsd:string</span></span>  <br/> |<span data-ttu-id="8489e-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="8489e-159">optional</span></span>  <br/> |<span data-ttu-id="8489e-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="8489e-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="8489e-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="8489e-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="8489e-162">V</span><span class="sxs-lookup"><span data-stu-id="8489e-162">V</span></span>  <br/> |<span data-ttu-id="8489e-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8489e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8489e-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="8489e-164">optional</span></span>  <br/> |<span data-ttu-id="8489e-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="8489e-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="8489e-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="8489e-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8489e-167">備考</span><span class="sxs-lookup"><span data-stu-id="8489e-167">Remarks</span></span>

<span data-ttu-id="8489e-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="8489e-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="8489e-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8489e-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="8489e-170">**値**</span><span class="sxs-lookup"><span data-stu-id="8489e-170">**Value**</span></span>|<span data-ttu-id="8489e-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="8489e-171">**Description**</span></span>|<span data-ttu-id="8489e-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="8489e-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8489e-173">X</span><span class="sxs-lookup"><span data-stu-id="8489e-173">X</span></span>  <br/> |<span data-ttu-id="8489e-174">コントロール ポイントの x 座標です。</span><span class="sxs-lookup"><span data-stu-id="8489e-174">The x-coordinate of a control point.</span></span>  <br/> |<span data-ttu-id="8489e-175">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8489e-175">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="8489e-176">Y</span><span class="sxs-lookup"><span data-stu-id="8489e-176">Y</span></span>  <br/> |<span data-ttu-id="8489e-177">コントロール ポイントの y 座標です。</span><span class="sxs-lookup"><span data-stu-id="8489e-177">The y-coordinate of a control point.</span></span>  <br/> |<span data-ttu-id="8489e-178">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8489e-178">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="8489e-179">A</span><span class="sxs-lookup"><span data-stu-id="8489e-179">A</span></span>  <br/> |<span data-ttu-id="8489e-180">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="8489e-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |<span data-ttu-id="8489e-181">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8489e-181">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
   

