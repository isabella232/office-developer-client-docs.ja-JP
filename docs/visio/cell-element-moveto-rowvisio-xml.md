---
title: セル要素 ([moveto] 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3b2a08f-07a0-5f1c-4910-503229927816
description: 図形の最初の頂点の x 座標または y 座標が含まれていますか、パス内の改行の後の最初の頂点の x 座標または y 座標を表します。
ms.openlocfilehash: dbcf8d111ab86671fb2aeb073d2a13f40810f941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804962"
---
# <a name="cell-element-moveto-row-visio-xml"></a><span data-ttu-id="89547-103">セル要素 ([moveto] 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="89547-103">Cell element (MoveTo Row) ('Visio XML')</span></span>

<span data-ttu-id="89547-104">図形の最初の頂点の x 座標または y 座標が含まれていますか、パス内の改行の後の最初の頂点の x 座標または y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-104">Contains the x- or y-coordinates of the first vertex of a shape, or represents the x- or y-coordinates of the first vertex after a break in a path.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89547-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="89547-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89547-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="89547-106">**Element type**</span></span> <br/> |[<span data-ttu-id="89547-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="89547-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="89547-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="89547-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="89547-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="89547-109">**Schema file**</span></span> <br/> |<span data-ttu-id="89547-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="89547-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="89547-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="89547-111">**Document parts**</span></span> <br/> |<span data-ttu-id="89547-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="89547-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="89547-113">定義</span><span class="sxs-lookup"><span data-stu-id="89547-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="89547-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="89547-114">Elements and attributes</span></span>

<span data-ttu-id="89547-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89547-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="89547-116">親要素</span><span class="sxs-lookup"><span data-stu-id="89547-116">Parent elements</span></span>

|<span data-ttu-id="89547-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="89547-117">**Element**</span></span>|<span data-ttu-id="89547-118">**型**</span><span class="sxs-lookup"><span data-stu-id="89547-118">**Type**</span></span>|<span data-ttu-id="89547-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="89547-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="89547-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="89547-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="89547-121">MoveTo_Type</span><span class="sxs-lookup"><span data-stu-id="89547-121">MoveTo_Type</span></span>](moveto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="89547-122">図形の最初の頂点の x 座標または y 座標が含まれていますか、パス内の改行の後の最初の頂点の x 座標または y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-122">Contains the x- or y-coordinates of the first vertex of a shape, or represents the x- or y-coordinates of the first vertex after a break in a path.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="89547-123">子要素</span><span class="sxs-lookup"><span data-stu-id="89547-123">Child elements</span></span>

|<span data-ttu-id="89547-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="89547-124">**Element**</span></span>|<span data-ttu-id="89547-125">**型**</span><span class="sxs-lookup"><span data-stu-id="89547-125">**Type**</span></span>|<span data-ttu-id="89547-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="89547-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="89547-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="89547-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="89547-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="89547-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="89547-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="89547-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="89547-130">属性</span><span class="sxs-lookup"><span data-stu-id="89547-130">Attributes</span></span>

|<span data-ttu-id="89547-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="89547-131">**Attribute**</span></span>|<span data-ttu-id="89547-132">**型**</span><span class="sxs-lookup"><span data-stu-id="89547-132">**Type**</span></span>|<span data-ttu-id="89547-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="89547-133">**Required**</span></span>|<span data-ttu-id="89547-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="89547-134">**Description**</span></span>|<span data-ttu-id="89547-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="89547-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="89547-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="89547-136">E</span></span>  <br/> |<span data-ttu-id="89547-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="89547-137">xsd:string</span></span>  <br/> |<span data-ttu-id="89547-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="89547-138">optional</span></span>  <br/> |<span data-ttu-id="89547-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="89547-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="89547-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="89547-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="89547-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="89547-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="89547-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="89547-142">F</span></span>  <br/> |<span data-ttu-id="89547-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="89547-143">xsd:string</span></span>  <br/> |<span data-ttu-id="89547-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="89547-144">optional</span></span>  <br/> | <span data-ttu-id="89547-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-145">Represents the element's formula.</span></span> <span data-ttu-id="89547-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89547-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="89547-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="89547-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="89547-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="89547-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="89547-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="89547-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="89547-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="89547-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="89547-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="89547-151">N</span></span>  <br/> |<span data-ttu-id="89547-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="89547-152">xsd:string</span></span>  <br/> |<span data-ttu-id="89547-153">必須</span><span class="sxs-lookup"><span data-stu-id="89547-153">required</span></span>  <br/> |<span data-ttu-id="89547-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="89547-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="89547-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="89547-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89547-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="89547-157">U</span><span class="sxs-lookup"><span data-stu-id="89547-157">U</span></span>  <br/> |<span data-ttu-id="89547-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="89547-158">xsd:string</span></span>  <br/> |<span data-ttu-id="89547-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="89547-159">optional</span></span>  <br/> |<span data-ttu-id="89547-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="89547-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="89547-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="89547-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="89547-162">V</span><span class="sxs-lookup"><span data-stu-id="89547-162">V</span></span>  <br/> |<span data-ttu-id="89547-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="89547-163">xsd:string</span></span>  <br/> |<span data-ttu-id="89547-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="89547-164">optional</span></span>  <br/> |<span data-ttu-id="89547-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="89547-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="89547-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89547-167">備考</span><span class="sxs-lookup"><span data-stu-id="89547-167">Remarks</span></span>

<span data-ttu-id="89547-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="89547-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="89547-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89547-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="89547-170">**値**</span><span class="sxs-lookup"><span data-stu-id="89547-170">**Value**</span></span>|<span data-ttu-id="89547-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="89547-171">**Description**</span></span>|<span data-ttu-id="89547-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="89547-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89547-173">X</span><span class="sxs-lookup"><span data-stu-id="89547-173">X</span></span>  <br/> |<span data-ttu-id="89547-174">**[Moveto]** 行がセクションの最初の行の場合は、[ **X** ] セルは、図形の最初の頂点の x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-174">If the **MoveTo** row is the first row in the section, the **X** cell represents the x-coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="89547-175">**[Moveto]** 行は、2 つの行の間で表示されている場合、[ **X** ] セルは、パスを切断した後最初の頂点の x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-175">If the **MoveTo** row appears between two rows, the **X** cell represents the x-coordinate of the first vertex after the break in the path.</span></span>  <br/> |<span data-ttu-id="89547-176">[[MoveTo] 行 ([Geometry] セクション)](moveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="89547-176">[MoveTo Row (Geometry Section)](moveto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="89547-177">Y</span><span class="sxs-lookup"><span data-stu-id="89547-177">Y</span></span>  <br/> |<span data-ttu-id="89547-178">**[Moveto]** 行がセクションの最初の行の場合は、[ **Y** ] セルは、図形の最初の頂点の y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-178">If the **MoveTo** row is the first row in the section, the **Y** cell represents the y-coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="89547-179">2 つの行の間、 **[moveto]** 行が表示されたら、[ **Y** ] セルは、パスを切断した後の最初の頂点の y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="89547-179">If the **MoveTo** row appears between two rows, the **Y** cell represents the y-coordinate of the first vertex after the break in the path.</span></span>  <br/> |<span data-ttu-id="89547-180">[[MoveTo] 行 ([Geometry] セクション)](moveto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="89547-180">[MoveTo Row (Geometry Section)](moveto-row-geometry-section.md)</span></span> <br/> |
   

