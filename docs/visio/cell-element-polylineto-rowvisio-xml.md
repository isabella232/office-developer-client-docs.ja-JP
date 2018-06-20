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
# <a name="cell-element-polylineto-row-visio-xml"></a><span data-ttu-id="43004-103">セル要素 ([polylineto] 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="43004-103">Cell element (PolyLineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="43004-104">X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43004-104">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43004-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="43004-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43004-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="43004-106">**Element type**</span></span> <br/> |[<span data-ttu-id="43004-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="43004-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="43004-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="43004-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="43004-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="43004-109">**Schema file**</span></span> <br/> |<span data-ttu-id="43004-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="43004-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="43004-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="43004-111">**Document parts**</span></span> <br/> |<span data-ttu-id="43004-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="43004-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43004-113">定義</span><span class="sxs-lookup"><span data-stu-id="43004-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43004-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="43004-114">Elements and attributes</span></span>

<span data-ttu-id="43004-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43004-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="43004-116">親要素</span><span class="sxs-lookup"><span data-stu-id="43004-116">Parent elements</span></span>

|<span data-ttu-id="43004-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="43004-117">**Element**</span></span>|<span data-ttu-id="43004-118">**型**</span><span class="sxs-lookup"><span data-stu-id="43004-118">**Type**</span></span>|<span data-ttu-id="43004-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="43004-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43004-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="43004-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="43004-121">PolylineTo_Type</span><span class="sxs-lookup"><span data-stu-id="43004-121">PolylineTo_Type</span></span>](polylineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="43004-122">X 座標または y 座標ポリラインまたはポリラインの数式の最後の点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43004-122">Contains x- or y-coordinates of the last point of a polyline or a polyline formula.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43004-123">子要素</span><span class="sxs-lookup"><span data-stu-id="43004-123">Child elements</span></span>

|<span data-ttu-id="43004-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="43004-124">**Element**</span></span>|<span data-ttu-id="43004-125">**型**</span><span class="sxs-lookup"><span data-stu-id="43004-125">**Type**</span></span>|<span data-ttu-id="43004-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="43004-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43004-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="43004-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43004-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="43004-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="43004-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="43004-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="43004-130">属性</span><span class="sxs-lookup"><span data-stu-id="43004-130">Attributes</span></span>

|<span data-ttu-id="43004-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="43004-131">**Attribute**</span></span>|<span data-ttu-id="43004-132">**型**</span><span class="sxs-lookup"><span data-stu-id="43004-132">**Type**</span></span>|<span data-ttu-id="43004-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="43004-133">**Required**</span></span>|<span data-ttu-id="43004-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="43004-134">**Description**</span></span>|<span data-ttu-id="43004-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="43004-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43004-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="43004-136">E</span></span>  <br/> |<span data-ttu-id="43004-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43004-137">xsd:string</span></span>  <br/> |<span data-ttu-id="43004-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="43004-138">optional</span></span>  <br/> |<span data-ttu-id="43004-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="43004-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="43004-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="43004-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="43004-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="43004-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="43004-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="43004-142">F</span></span>  <br/> |<span data-ttu-id="43004-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43004-143">xsd:string</span></span>  <br/> |<span data-ttu-id="43004-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="43004-144">optional</span></span>  <br/> | <span data-ttu-id="43004-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="43004-145">Represents the element's formula.</span></span> <span data-ttu-id="43004-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="43004-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="43004-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="43004-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="43004-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="43004-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="43004-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="43004-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="43004-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="43004-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="43004-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="43004-151">N</span></span>  <br/> |<span data-ttu-id="43004-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43004-152">xsd:string</span></span>  <br/> |<span data-ttu-id="43004-153">必須</span><span class="sxs-lookup"><span data-stu-id="43004-153">required</span></span>  <br/> |<span data-ttu-id="43004-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="43004-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="43004-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="43004-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="43004-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43004-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="43004-157">U</span><span class="sxs-lookup"><span data-stu-id="43004-157">U</span></span>  <br/> |<span data-ttu-id="43004-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43004-158">xsd:string</span></span>  <br/> |<span data-ttu-id="43004-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="43004-159">optional</span></span>  <br/> |<span data-ttu-id="43004-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="43004-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="43004-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="43004-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="43004-162">V</span><span class="sxs-lookup"><span data-stu-id="43004-162">V</span></span>  <br/> |<span data-ttu-id="43004-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43004-163">xsd:string</span></span>  <br/> |<span data-ttu-id="43004-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="43004-164">optional</span></span>  <br/> |<span data-ttu-id="43004-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="43004-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="43004-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="43004-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43004-167">備考</span><span class="sxs-lookup"><span data-stu-id="43004-167">Remarks</span></span>

<span data-ttu-id="43004-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="43004-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="43004-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43004-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="43004-170">**値**</span><span class="sxs-lookup"><span data-stu-id="43004-170">**Value**</span></span>|<span data-ttu-id="43004-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="43004-171">**Description**</span></span>|<span data-ttu-id="43004-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="43004-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43004-173">X</span><span class="sxs-lookup"><span data-stu-id="43004-173">X</span></span>  <br/> |<span data-ttu-id="43004-174">ポリラインの終点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="43004-174">The x-coordinate of the ending vertex of a polyline.</span></span>  <br/> |<span data-ttu-id="43004-175">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="43004-175">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="43004-176">Y</span><span class="sxs-lookup"><span data-stu-id="43004-176">Y</span></span>  <br/> |<span data-ttu-id="43004-177">ポリラインの終点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="43004-177">The y-coordinate of the ending vertex of a polyline.</span></span>  <br/> |<span data-ttu-id="43004-178">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="43004-178">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="43004-179">A</span><span class="sxs-lookup"><span data-stu-id="43004-179">A</span></span>  <br/> |<span data-ttu-id="43004-180">ポリラインの数式です。</span><span class="sxs-lookup"><span data-stu-id="43004-180">The polyline formula.</span></span>  <br/> |<span data-ttu-id="43004-181">[[PolylineTo] 行 ([Geometry] セクション)](polylineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="43004-181">[PolylineTo Row (Geometry Section)](polylineto-row-geometry-section.md)</span></span> <br/> |
   

