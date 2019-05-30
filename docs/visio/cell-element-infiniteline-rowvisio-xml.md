---
title: Cell 要素 ([Infiniteline] Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e14b8246-0064-3a54-7bd6-ad28180f9ea6
description: 無限線上にある2つの点の x 座標または y 座標を格納します。
ms.openlocfilehash: 1198e516a15e829b9a2da23491ca5f75e88a8e7d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539773"
---
# <a name="cell-element-infiniteline-row-visio-xml"></a><span data-ttu-id="0d91b-103">Cell 要素 ([Infiniteline] Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0d91b-103">Cell element (InfiniteLine Row) (Visio XML)</span></span>

<span data-ttu-id="0d91b-104">無限線上にある2つの点の x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-104">Contains the x- or y-coordinates of two points on an infinite line.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d91b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0d91b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d91b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0d91b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0d91b-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0d91b-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0d91b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0d91b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0d91b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0d91b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0d91b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="0d91b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0d91b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0d91b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0d91b-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="0d91b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d91b-113">定義</span><span class="sxs-lookup"><span data-stu-id="0d91b-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d91b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0d91b-114">Elements and attributes</span></span>

<span data-ttu-id="0d91b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d91b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0d91b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0d91b-116">Parent elements</span></span>

|<span data-ttu-id="0d91b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0d91b-117">**Element**</span></span>|<span data-ttu-id="0d91b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0d91b-118">**Type**</span></span>|<span data-ttu-id="0d91b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d91b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d91b-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="0d91b-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0d91b-121">InfiniteLine_Type</span><span class="sxs-lookup"><span data-stu-id="0d91b-121">InfiniteLine_Type</span></span>](infiniteline_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d91b-122">無限線上にある2つの点の x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-122">Contains the x- or y-coordinates of two points on an infinite line.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d91b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0d91b-123">Child elements</span></span>

|<span data-ttu-id="0d91b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d91b-124">**Element**</span></span>|<span data-ttu-id="0d91b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0d91b-125">**Type**</span></span>|<span data-ttu-id="0d91b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d91b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d91b-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="0d91b-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d91b-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="0d91b-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d91b-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0d91b-130">属性</span><span class="sxs-lookup"><span data-stu-id="0d91b-130">Attributes</span></span>

|<span data-ttu-id="0d91b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="0d91b-131">**Attribute**</span></span>|<span data-ttu-id="0d91b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="0d91b-132">**Type**</span></span>|<span data-ttu-id="0d91b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="0d91b-133">**Required**</span></span>|<span data-ttu-id="0d91b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d91b-134">**Description**</span></span>|<span data-ttu-id="0d91b-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0d91b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d91b-136">E</span><span class="sxs-lookup"><span data-stu-id="0d91b-136">E</span></span>  <br/> |<span data-ttu-id="0d91b-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0d91b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0d91b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d91b-138">optional</span></span>  <br/> |<span data-ttu-id="0d91b-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="0d91b-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="0d91b-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="0d91b-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="0d91b-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="0d91b-142">F</span><span class="sxs-lookup"><span data-stu-id="0d91b-142">F</span></span>  <br/> |<span data-ttu-id="0d91b-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0d91b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0d91b-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d91b-144">optional</span></span>  <br/> | <span data-ttu-id="0d91b-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-145">Represents the element's formula.</span></span> <span data-ttu-id="0d91b-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0d91b-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="0d91b-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="0d91b-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="0d91b-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="0d91b-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="0d91b-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="0d91b-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="0d91b-150">数式。</span><span class="sxs-lookup"><span data-stu-id="0d91b-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="0d91b-151">N</span><span class="sxs-lookup"><span data-stu-id="0d91b-151">N</span></span>  <br/> |<span data-ttu-id="0d91b-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0d91b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0d91b-153">必須</span><span class="sxs-lookup"><span data-stu-id="0d91b-153">required</span></span>  <br/> |<span data-ttu-id="0d91b-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="0d91b-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="0d91b-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d91b-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="0d91b-157">U</span><span class="sxs-lookup"><span data-stu-id="0d91b-157">U</span></span>  <br/> |<span data-ttu-id="0d91b-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0d91b-158">xsd:string</span></span>  <br/> |<span data-ttu-id="0d91b-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d91b-159">optional</span></span>  <br/> |<span data-ttu-id="0d91b-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="0d91b-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="0d91b-162">V</span><span class="sxs-lookup"><span data-stu-id="0d91b-162">V</span></span>  <br/> |<span data-ttu-id="0d91b-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0d91b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="0d91b-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d91b-164">optional</span></span>  <br/> |<span data-ttu-id="0d91b-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="0d91b-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d91b-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d91b-167">注釈</span><span class="sxs-lookup"><span data-stu-id="0d91b-167">Remarks</span></span>

<span data-ttu-id="0d91b-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d91b-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="0d91b-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d91b-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="0d91b-170">**値**</span><span class="sxs-lookup"><span data-stu-id="0d91b-170">**Value**</span></span>|<span data-ttu-id="0d91b-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d91b-171">**Description**</span></span>|<span data-ttu-id="0d91b-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="0d91b-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d91b-173">X</span><span class="sxs-lookup"><span data-stu-id="0d91b-173">X</span></span>  <br/> |<span data-ttu-id="0d91b-174">無限線上の点の x 座標です。対応する y 座標は [Y] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="0d91b-174">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the Y cell.</span></span>  <br/> |<span data-ttu-id="0d91b-175">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0d91b-175">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0d91b-176">Y</span><span class="sxs-lookup"><span data-stu-id="0d91b-176">Y</span></span>  <br/> |<span data-ttu-id="0d91b-177">無限線上の点の y 座標です。対応する x 座標は [X] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="0d91b-177">A y-coordinate of a point on the infinite line; paired with x-coordinate represented by the X cell.</span></span>  <br/> |<span data-ttu-id="0d91b-178">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0d91b-178">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0d91b-179">A</span><span class="sxs-lookup"><span data-stu-id="0d91b-179">A</span></span>  <br/> |<span data-ttu-id="0d91b-180">無限線上の点の x 座標です。対応する y 座標は [B] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="0d91b-180">An x-coordinate of a point on the infinite line; paired with y-coordinate represented by the B cell.</span></span>  <br/> |<span data-ttu-id="0d91b-181">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0d91b-181">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="0d91b-182">B</span><span class="sxs-lookup"><span data-stu-id="0d91b-182">B</span></span>  <br/> |<span data-ttu-id="0d91b-183">無限線上の点の y 座標です。対応する x 座標は [A] セルで表されます。</span><span class="sxs-lookup"><span data-stu-id="0d91b-183">A y-coordinate of a point on an infinite line; paired with x-coordinate represented by the A cell.</span></span>  <br/> |<span data-ttu-id="0d91b-184">[[InfiniteLine] 行 ([Geometry] セクション)](infiniteline-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="0d91b-184">[InfiniteLine Row (Geometry Section)](infiniteline-row-geometry-section.md)</span></span> <br/> |
   

