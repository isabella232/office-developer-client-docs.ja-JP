---
title: セル要素 (InfiniteLine 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e14b8246-0064-3a54-7bd6-ad28180f9ea6
description: 無限線上の 2 つの点の x 座標または y 座標が含まれています。
ms.openlocfilehash: 2ead373e3ef28f9871d861a668f564c1296023d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804971"
---
# <a name="cell-element-infiniteline-row-visio-xml"></a><span data-ttu-id="4cb00-103">セル要素 (InfiniteLine 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4cb00-103">Cell element (InfiniteLine Row) ('Visio XML')</span></span>

<span data-ttu-id="4cb00-104">無限線上の 2 つの点の x 座標または y 座標が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cb00-104">Contains the x- or y-coordinates of two points on an infinite line.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cb00-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4cb00-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cb00-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4cb00-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4cb00-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4cb00-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4cb00-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4cb00-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4cb00-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4cb00-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4cb00-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4cb00-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4cb00-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4cb00-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4cb00-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="4cb00-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4cb00-113">定義</span><span class="sxs-lookup"><span data-stu-id="4cb00-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4cb00-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4cb00-114">Elements and attributes</span></span>

<span data-ttu-id="4cb00-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cb00-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4cb00-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4cb00-116">Parent elements</span></span>

|<span data-ttu-id="4cb00-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4cb00-117">**Element**</span></span>|<span data-ttu-id="4cb00-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4cb00-118">**Type**</span></span>|<span data-ttu-id="4cb00-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cb00-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4cb00-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="4cb00-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4cb00-121">InfiniteLine_Type</span><span class="sxs-lookup"><span data-stu-id="4cb00-121">InfiniteLine_Type</span></span>](infiniteline_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4cb00-122">無限線上の 2 つの点の x 座標または y 座標が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cb00-122">Contains the x- or y-coordinates of two points on an infinite line.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4cb00-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4cb00-123">Child elements</span></span>

|<span data-ttu-id="4cb00-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="4cb00-124">**Element**</span></span>|<span data-ttu-id="4cb00-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4cb00-125">**Type**</span></span>|<span data-ttu-id="4cb00-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cb00-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4cb00-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="4cb00-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4cb00-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4cb00-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4cb00-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cb00-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4cb00-130">属性</span><span class="sxs-lookup"><span data-stu-id="4cb00-130">Attributes</span></span>

|<span data-ttu-id="4cb00-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="4cb00-131">**Attribute**</span></span>|<span data-ttu-id="4cb00-132">**型**</span><span class="sxs-lookup"><span data-stu-id="4cb00-132">**Type**</span></span>|<span data-ttu-id="4cb00-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="4cb00-133">**Required**</span></span>|<span data-ttu-id="4cb00-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cb00-134">**Description**</span></span>|<span data-ttu-id="4cb00-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4cb00-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4cb00-136">E</span><span class="sxs-lookup"><span data-stu-id="4cb00-136">E</span></span>  <br/> |<span data-ttu-id="4cb00-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4cb00-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4cb00-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb00-138">optional</span></span>  <br/> |<span data-ttu-id="4cb00-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="4cb00-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="4cb00-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="4cb00-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="4cb00-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="4cb00-142">F</span></span>  <br/> |<span data-ttu-id="4cb00-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4cb00-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4cb00-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb00-144">optional</span></span>  <br/> | <span data-ttu-id="4cb00-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="4cb00-145">Represents the element's formula.</span></span> <span data-ttu-id="4cb00-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="4cb00-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="4cb00-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="4cb00-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="4cb00-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="4cb00-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="4cb00-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="4cb00-151">N</span><span class="sxs-lookup"><span data-stu-id="4cb00-151">N</span></span>  <br/> |<span data-ttu-id="4cb00-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4cb00-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4cb00-153">必須</span><span class="sxs-lookup"><span data-stu-id="4cb00-153">required</span></span>  <br/> |<span data-ttu-id="4cb00-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="4cb00-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="4cb00-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="4cb00-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cb00-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="4cb00-157">U</span><span class="sxs-lookup"><span data-stu-id="4cb00-157">U</span></span>  <br/> |<span data-ttu-id="4cb00-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4cb00-158">xsd:string</span></span>  <br/> |<span data-ttu-id="4cb00-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb00-159">optional</span></span>  <br/> |<span data-ttu-id="4cb00-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="4cb00-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="4cb00-162">V</span><span class="sxs-lookup"><span data-stu-id="4cb00-162">V</span></span>  <br/> |<span data-ttu-id="4cb00-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4cb00-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4cb00-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cb00-164">optional</span></span>  <br/> |<span data-ttu-id="4cb00-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="4cb00-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="4cb00-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="4cb00-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cb00-167">注釈</span><span class="sxs-lookup"><span data-stu-id="4cb00-167">Remarks</span></span>

<span data-ttu-id="4cb00-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb00-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="4cb00-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cb00-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="4cb00-170">**値**</span><span class="sxs-lookup"><span data-stu-id="4cb00-170">**Value**</span></span>|<span data-ttu-id="4cb00-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cb00-171">**Description**</span></span>|<span data-ttu-id="4cb00-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="4cb00-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4cb00-173">X</span><span class="sxs-lookup"><span data-stu-id="4cb00-173">X</span></span>  <br/> |<span data-ttu-id="4cb00-174">無限線上の点の x 座標です。対応する y 座標は [Y] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-174">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the Y cell.</span></span>  <br/> |<span data-ttu-id="4cb00-175">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4cb00-175">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="4cb00-176">Y</span><span class="sxs-lookup"><span data-stu-id="4cb00-176">Y</span></span>  <br/> |<span data-ttu-id="4cb00-177">無限線上の点の y 座標です。対応する x 座標は [X] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-177">A y-coordinate of a point on the infinite line; paired with x-coordinate represented by the X cell.</span></span>  <br/> |<span data-ttu-id="4cb00-178">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4cb00-178">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="4cb00-179">A</span><span class="sxs-lookup"><span data-stu-id="4cb00-179">A</span></span>  <br/> |<span data-ttu-id="4cb00-180">無限線上の点の x 座標です。対応する y 座標は [B] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-180">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the B cell.</span></span>  <br/> |<span data-ttu-id="4cb00-181">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4cb00-181">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="4cb00-182">B</span><span class="sxs-lookup"><span data-stu-id="4cb00-182">B</span></span>  <br/> |<span data-ttu-id="4cb00-183">無限線上の点の y 座標です。対応する x 座標は [A] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="4cb00-183">A y-coordinate of a point on an infinite line; paired with x-coordinate represented by the A cell.</span></span>  <br/> |<span data-ttu-id="4cb00-184">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="4cb00-184">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
   

