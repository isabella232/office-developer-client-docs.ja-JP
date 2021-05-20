---
title: Cell 要素 (RelLineTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 44d369f0-ab37-75ca-727e-b421d6f95ba7
description: 図形の幅と高さに相対する、直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。
ms.openlocfilehash: 1a3277eac2b0f759d3da6cb93b5339f97a5ac876
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539419"
---
# <a name="cell-element-rellineto-row-visio-xml"></a><span data-ttu-id="bf041-103">Cell 要素 (RelLineTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bf041-103">Cell element (RelLineTo Row) (Visio XML)</span></span>

<span data-ttu-id="bf041-104">図形の幅と高さに相対する、直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="bf041-104">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf041-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="bf041-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf041-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="bf041-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bf041-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="bf041-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bf041-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bf041-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bf041-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bf041-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bf041-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bf041-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bf041-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="bf041-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bf041-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="bf041-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf041-113">定義</span><span class="sxs-lookup"><span data-stu-id="bf041-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf041-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bf041-114">Elements and attributes</span></span>

<span data-ttu-id="bf041-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf041-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bf041-116">親要素</span><span class="sxs-lookup"><span data-stu-id="bf041-116">Parent elements</span></span>

|<span data-ttu-id="bf041-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="bf041-117">**Element**</span></span>|<span data-ttu-id="bf041-118">**型**</span><span class="sxs-lookup"><span data-stu-id="bf041-118">**Type**</span></span>|<span data-ttu-id="bf041-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf041-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf041-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="bf041-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="bf041-121">RelLineTo_Type</span><span class="sxs-lookup"><span data-stu-id="bf041-121">RelLineTo_Type</span></span>](rellineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bf041-122">図形の幅と高さに相対する、直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="bf041-122">Contains x-or y-coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bf041-123">子要素</span><span class="sxs-lookup"><span data-stu-id="bf041-123">Child elements</span></span>

|<span data-ttu-id="bf041-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf041-124">**Element**</span></span>|<span data-ttu-id="bf041-125">**型**</span><span class="sxs-lookup"><span data-stu-id="bf041-125">**Type**</span></span>|<span data-ttu-id="bf041-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf041-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf041-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="bf041-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bf041-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="bf041-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bf041-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf041-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bf041-130">属性</span><span class="sxs-lookup"><span data-stu-id="bf041-130">Attributes</span></span>

|<span data-ttu-id="bf041-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="bf041-131">**Attribute**</span></span>|<span data-ttu-id="bf041-132">**型**</span><span class="sxs-lookup"><span data-stu-id="bf041-132">**Type**</span></span>|<span data-ttu-id="bf041-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="bf041-133">**Required**</span></span>|<span data-ttu-id="bf041-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf041-134">**Description**</span></span>|<span data-ttu-id="bf041-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bf041-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf041-136">E</span><span class="sxs-lookup"><span data-stu-id="bf041-136">E</span></span>  <br/> |<span data-ttu-id="bf041-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bf041-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bf041-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="bf041-138">optional</span></span>  <br/> |<span data-ttu-id="bf041-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bf041-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="bf041-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="bf041-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="bf041-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="bf041-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="bf041-142">F</span><span class="sxs-lookup"><span data-stu-id="bf041-142">F</span></span>  <br/> |<span data-ttu-id="bf041-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bf041-143">xsd:string</span></span>  <br/> |<span data-ttu-id="bf041-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="bf041-144">optional</span></span>  <br/> | <span data-ttu-id="bf041-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="bf041-145">Represents the element's formula.</span></span> <span data-ttu-id="bf041-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="bf041-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="bf041-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="bf041-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="bf041-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="bf041-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="bf041-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="bf041-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="bf041-150">数式。</span><span class="sxs-lookup"><span data-stu-id="bf041-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="bf041-151">N</span><span class="sxs-lookup"><span data-stu-id="bf041-151">N</span></span>  <br/> |<span data-ttu-id="bf041-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bf041-152">xsd:string</span></span>  <br/> |<span data-ttu-id="bf041-153">必須</span><span class="sxs-lookup"><span data-stu-id="bf041-153">required</span></span>  <br/> |<span data-ttu-id="bf041-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="bf041-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="bf041-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf041-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="bf041-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf041-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="bf041-157">U</span><span class="sxs-lookup"><span data-stu-id="bf041-157">U</span></span>  <br/> |<span data-ttu-id="bf041-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bf041-158">xsd:string</span></span>  <br/> |<span data-ttu-id="bf041-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="bf041-159">optional</span></span>  <br/> |<span data-ttu-id="bf041-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="bf041-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="bf041-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="bf041-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="bf041-162">V</span><span class="sxs-lookup"><span data-stu-id="bf041-162">V</span></span>  <br/> |<span data-ttu-id="bf041-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="bf041-163">xsd:string</span></span>  <br/> |<span data-ttu-id="bf041-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="bf041-164">optional</span></span>  <br/> |<span data-ttu-id="bf041-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="bf041-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="bf041-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf041-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf041-167">注釈</span><span class="sxs-lookup"><span data-stu-id="bf041-167">Remarks</span></span>

<span data-ttu-id="bf041-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf041-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="bf041-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="bf041-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="bf041-170">**値**</span><span class="sxs-lookup"><span data-stu-id="bf041-170">**Value**</span></span>|<span data-ttu-id="bf041-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="bf041-171">**Description**</span></span>|<span data-ttu-id="bf041-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="bf041-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf041-173">X</span><span class="sxs-lookup"><span data-stu-id="bf041-173">X</span></span>  <br/> |<span data-ttu-id="bf041-174">図形の幅を基準にした直線セグメントの終了頂点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="bf041-174">The x-coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |[<span data-ttu-id="bf041-175">RelLineTo 行 (Geometry セクション)</span><span class="sxs-lookup"><span data-stu-id="bf041-175">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
|<span data-ttu-id="bf041-176">Y</span><span class="sxs-lookup"><span data-stu-id="bf041-176">Y</span></span>  <br/> |<span data-ttu-id="bf041-177">図形の高さを基準にした直線セグメントの終了頂点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="bf041-177">The y-coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |[<span data-ttu-id="bf041-178">RelLineTo 行 (Geometry セクション)</span><span class="sxs-lookup"><span data-stu-id="bf041-178">RelLineTo Row (Geometry Section)</span></span>](rellineto-row-geometry-section.md) <br/> |
   

