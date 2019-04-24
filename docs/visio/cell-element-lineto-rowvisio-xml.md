---
title: Cell 要素 ([LineTo] 行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 64f2494d-2de7-6bc5-0db4-91b952bdcb5e
description: 直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。
ms.openlocfilehash: 5b7d8128cbef57c4dd9fb69d5b82e1c1c2ccef68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318202"
---
# <a name="cell-element-lineto-row-visio-xml"></a><span data-ttu-id="e3d52-103">Cell 要素 ([LineTo] 行) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e3d52-103">Cell element (LineTo Row) ('Visio XML')</span></span>

<span data-ttu-id="e3d52-104">直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-104">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3d52-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e3d52-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3d52-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e3d52-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e3d52-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e3d52-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e3d52-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e3d52-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e3d52-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e3d52-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e3d52-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="e3d52-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e3d52-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e3d52-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e3d52-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="e3d52-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e3d52-113">定義</span><span class="sxs-lookup"><span data-stu-id="e3d52-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e3d52-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e3d52-114">Elements and attributes</span></span>

<span data-ttu-id="e3d52-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3d52-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e3d52-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e3d52-116">Parent elements</span></span>

|<span data-ttu-id="e3d52-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e3d52-117">**Element**</span></span>|<span data-ttu-id="e3d52-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e3d52-118">**Type**</span></span>|<span data-ttu-id="e3d52-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3d52-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e3d52-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="e3d52-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e3d52-121">LineTo_Type</span><span class="sxs-lookup"><span data-stu-id="e3d52-121">LineTo_Type</span></span>](lineto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e3d52-122">直線セグメントの最後の頂点に対する x 座標または y 座標を格納します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-122">Contains x-or y-coordinates of the ending vertex of a straight line segment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e3d52-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e3d52-123">Child elements</span></span>

|<span data-ttu-id="e3d52-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3d52-124">**Element**</span></span>|<span data-ttu-id="e3d52-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e3d52-125">**Type**</span></span>|<span data-ttu-id="e3d52-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3d52-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e3d52-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e3d52-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e3d52-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e3d52-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e3d52-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e3d52-130">属性</span><span class="sxs-lookup"><span data-stu-id="e3d52-130">Attributes</span></span>

|<span data-ttu-id="e3d52-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="e3d52-131">**Attribute**</span></span>|<span data-ttu-id="e3d52-132">**型**</span><span class="sxs-lookup"><span data-stu-id="e3d52-132">**Type**</span></span>|<span data-ttu-id="e3d52-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="e3d52-133">**Required**</span></span>|<span data-ttu-id="e3d52-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3d52-134">**Description**</span></span>|<span data-ttu-id="e3d52-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e3d52-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e3d52-136">E</span><span class="sxs-lookup"><span data-stu-id="e3d52-136">E</span></span>  <br/> |<span data-ttu-id="e3d52-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e3d52-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e3d52-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="e3d52-138">optional</span></span>  <br/> |<span data-ttu-id="e3d52-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e3d52-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="e3d52-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e3d52-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="e3d52-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e3d52-142">F</span><span class="sxs-lookup"><span data-stu-id="e3d52-142">F</span></span>  <br/> |<span data-ttu-id="e3d52-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e3d52-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e3d52-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="e3d52-144">optional</span></span>  <br/> | <span data-ttu-id="e3d52-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-145">Represents the element's formula.</span></span> <span data-ttu-id="e3d52-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e3d52-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e3d52-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="e3d52-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e3d52-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="e3d52-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e3d52-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="e3d52-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e3d52-150">数式。</span><span class="sxs-lookup"><span data-stu-id="e3d52-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e3d52-151">N</span><span class="sxs-lookup"><span data-stu-id="e3d52-151">N</span></span>  <br/> |<span data-ttu-id="e3d52-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e3d52-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e3d52-153">必須</span><span class="sxs-lookup"><span data-stu-id="e3d52-153">required</span></span>  <br/> |<span data-ttu-id="e3d52-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e3d52-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e3d52-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3d52-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e3d52-157">U</span><span class="sxs-lookup"><span data-stu-id="e3d52-157">U</span></span>  <br/> |<span data-ttu-id="e3d52-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e3d52-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e3d52-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="e3d52-159">optional</span></span>  <br/> |<span data-ttu-id="e3d52-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e3d52-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e3d52-162">V</span><span class="sxs-lookup"><span data-stu-id="e3d52-162">V</span></span>  <br/> |<span data-ttu-id="e3d52-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="e3d52-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e3d52-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="e3d52-164">optional</span></span>  <br/> |<span data-ttu-id="e3d52-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e3d52-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3d52-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3d52-167">解説</span><span class="sxs-lookup"><span data-stu-id="e3d52-167">Remarks</span></span>

<span data-ttu-id="e3d52-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3d52-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e3d52-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3d52-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e3d52-170">**値**</span><span class="sxs-lookup"><span data-stu-id="e3d52-170">**Value**</span></span>|<span data-ttu-id="e3d52-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3d52-171">**Description**</span></span>|<span data-ttu-id="e3d52-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="e3d52-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3d52-173">X</span><span class="sxs-lookup"><span data-stu-id="e3d52-173">X</span></span>  <br/> |<span data-ttu-id="e3d52-174">直線セグメントの最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="e3d52-174">The x-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |<span data-ttu-id="e3d52-175">[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e3d52-175">[LineTo Row (Geometry Section)](lineto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="e3d52-176">Y</span><span class="sxs-lookup"><span data-stu-id="e3d52-176">Y</span></span>  <br/> |<span data-ttu-id="e3d52-177">直線セグメントの最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="e3d52-177">The y-coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |<span data-ttu-id="e3d52-178">[[LineTo] 行 ([Geometry] セクション)](lineto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e3d52-178">[LineTo Row (Geometry Section)](lineto-row-geometry-section.md)</span></span> <br/> |
   

