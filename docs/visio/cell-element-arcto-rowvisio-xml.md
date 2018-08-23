---
title: セル要素 (ArcTo 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 69f1a0cc-90fe-4b49-653c-bba4a1a2b1b2
description: X を含む座標、y 座標、または円弧の弓。
ms.openlocfilehash: a51cf775f787a34aa8f5de6f6cf90ffc230f3500
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804943"
---
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="e431d-103">セル要素 (ArcTo 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e431d-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="e431d-104">X を含む座標、y 座標、または円弧の弓。</span><span class="sxs-lookup"><span data-stu-id="e431d-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e431d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e431d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e431d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e431d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e431d-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e431d-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e431d-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e431d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e431d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e431d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e431d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e431d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e431d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e431d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e431d-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="e431d-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e431d-113">定義</span><span class="sxs-lookup"><span data-stu-id="e431d-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e431d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e431d-114">Elements and attributes</span></span>

<span data-ttu-id="e431d-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e431d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e431d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e431d-116">Parent elements</span></span>

|<span data-ttu-id="e431d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e431d-117">**Element**</span></span>|<span data-ttu-id="e431d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e431d-118">**Type**</span></span>|<span data-ttu-id="e431d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e431d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e431d-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="e431d-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e431d-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="e431d-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e431d-122">円弧の x 座標と y 座標、および弧を格納します。</span><span class="sxs-lookup"><span data-stu-id="e431d-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e431d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e431d-123">Child elements</span></span>

|<span data-ttu-id="e431d-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="e431d-124">**Element**</span></span>|<span data-ttu-id="e431d-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e431d-125">**Type**</span></span>|<span data-ttu-id="e431d-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e431d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e431d-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e431d-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e431d-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e431d-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e431d-129">X を含む座標、y 座標、または円弧の弓。</span><span class="sxs-lookup"><span data-stu-id="e431d-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e431d-130">属性</span><span class="sxs-lookup"><span data-stu-id="e431d-130">Attributes</span></span>

|<span data-ttu-id="e431d-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="e431d-131">**Attribute**</span></span>|<span data-ttu-id="e431d-132">**型**</span><span class="sxs-lookup"><span data-stu-id="e431d-132">**Type**</span></span>|<span data-ttu-id="e431d-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="e431d-133">**Required**</span></span>|<span data-ttu-id="e431d-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="e431d-134">**Description**</span></span>|<span data-ttu-id="e431d-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="e431d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e431d-136">E</span><span class="sxs-lookup"><span data-stu-id="e431d-136">E</span></span>  <br/> |<span data-ttu-id="e431d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e431d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e431d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="e431d-138">optional</span></span>  <br/> |<span data-ttu-id="e431d-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="e431d-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e431d-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="e431d-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e431d-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="e431d-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e431d-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="e431d-142">F</span></span>  <br/> |<span data-ttu-id="e431d-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e431d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e431d-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="e431d-144">optional</span></span>  <br/> | <span data-ttu-id="e431d-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="e431d-145">Represents the element's formula.</span></span> <span data-ttu-id="e431d-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e431d-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e431d-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="e431d-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e431d-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="e431d-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e431d-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="e431d-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e431d-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="e431d-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e431d-151">N</span><span class="sxs-lookup"><span data-stu-id="e431d-151">N</span></span>  <br/> |<span data-ttu-id="e431d-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e431d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e431d-153">必須</span><span class="sxs-lookup"><span data-stu-id="e431d-153">required</span></span>  <br/> |<span data-ttu-id="e431d-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="e431d-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e431d-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="e431d-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e431d-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e431d-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e431d-157">U</span><span class="sxs-lookup"><span data-stu-id="e431d-157">U</span></span>  <br/> |<span data-ttu-id="e431d-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e431d-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e431d-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="e431d-159">optional</span></span>  <br/> |<span data-ttu-id="e431d-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="e431d-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e431d-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="e431d-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e431d-162">V</span><span class="sxs-lookup"><span data-stu-id="e431d-162">V</span></span>  <br/> |<span data-ttu-id="e431d-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e431d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e431d-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="e431d-164">optional</span></span>  <br/> |<span data-ttu-id="e431d-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="e431d-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e431d-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="e431d-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e431d-167">注釈</span><span class="sxs-lookup"><span data-stu-id="e431d-167">Remarks</span></span>

<span data-ttu-id="e431d-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e431d-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e431d-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e431d-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e431d-170">**値**</span><span class="sxs-lookup"><span data-stu-id="e431d-170">**Value**</span></span>|<span data-ttu-id="e431d-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="e431d-171">**Description**</span></span>|<span data-ttu-id="e431d-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="e431d-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e431d-173">A</span><span class="sxs-lookup"><span data-stu-id="e431d-173">A</span></span>  <br/> |<span data-ttu-id="e431d-174">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="e431d-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |<span data-ttu-id="e431d-175">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e431d-175">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="e431d-176">X</span><span class="sxs-lookup"><span data-stu-id="e431d-176">X</span></span>  <br/> |<span data-ttu-id="e431d-177">円弧の最後の頂点に対する x 座標です。</span><span class="sxs-lookup"><span data-stu-id="e431d-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="e431d-178">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e431d-178">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="e431d-179">Y</span><span class="sxs-lookup"><span data-stu-id="e431d-179">Y</span></span>  <br/> |<span data-ttu-id="e431d-180">円弧の最後の頂点に対する y 座標です。</span><span class="sxs-lookup"><span data-stu-id="e431d-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="e431d-181">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="e431d-181">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
   

