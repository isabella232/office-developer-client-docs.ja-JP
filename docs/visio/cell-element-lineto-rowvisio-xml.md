---
title: Cell 要素 (LineTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: 直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。
ms.openlocfilehash: 4b1628549e659712a1c2e79ae0fbf53d594e18f9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539510"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="6d95c-103">Cell 要素 (LineTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6d95c-103">Cell element (LineTo Row) (Visio XML)</span></span>

<span data-ttu-id="6d95c-104">直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d95c-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="6d95c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d95c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6d95c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6d95c-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6d95c-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6d95c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6d95c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6d95c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6d95c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6d95c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6d95c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6d95c-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="6d95c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6d95c-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="6d95c-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6d95c-113">定義</span><span class="sxs-lookup"><span data-stu-id="6d95c-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6d95c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6d95c-114">Elements and attributes</span></span>

<span data-ttu-id="6d95c-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d95c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6d95c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6d95c-116">Parent elements</span></span>

|<span data-ttu-id="6d95c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6d95c-117">**Element**</span></span>|<span data-ttu-id="6d95c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6d95c-118">**Type**</span></span>|<span data-ttu-id="6d95c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d95c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d95c-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="6d95c-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6d95c-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="6d95c-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6d95c-122">直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6d95c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6d95c-123">Child elements</span></span>

|<span data-ttu-id="6d95c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d95c-124">**Element**</span></span>|<span data-ttu-id="6d95c-125">**型**</span><span class="sxs-lookup"><span data-stu-id="6d95c-125">**Type**</span></span>|<span data-ttu-id="6d95c-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d95c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6d95c-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="6d95c-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6d95c-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="6d95c-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6d95c-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6d95c-130">属性</span><span class="sxs-lookup"><span data-stu-id="6d95c-130">Attributes</span></span>

|<span data-ttu-id="6d95c-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="6d95c-131">**Attribute**</span></span>|<span data-ttu-id="6d95c-132">**型**</span><span class="sxs-lookup"><span data-stu-id="6d95c-132">**Type**</span></span>|<span data-ttu-id="6d95c-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="6d95c-133">**Required**</span></span>|<span data-ttu-id="6d95c-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d95c-134">**Description**</span></span>|<span data-ttu-id="6d95c-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="6d95c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6d95c-136">E</span><span class="sxs-lookup"><span data-stu-id="6d95c-136">E</span></span>  <br/> |<span data-ttu-id="6d95c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d95c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6d95c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d95c-138">optional</span></span>  <br/> |<span data-ttu-id="6d95c-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="6d95c-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="6d95c-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="6d95c-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="6d95c-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="6d95c-142">F</span><span class="sxs-lookup"><span data-stu-id="6d95c-142">F</span></span>  <br/> |<span data-ttu-id="6d95c-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d95c-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6d95c-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d95c-144">optional</span></span>  <br/> | <span data-ttu-id="6d95c-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-145">Represents the element's formula.</span></span> <span data-ttu-id="6d95c-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="6d95c-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="6d95c-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="6d95c-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="6d95c-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="6d95c-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="6d95c-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="6d95c-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="6d95c-150">数式。</span><span class="sxs-lookup"><span data-stu-id="6d95c-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="6d95c-151">N</span><span class="sxs-lookup"><span data-stu-id="6d95c-151">N</span></span>  <br/> |<span data-ttu-id="6d95c-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d95c-152">xsd:string</span></span>  <br/> |<span data-ttu-id="6d95c-153">必須</span><span class="sxs-lookup"><span data-stu-id="6d95c-153">required</span></span>  <br/> |<span data-ttu-id="6d95c-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="6d95c-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="6d95c-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d95c-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="6d95c-157">U</span><span class="sxs-lookup"><span data-stu-id="6d95c-157">U</span></span>  <br/> |<span data-ttu-id="6d95c-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d95c-158">xsd:string</span></span>  <br/> |<span data-ttu-id="6d95c-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d95c-159">optional</span></span>  <br/> |<span data-ttu-id="6d95c-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="6d95c-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="6d95c-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="6d95c-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="6d95c-162">V</span><span class="sxs-lookup"><span data-stu-id="6d95c-162">V</span></span>  <br/> |<span data-ttu-id="6d95c-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6d95c-163">xsd:string</span></span>  <br/> |<span data-ttu-id="6d95c-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="6d95c-164">optional</span></span>  <br/> |<span data-ttu-id="6d95c-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="6d95c-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d95c-167">注釈</span><span class="sxs-lookup"><span data-stu-id="6d95c-167">Remarks</span></span>

<span data-ttu-id="6d95c-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d95c-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="6d95c-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="6d95c-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="6d95c-170">**値**</span><span class="sxs-lookup"><span data-stu-id="6d95c-170">**Value**</span></span>|<span data-ttu-id="6d95c-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d95c-171">**Description**</span></span>|<span data-ttu-id="6d95c-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="6d95c-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d95c-173">X</span><span class="sxs-lookup"><span data-stu-id="6d95c-173">X</span></span>  <br/> |<span data-ttu-id="6d95c-174">直線セグメントの最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="6d95c-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |<span data-ttu-id="6d95c-175">[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="6d95c-175">[LineTo Row (Geometry Section)](lineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="6d95c-176">Y</span><span class="sxs-lookup"><span data-stu-id="6d95c-176">Y</span></span>  <br/> |<span data-ttu-id="6d95c-177">直線セグメントの最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="6d95c-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |<span data-ttu-id="6d95c-178">[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="6d95c-178">[LineTo Row (Geometry Section)](lineto-row-geometry-section.md)</span></span> <br/> |
   

