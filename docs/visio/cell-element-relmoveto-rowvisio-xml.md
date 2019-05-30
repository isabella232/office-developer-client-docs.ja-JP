---
title: Cell 要素 (RelMoveTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8e91497c-0aa1-2021-9317-cf989e5b84a3
description: 図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。
ms.openlocfilehash: 6ec7990887ed59ae229e88b6ad02a7759c770700
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539405"
---
# <a name="cell-element-relmoveto-row-visio-xml"></a><span data-ttu-id="57618-103">Cell 要素 (RelMoveTo Row) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="57618-103">Cell element (RelMoveTo Row) (Visio XML)</span></span>

<span data-ttu-id="57618-104">図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="57618-104">Contains the x- or y-coordinates of the first vertex of a shape, or the x- or y-coordinates of the first vertex after a break in a path, relative to the height and width of the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57618-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="57618-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57618-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="57618-106">**Element type**</span></span> <br/> |[<span data-ttu-id="57618-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="57618-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="57618-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="57618-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="57618-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="57618-109">**Schema file**</span></span> <br/> |<span data-ttu-id="57618-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="57618-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="57618-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="57618-111">**Document parts**</span></span> <br/> |<span data-ttu-id="57618-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="57618-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57618-113">定義</span><span class="sxs-lookup"><span data-stu-id="57618-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="57618-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="57618-114">Elements and attributes</span></span>

<span data-ttu-id="57618-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="57618-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="57618-116">親要素</span><span class="sxs-lookup"><span data-stu-id="57618-116">Parent elements</span></span>

|<span data-ttu-id="57618-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="57618-117">**Element**</span></span>|<span data-ttu-id="57618-118">**型**</span><span class="sxs-lookup"><span data-stu-id="57618-118">**Type**</span></span>|<span data-ttu-id="57618-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="57618-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="57618-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="57618-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="57618-121">RelMoveTo_Type</span><span class="sxs-lookup"><span data-stu-id="57618-121">RelMoveTo_Type</span></span>](relmoveto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="57618-122">図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。</span><span class="sxs-lookup"><span data-stu-id="57618-122">Contains the x- or y-coordinates of the first vertex of a shape, or the x- or y-coordinates of the first vertex after a break in a path, relative to the height and width of the shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="57618-123">子要素</span><span class="sxs-lookup"><span data-stu-id="57618-123">Child elements</span></span>

|<span data-ttu-id="57618-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="57618-124">**Element**</span></span>|<span data-ttu-id="57618-125">**型**</span><span class="sxs-lookup"><span data-stu-id="57618-125">**Type**</span></span>|<span data-ttu-id="57618-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="57618-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="57618-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="57618-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="57618-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="57618-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="57618-129">ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="57618-129">Specifies a reference to a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="57618-130">属性</span><span class="sxs-lookup"><span data-stu-id="57618-130">Attributes</span></span>

|<span data-ttu-id="57618-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="57618-131">**Attribute**</span></span>|<span data-ttu-id="57618-132">**型**</span><span class="sxs-lookup"><span data-stu-id="57618-132">**Type**</span></span>|<span data-ttu-id="57618-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="57618-133">**Required**</span></span>|<span data-ttu-id="57618-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="57618-134">**Description**</span></span>|<span data-ttu-id="57618-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="57618-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="57618-136">E</span><span class="sxs-lookup"><span data-stu-id="57618-136">E</span></span>  <br/> |<span data-ttu-id="57618-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57618-137">xsd:string</span></span>  <br/> |<span data-ttu-id="57618-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="57618-138">optional</span></span>  <br/> |<span data-ttu-id="57618-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="57618-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="57618-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="57618-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="57618-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="57618-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="57618-142">F</span><span class="sxs-lookup"><span data-stu-id="57618-142">F</span></span>  <br/> |<span data-ttu-id="57618-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57618-143">xsd:string</span></span>  <br/> |<span data-ttu-id="57618-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="57618-144">optional</span></span>  <br/> | <span data-ttu-id="57618-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-145">Represents the element's formula.</span></span> <span data-ttu-id="57618-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="57618-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="57618-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="57618-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="57618-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="57618-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="57618-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="57618-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="57618-150">数式。</span><span class="sxs-lookup"><span data-stu-id="57618-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="57618-151">N</span><span class="sxs-lookup"><span data-stu-id="57618-151">N</span></span>  <br/> |<span data-ttu-id="57618-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57618-152">xsd:string</span></span>  <br/> |<span data-ttu-id="57618-153">必須</span><span class="sxs-lookup"><span data-stu-id="57618-153">required</span></span>  <br/> |<span data-ttu-id="57618-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="57618-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="57618-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="57618-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57618-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="57618-157">U</span><span class="sxs-lookup"><span data-stu-id="57618-157">U</span></span>  <br/> |<span data-ttu-id="57618-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57618-158">xsd:string</span></span>  <br/> |<span data-ttu-id="57618-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="57618-159">optional</span></span>  <br/> |<span data-ttu-id="57618-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="57618-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="57618-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="57618-162">V</span><span class="sxs-lookup"><span data-stu-id="57618-162">V</span></span>  <br/> |<span data-ttu-id="57618-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="57618-163">xsd:string</span></span>  <br/> |<span data-ttu-id="57618-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="57618-164">optional</span></span>  <br/> |<span data-ttu-id="57618-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="57618-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="57618-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57618-167">注釈</span><span class="sxs-lookup"><span data-stu-id="57618-167">Remarks</span></span>

<span data-ttu-id="57618-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="57618-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="57618-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57618-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="57618-170">**値**</span><span class="sxs-lookup"><span data-stu-id="57618-170">**Value**</span></span>|<span data-ttu-id="57618-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="57618-171">**Description**</span></span>|<span data-ttu-id="57618-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="57618-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57618-173">X</span><span class="sxs-lookup"><span data-stu-id="57618-173">X</span></span>  <br/> |<span data-ttu-id="57618-174">[ **Relmoveto** ] 行がセクションの最初の行の場合、[ **x** ] セルは図形の幅を基準にして、図形の最初の頂点に対する x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-174">If the **RelMoveTo** row is the first row in the section, the **X** cell represents the x-coordinate of the first vertex of a shape relative to the width of the shape.</span></span> <span data-ttu-id="57618-175">2つの行の間に [ **Relmoveto** ] 行が表示されている場合、[ **x** ] セルは、パスを切断した後の最初の頂点に対する x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-175">If the **RelMoveTo** row appears between two rows, the **X** cell represents the x-coordinate of the first vertex after the break in the path.</span></span>  <br/> |[<span data-ttu-id="57618-176">「RelMoveTo」行 (「Geometry」セクション)</span><span class="sxs-lookup"><span data-stu-id="57618-176">RelMoveTo Row (Geometry Section)</span></span>](relmoveto-row-geometry-section.md) <br/> |
|<span data-ttu-id="57618-177">Y</span><span class="sxs-lookup"><span data-stu-id="57618-177">Y</span></span>  <br/> |<span data-ttu-id="57618-178">[ **Relmoveto** ] 行がセクションの最初の行の場合、[ **y** ] セルは、図形の高さを基準にして、図形の最初の頂点に対する y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-178">If the **RelMoveTo** row is the first row in the section, the **Y** cell represents the y-coordinate of the first vertex of a shape relative to the height of the shape.</span></span> <span data-ttu-id="57618-179">2つの行の間に [ **Relmoveto** ] 行が表示されている場合、[ **y** ] セルは、パスを切断した後の最初の頂点に対する y 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="57618-179">If the **RelMoveTo** row appears between two rows, the **Y** cell represents the y-coordinate of the first vertex after the break in the path.</span></span>  <br/> |[<span data-ttu-id="57618-180">「RelMoveTo」行 (「Geometry」セクション)</span><span class="sxs-lookup"><span data-stu-id="57618-180">RelMoveTo Row (Geometry Section)</span></span>](relmoveto-row-geometry-section.md) <br/> |
   

