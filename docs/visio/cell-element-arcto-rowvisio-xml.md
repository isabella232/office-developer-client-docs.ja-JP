---
title: Cell 要素 (ArcTo 行) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: 円弧の x 座標、y 座標、または弧を格納します。
ms.openlocfilehash: 6d744366cda7db0f3950ed0962c7ba5bd01b8e36
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538824"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="fb728-103">Cell 要素 (ArcTo 行) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fb728-103">Cell element (ArcTo Row) (Visio XML)</span></span>

<span data-ttu-id="fb728-104">円弧の x 座標、y 座標、または弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="fb728-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb728-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="fb728-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb728-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="fb728-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fb728-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="fb728-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fb728-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb728-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fb728-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fb728-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fb728-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="fb728-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fb728-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="fb728-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fb728-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="fb728-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb728-113">定義</span><span class="sxs-lookup"><span data-stu-id="fb728-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fb728-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fb728-114">Elements and attributes</span></span>

<span data-ttu-id="fb728-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb728-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fb728-116">親要素</span><span class="sxs-lookup"><span data-stu-id="fb728-116">Parent elements</span></span>

|<span data-ttu-id="fb728-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="fb728-117">**Element**</span></span>|<span data-ttu-id="fb728-118">**型**</span><span class="sxs-lookup"><span data-stu-id="fb728-118">**Type**</span></span>|<span data-ttu-id="fb728-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="fb728-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb728-120">Row 要素 (Geometry)</span><span class="sxs-lookup"><span data-stu-id="fb728-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="fb728-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="fb728-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb728-122">円弧の x 座標と y 座標、および弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="fb728-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb728-123">子要素</span><span class="sxs-lookup"><span data-stu-id="fb728-123">Child elements</span></span>

|<span data-ttu-id="fb728-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="fb728-124">**Element**</span></span>|<span data-ttu-id="fb728-125">**型**</span><span class="sxs-lookup"><span data-stu-id="fb728-125">**Type**</span></span>|<span data-ttu-id="fb728-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="fb728-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb728-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="fb728-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb728-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="fb728-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb728-129">円弧の x 座標、y 座標、または弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="fb728-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fb728-130">属性</span><span class="sxs-lookup"><span data-stu-id="fb728-130">Attributes</span></span>

|<span data-ttu-id="fb728-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="fb728-131">**Attribute**</span></span>|<span data-ttu-id="fb728-132">**型**</span><span class="sxs-lookup"><span data-stu-id="fb728-132">**Type**</span></span>|<span data-ttu-id="fb728-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="fb728-133">**Required**</span></span>|<span data-ttu-id="fb728-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="fb728-134">**Description**</span></span>|<span data-ttu-id="fb728-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fb728-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb728-136">E</span><span class="sxs-lookup"><span data-stu-id="fb728-136">E</span></span>  <br/> |<span data-ttu-id="fb728-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb728-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fb728-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb728-138">optional</span></span>  <br/> |<span data-ttu-id="fb728-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="fb728-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="fb728-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="fb728-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="fb728-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="fb728-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="fb728-142">F</span><span class="sxs-lookup"><span data-stu-id="fb728-142">F</span></span>  <br/> |<span data-ttu-id="fb728-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb728-143">xsd:string</span></span>  <br/> |<span data-ttu-id="fb728-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb728-144">optional</span></span>  <br/> | <span data-ttu-id="fb728-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="fb728-145">Represents the element's formula.</span></span> <span data-ttu-id="fb728-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fb728-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="fb728-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="fb728-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="fb728-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="fb728-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="fb728-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="fb728-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="fb728-150">数式。</span><span class="sxs-lookup"><span data-stu-id="fb728-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="fb728-151">N</span><span class="sxs-lookup"><span data-stu-id="fb728-151">N</span></span>  <br/> |<span data-ttu-id="fb728-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb728-152">xsd:string</span></span>  <br/> |<span data-ttu-id="fb728-153">必須</span><span class="sxs-lookup"><span data-stu-id="fb728-153">required</span></span>  <br/> |<span data-ttu-id="fb728-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="fb728-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="fb728-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb728-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="fb728-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb728-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="fb728-157">U</span><span class="sxs-lookup"><span data-stu-id="fb728-157">U</span></span>  <br/> |<span data-ttu-id="fb728-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb728-158">xsd:string</span></span>  <br/> |<span data-ttu-id="fb728-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb728-159">optional</span></span>  <br/> |<span data-ttu-id="fb728-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="fb728-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="fb728-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="fb728-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="fb728-162">V</span><span class="sxs-lookup"><span data-stu-id="fb728-162">V</span></span>  <br/> |<span data-ttu-id="fb728-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb728-163">xsd:string</span></span>  <br/> |<span data-ttu-id="fb728-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb728-164">optional</span></span>  <br/> |<span data-ttu-id="fb728-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="fb728-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="fb728-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fb728-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb728-167">注釈</span><span class="sxs-lookup"><span data-stu-id="fb728-167">Remarks</span></span>

<span data-ttu-id="fb728-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb728-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="fb728-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb728-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="fb728-170">**値**</span><span class="sxs-lookup"><span data-stu-id="fb728-170">**Value**</span></span>|<span data-ttu-id="fb728-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="fb728-171">**Description**</span></span>|<span data-ttu-id="fb728-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="fb728-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb728-173">A</span><span class="sxs-lookup"><span data-stu-id="fb728-173">A</span></span>  <br/> |<span data-ttu-id="fb728-174">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="fb728-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |<span data-ttu-id="fb728-175">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fb728-175">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="fb728-176">X</span><span class="sxs-lookup"><span data-stu-id="fb728-176">X</span></span>  <br/> |<span data-ttu-id="fb728-177">円弧の最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="fb728-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="fb728-178">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fb728-178">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="fb728-179">Y</span><span class="sxs-lookup"><span data-stu-id="fb728-179">Y</span></span>  <br/> |<span data-ttu-id="fb728-180">円弧の最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="fb728-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="fb728-181">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="fb728-181">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
   

