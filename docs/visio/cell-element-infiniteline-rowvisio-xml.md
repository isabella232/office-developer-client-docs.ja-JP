---
title: セル要素 (InfiniteLine 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e14b8246-0064-3a54-7bd6-ad28180f9ea6
description: 無限線上の 2 つの点の x 座標または y 座標が含まれています。
ms.openlocfilehash: 1dde7958116824efffce6247855a959fee61e869
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392789"
---
# <a name="cell-element-infiniteline-row-visio-xml"></a><span data-ttu-id="c5ca6-103">セル要素 (InfiniteLine 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c5ca6-103">Cell element (InfiniteLine Row) ('Visio XML')</span></span>

<span data-ttu-id="c5ca6-104">無限線上の 2 つの点の x 座標または y 座標が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-104">Contains the x- or y-coordinates of two points on an infinite line.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5ca6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c5ca6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5ca6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5ca6-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c5ca6-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5ca6-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5ca6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5ca6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5ca6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5ca6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c5ca6-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="c5ca6-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5ca6-113">定義</span><span class="sxs-lookup"><span data-stu-id="c5ca6-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5ca6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c5ca6-114">Elements and attributes</span></span>

<span data-ttu-id="c5ca6-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5ca6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c5ca6-116">Parent elements</span></span>

|<span data-ttu-id="c5ca6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-117">**Element**</span></span>|<span data-ttu-id="c5ca6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-118">**Type**</span></span>|<span data-ttu-id="c5ca6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5ca6-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="c5ca6-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="c5ca6-121">InfiniteLine_Type</span><span class="sxs-lookup"><span data-stu-id="c5ca6-121">InfiniteLine_Type</span></span>](infiniteline_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5ca6-122">無限線上の 2 つの点の x 座標または y 座標が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-122">Contains the x- or y-coordinates of two points on an infinite line.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5ca6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c5ca6-123">Child elements</span></span>

|<span data-ttu-id="c5ca6-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-124">**Element**</span></span>|<span data-ttu-id="c5ca6-125">**型**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-125">**Type**</span></span>|<span data-ttu-id="c5ca6-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5ca6-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="c5ca6-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c5ca6-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c5ca6-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5ca6-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c5ca6-130">属性</span><span class="sxs-lookup"><span data-stu-id="c5ca6-130">Attributes</span></span>

|<span data-ttu-id="c5ca6-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-131">**Attribute**</span></span>|<span data-ttu-id="c5ca6-132">**型**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-132">**Type**</span></span>|<span data-ttu-id="c5ca6-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-133">**Required**</span></span>|<span data-ttu-id="c5ca6-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-134">**Description**</span></span>|<span data-ttu-id="c5ca6-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5ca6-136">E</span><span class="sxs-lookup"><span data-stu-id="c5ca6-136">E</span></span>  <br/> |<span data-ttu-id="c5ca6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5ca6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c5ca6-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c5ca6-138">optional</span></span>  <br/> |<span data-ttu-id="c5ca6-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="c5ca6-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="c5ca6-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="c5ca6-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="c5ca6-142">F</span></span>  <br/> |<span data-ttu-id="c5ca6-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5ca6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c5ca6-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="c5ca6-144">optional</span></span>  <br/> | <span data-ttu-id="c5ca6-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-145">Represents the element's formula.</span></span> <span data-ttu-id="c5ca6-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="c5ca6-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="c5ca6-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="c5ca6-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="c5ca6-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="c5ca6-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="c5ca6-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="c5ca6-151">N</span><span class="sxs-lookup"><span data-stu-id="c5ca6-151">N</span></span>  <br/> |<span data-ttu-id="c5ca6-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5ca6-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c5ca6-153">必須</span><span class="sxs-lookup"><span data-stu-id="c5ca6-153">required</span></span>  <br/> |<span data-ttu-id="c5ca6-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="c5ca6-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="c5ca6-157">U</span><span class="sxs-lookup"><span data-stu-id="c5ca6-157">U</span></span>  <br/> |<span data-ttu-id="c5ca6-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5ca6-158">xsd:string</span></span>  <br/> |<span data-ttu-id="c5ca6-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="c5ca6-159">optional</span></span>  <br/> |<span data-ttu-id="c5ca6-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="c5ca6-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="c5ca6-162">V</span><span class="sxs-lookup"><span data-stu-id="c5ca6-162">V</span></span>  <br/> |<span data-ttu-id="c5ca6-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5ca6-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c5ca6-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="c5ca6-164">optional</span></span>  <br/> |<span data-ttu-id="c5ca6-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5ca6-167">備考</span><span class="sxs-lookup"><span data-stu-id="c5ca6-167">Remarks</span></span>

<span data-ttu-id="c5ca6-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="c5ca6-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="c5ca6-170">**値**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-170">**Value**</span></span>|<span data-ttu-id="c5ca6-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-171">**Description**</span></span>|<span data-ttu-id="c5ca6-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="c5ca6-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5ca6-173">X</span><span class="sxs-lookup"><span data-stu-id="c5ca6-173">X</span></span>  <br/> |<span data-ttu-id="c5ca6-174">無限線上の点の x 座標です。対応する y 座標は [Y] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-174">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the Y cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-175">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c5ca6-175">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="c5ca6-176">Y</span><span class="sxs-lookup"><span data-stu-id="c5ca6-176">Y</span></span>  <br/> |<span data-ttu-id="c5ca6-177">無限線上の点の y 座標です。対応する x 座標は [X] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-177">A y-coordinate of a point on the infinite line; paired with x-coordinate represented by the X cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-178">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c5ca6-178">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="c5ca6-179">A</span><span class="sxs-lookup"><span data-stu-id="c5ca6-179">A</span></span>  <br/> |<span data-ttu-id="c5ca6-180">無限線上の点の x 座標です。対応する y 座標は [B] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-180">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the B cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-181">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c5ca6-181">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="c5ca6-182">B</span><span class="sxs-lookup"><span data-stu-id="c5ca6-182">B</span></span>  <br/> |<span data-ttu-id="c5ca6-183">無限線上の点の y 座標です。対応する x 座標は [A] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="c5ca6-183">A y-coordinate of a point on an infinite line; paired with x-coordinate represented by the A cell.</span></span>  <br/> |<span data-ttu-id="c5ca6-184">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="c5ca6-184">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
   

