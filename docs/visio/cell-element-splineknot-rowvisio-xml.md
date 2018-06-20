---
title: セル要素 (SplineKnot 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61faf0d6-c0a2-9350-8712-7a450591afad
description: X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。
ms.openlocfilehash: 14a62fba7d900f1d15a21b4a348c9affda6cad05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804973"
---
# <a name="cell-element-splineknot-row-visio-xml"></a><span data-ttu-id="5819c-103">セル要素 (SplineKnot 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5819c-103">Cell element (SplineKnot Row) ('Visio XML')</span></span>

<span data-ttu-id="5819c-104">X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5819c-104">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5819c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5819c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5819c-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="5819c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5819c-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5819c-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5819c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5819c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5819c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5819c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5819c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5819c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5819c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5819c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5819c-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="5819c-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5819c-113">定義</span><span class="sxs-lookup"><span data-stu-id="5819c-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5819c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5819c-114">Elements and attributes</span></span>

<span data-ttu-id="5819c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5819c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5819c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5819c-116">Parent elements</span></span>

|<span data-ttu-id="5819c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5819c-117">**Element**</span></span>|<span data-ttu-id="5819c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5819c-118">**Type**</span></span>|<span data-ttu-id="5819c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5819c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5819c-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="5819c-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5819c-121">SplineKot_Type</span><span class="sxs-lookup"><span data-stu-id="5819c-121">SplineKot_Type</span></span>](splineknot_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5819c-122">X 座標または y 座標、スプラインの制御点、またはスプラインのノットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5819c-122">Contains x- or y-coordinates for a spline's control point or a spline's knot.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5819c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5819c-123">Child elements</span></span>

|<span data-ttu-id="5819c-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="5819c-124">**Element**</span></span>|<span data-ttu-id="5819c-125">**型**</span><span class="sxs-lookup"><span data-stu-id="5819c-125">**Type**</span></span>|<span data-ttu-id="5819c-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="5819c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5819c-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="5819c-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5819c-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="5819c-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5819c-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="5819c-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5819c-130">属性</span><span class="sxs-lookup"><span data-stu-id="5819c-130">Attributes</span></span>

|<span data-ttu-id="5819c-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="5819c-131">**Attribute**</span></span>|<span data-ttu-id="5819c-132">**型**</span><span class="sxs-lookup"><span data-stu-id="5819c-132">**Type**</span></span>|<span data-ttu-id="5819c-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="5819c-133">**Required**</span></span>|<span data-ttu-id="5819c-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="5819c-134">**Description**</span></span>|<span data-ttu-id="5819c-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="5819c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5819c-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="5819c-136">E</span></span>  <br/> |<span data-ttu-id="5819c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5819c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="5819c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="5819c-138">optional</span></span>  <br/> |<span data-ttu-id="5819c-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="5819c-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="5819c-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="5819c-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="5819c-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="5819c-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="5819c-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="5819c-142">F</span></span>  <br/> |<span data-ttu-id="5819c-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5819c-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5819c-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="5819c-144">optional</span></span>  <br/> | <span data-ttu-id="5819c-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="5819c-145">Represents the element's formula.</span></span> <span data-ttu-id="5819c-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5819c-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="5819c-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="5819c-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="5819c-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="5819c-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="5819c-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="5819c-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="5819c-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="5819c-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="5819c-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="5819c-151">N</span></span>  <br/> |<span data-ttu-id="5819c-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5819c-152">xsd:string</span></span>  <br/> |<span data-ttu-id="5819c-153">必須</span><span class="sxs-lookup"><span data-stu-id="5819c-153">required</span></span>  <br/> |<span data-ttu-id="5819c-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="5819c-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="5819c-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="5819c-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="5819c-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5819c-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="5819c-157">U</span><span class="sxs-lookup"><span data-stu-id="5819c-157">U</span></span>  <br/> |<span data-ttu-id="5819c-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5819c-158">xsd:string</span></span>  <br/> |<span data-ttu-id="5819c-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="5819c-159">optional</span></span>  <br/> |<span data-ttu-id="5819c-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="5819c-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="5819c-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="5819c-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="5819c-162">V</span><span class="sxs-lookup"><span data-stu-id="5819c-162">V</span></span>  <br/> |<span data-ttu-id="5819c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5819c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="5819c-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="5819c-164">optional</span></span>  <br/> |<span data-ttu-id="5819c-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="5819c-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="5819c-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="5819c-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5819c-167">備考</span><span class="sxs-lookup"><span data-stu-id="5819c-167">Remarks</span></span>

<span data-ttu-id="5819c-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5819c-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="5819c-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5819c-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="5819c-170">**値**</span><span class="sxs-lookup"><span data-stu-id="5819c-170">**Value**</span></span>|<span data-ttu-id="5819c-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="5819c-171">**Description**</span></span>|<span data-ttu-id="5819c-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="5819c-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5819c-173">X</span><span class="sxs-lookup"><span data-stu-id="5819c-173">X</span></span>  <br/> |<span data-ttu-id="5819c-174">コントロール ポイントの x 座標。</span><span class="sxs-lookup"><span data-stu-id="5819c-174">The x-coordinate of a control point.</span></span>  <br/> |<span data-ttu-id="5819c-175">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="5819c-175">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="5819c-176">Y</span><span class="sxs-lookup"><span data-stu-id="5819c-176">Y</span></span>  <br/> |<span data-ttu-id="5819c-177">コントロール ポイントの y 座標。</span><span class="sxs-lookup"><span data-stu-id="5819c-177">The y-coordinate of a control point.</span></span>  <br/> |<span data-ttu-id="5819c-178">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="5819c-178">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="5819c-179">A</span><span class="sxs-lookup"><span data-stu-id="5819c-179">A</span></span>  <br/> |<span data-ttu-id="5819c-180">スプラインのノットのいずれか 1 つです (最後のノットと最初の 2 つのノットは除く)。</span><span class="sxs-lookup"><span data-stu-id="5819c-180">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |<span data-ttu-id="5819c-181">[[SplineKnot] 行 ([Geometry] セクション)](splineknot-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="5819c-181">[SplineKnot Row (Geometry Section)](splineknot-row-geometry-section.md)</span></span> <br/> |
   

