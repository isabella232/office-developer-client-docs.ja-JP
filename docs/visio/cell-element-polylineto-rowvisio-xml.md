---
title: セル要素 ([polylineto] 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a62fbb51-e2a7-cdae-3516-5ce9ba30f26d
description: X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。
ms.openlocfilehash: 485682b43db045893bfc968cfb0859cf8cb2ce2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804970"
---
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="09e8b-103">セル要素 ([polylineto] 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="09e8b-103">Cell element (PolyLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="09e8b-104">X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09e8b-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09e8b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="09e8b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09e8b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="09e8b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="09e8b-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="09e8b-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="09e8b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="09e8b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="09e8b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="09e8b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="09e8b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="09e8b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="09e8b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="09e8b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="09e8b-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="09e8b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09e8b-113">定義</span><span class="sxs-lookup"><span data-stu-id="09e8b-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09e8b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="09e8b-114">Elements and attributes</span></span>

<span data-ttu-id="09e8b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09e8b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="09e8b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="09e8b-116">Parent elements</span></span>

|<span data-ttu-id="09e8b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="09e8b-117">**Element**</span></span>|<span data-ttu-id="09e8b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="09e8b-118">**Type**</span></span>|<span data-ttu-id="09e8b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="09e8b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09e8b-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="09e8b-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="09e8b-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="09e8b-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09e8b-122">X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09e8b-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="09e8b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="09e8b-123">Child elements</span></span>

|<span data-ttu-id="09e8b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="09e8b-124">**Element**</span></span>|<span data-ttu-id="09e8b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="09e8b-125">**Type**</span></span>|<span data-ttu-id="09e8b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="09e8b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09e8b-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="09e8b-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09e8b-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="09e8b-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09e8b-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="09e8b-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="09e8b-130">属性</span><span class="sxs-lookup"><span data-stu-id="09e8b-130">Attributes</span></span>

|<span data-ttu-id="09e8b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="09e8b-131">**Attribute**</span></span>|<span data-ttu-id="09e8b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="09e8b-132">**Type**</span></span>|<span data-ttu-id="09e8b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="09e8b-133">**Required**</span></span>|<span data-ttu-id="09e8b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="09e8b-134">**Description**</span></span>|<span data-ttu-id="09e8b-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="09e8b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09e8b-136">E</span><span class="sxs-lookup"><span data-stu-id="09e8b-136">E</span></span>  <br/> |<span data-ttu-id="09e8b-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e8b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="09e8b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="09e8b-138">optional</span></span>  <br/> |<span data-ttu-id="09e8b-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="09e8b-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="09e8b-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="09e8b-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="09e8b-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="09e8b-142">F</span></span>  <br/> |<span data-ttu-id="09e8b-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e8b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="09e8b-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="09e8b-144">optional</span></span>  <br/> | <span data-ttu-id="09e8b-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="09e8b-145">Represents the element's formula.</span></span> <span data-ttu-id="09e8b-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="09e8b-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="09e8b-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="09e8b-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="09e8b-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="09e8b-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="09e8b-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="09e8b-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="09e8b-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="09e8b-151">N</span><span class="sxs-lookup"><span data-stu-id="09e8b-151">N</span></span>  <br/> |<span data-ttu-id="09e8b-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e8b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="09e8b-153">必須</span><span class="sxs-lookup"><span data-stu-id="09e8b-153">required</span></span>  <br/> |<span data-ttu-id="09e8b-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="09e8b-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="09e8b-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="09e8b-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09e8b-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="09e8b-157">U</span><span class="sxs-lookup"><span data-stu-id="09e8b-157">U</span></span>  <br/> |<span data-ttu-id="09e8b-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e8b-158">xsd:string</span></span>  <br/> |<span data-ttu-id="09e8b-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="09e8b-159">optional</span></span>  <br/> |<span data-ttu-id="09e8b-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="09e8b-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="09e8b-162">V</span><span class="sxs-lookup"><span data-stu-id="09e8b-162">V</span></span>  <br/> |<span data-ttu-id="09e8b-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e8b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="09e8b-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="09e8b-164">optional</span></span>  <br/> |<span data-ttu-id="09e8b-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="09e8b-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="09e8b-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09e8b-167">注釈</span><span class="sxs-lookup"><span data-stu-id="09e8b-167">Remarks</span></span>

<span data-ttu-id="09e8b-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="09e8b-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="09e8b-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09e8b-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="09e8b-170">**値**</span><span class="sxs-lookup"><span data-stu-id="09e8b-170">**Value**</span></span>|<span data-ttu-id="09e8b-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="09e8b-171">**Description**</span></span>|<span data-ttu-id="09e8b-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="09e8b-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09e8b-173">X</span><span class="sxs-lookup"><span data-stu-id="09e8b-173">X</span></span>  <br/> |<span data-ttu-id="09e8b-174">ポリラインの最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |<span data-ttu-id="09e8b-175">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="09e8b-175">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="09e8b-176">Y</span><span class="sxs-lookup"><span data-stu-id="09e8b-176">Y</span></span>  <br/> |<span data-ttu-id="09e8b-177">ポリラインの最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |<span data-ttu-id="09e8b-178">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="09e8b-178">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="09e8b-179">A</span><span class="sxs-lookup"><span data-stu-id="09e8b-179">A</span></span>  <br/> |<span data-ttu-id="09e8b-180">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="09e8b-180">The polyline formula.</span></span>  <br/> |<span data-ttu-id="09e8b-181">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="09e8b-181">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
   

