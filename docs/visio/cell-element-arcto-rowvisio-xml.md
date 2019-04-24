---
title: Cell 要素 (arcto 行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: 円弧の x 座標、y 座標、または弧を格納します。
ms.openlocfilehash: 709251c40299425d59df97fc0c48901bb0204167
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356135"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="8b87f-103">Cell 要素 (arcto 行) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8b87f-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="8b87f-104">円弧の x 座標、y 座標、または弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b87f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8b87f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b87f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8b87f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8b87f-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8b87f-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8b87f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8b87f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8b87f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8b87f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8b87f-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8b87f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8b87f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8b87f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8b87f-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="8b87f-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b87f-113">定義</span><span class="sxs-lookup"><span data-stu-id="8b87f-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8b87f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8b87f-114">Elements and attributes</span></span>

<span data-ttu-id="8b87f-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b87f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8b87f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8b87f-116">Parent elements</span></span>

|<span data-ttu-id="8b87f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8b87f-117">**Element**</span></span>|<span data-ttu-id="8b87f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8b87f-118">**Type**</span></span>|<span data-ttu-id="8b87f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b87f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b87f-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="8b87f-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8b87f-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="8b87f-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8b87f-122">円弧の x 座標と y 座標、および弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b87f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8b87f-123">Child elements</span></span>

|<span data-ttu-id="8b87f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b87f-124">**Element**</span></span>|<span data-ttu-id="8b87f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8b87f-125">**Type**</span></span>|<span data-ttu-id="8b87f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b87f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b87f-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="8b87f-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8b87f-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="8b87f-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8b87f-129">円弧の x 座標、y 座標、または弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8b87f-130">属性</span><span class="sxs-lookup"><span data-stu-id="8b87f-130">Attributes</span></span>

|<span data-ttu-id="8b87f-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="8b87f-131">**Attribute**</span></span>|<span data-ttu-id="8b87f-132">**型**</span><span class="sxs-lookup"><span data-stu-id="8b87f-132">**Type**</span></span>|<span data-ttu-id="8b87f-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="8b87f-133">**Required**</span></span>|<span data-ttu-id="8b87f-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b87f-134">**Description**</span></span>|<span data-ttu-id="8b87f-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8b87f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8b87f-136">E</span><span class="sxs-lookup"><span data-stu-id="8b87f-136">E</span></span>  <br/> |<span data-ttu-id="8b87f-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8b87f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8b87f-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="8b87f-138">optional</span></span>  <br/> |<span data-ttu-id="8b87f-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="8b87f-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="8b87f-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="8b87f-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="8b87f-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="8b87f-142">F</span><span class="sxs-lookup"><span data-stu-id="8b87f-142">F</span></span>  <br/> |<span data-ttu-id="8b87f-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8b87f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="8b87f-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="8b87f-144">optional</span></span>  <br/> | <span data-ttu-id="8b87f-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-145">Represents the element's formula.</span></span> <span data-ttu-id="8b87f-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8b87f-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="8b87f-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="8b87f-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="8b87f-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="8b87f-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="8b87f-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="8b87f-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="8b87f-150">数式。</span><span class="sxs-lookup"><span data-stu-id="8b87f-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="8b87f-151">N</span><span class="sxs-lookup"><span data-stu-id="8b87f-151">N</span></span>  <br/> |<span data-ttu-id="8b87f-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8b87f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="8b87f-153">必須</span><span class="sxs-lookup"><span data-stu-id="8b87f-153">required</span></span>  <br/> |<span data-ttu-id="8b87f-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="8b87f-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="8b87f-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b87f-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="8b87f-157">U</span><span class="sxs-lookup"><span data-stu-id="8b87f-157">U</span></span>  <br/> |<span data-ttu-id="8b87f-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8b87f-158">xsd:string</span></span>  <br/> |<span data-ttu-id="8b87f-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="8b87f-159">optional</span></span>  <br/> |<span data-ttu-id="8b87f-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="8b87f-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="8b87f-162">V</span><span class="sxs-lookup"><span data-stu-id="8b87f-162">V</span></span>  <br/> |<span data-ttu-id="8b87f-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8b87f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="8b87f-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="8b87f-164">optional</span></span>  <br/> |<span data-ttu-id="8b87f-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="8b87f-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8b87f-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b87f-167">解説</span><span class="sxs-lookup"><span data-stu-id="8b87f-167">Remarks</span></span>

<span data-ttu-id="8b87f-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b87f-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="8b87f-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b87f-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="8b87f-170">**値**</span><span class="sxs-lookup"><span data-stu-id="8b87f-170">**Value**</span></span>|<span data-ttu-id="8b87f-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b87f-171">**Description**</span></span>|<span data-ttu-id="8b87f-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="8b87f-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b87f-173">A</span><span class="sxs-lookup"><span data-stu-id="8b87f-173">A</span></span>  <br/> |<span data-ttu-id="8b87f-174">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="8b87f-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |<span data-ttu-id="8b87f-175">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8b87f-175">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="8b87f-176">X</span><span class="sxs-lookup"><span data-stu-id="8b87f-176">X</span></span>  <br/> |<span data-ttu-id="8b87f-177">円弧の最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="8b87f-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="8b87f-178">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8b87f-178">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="8b87f-179">Y</span><span class="sxs-lookup"><span data-stu-id="8b87f-179">Y</span></span>  <br/> |<span data-ttu-id="8b87f-180">円弧の最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="8b87f-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="8b87f-181">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="8b87f-181">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
   

