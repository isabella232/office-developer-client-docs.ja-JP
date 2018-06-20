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
# <a name="cell-element-arcto-row-visio-xml"></a><span data-ttu-id="1b2c3-103">セル要素 (ArcTo 行) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="1b2c3-103">Cell element (ArcTo Row) ('Visio XML')</span></span>

<span data-ttu-id="1b2c3-104">X を含む座標、y 座標、または円弧の弓。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-104">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b2c3-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1b2c3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b2c3-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1b2c3-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1b2c3-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1b2c3-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1b2c3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1b2c3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1b2c3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1b2c3-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1b2c3-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="1b2c3-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b2c3-113">定義</span><span class="sxs-lookup"><span data-stu-id="1b2c3-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b2c3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b2c3-114">Elements and attributes</span></span>

<span data-ttu-id="1b2c3-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b2c3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1b2c3-116">Parent elements</span></span>

|<span data-ttu-id="1b2c3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-117">**Element**</span></span>|<span data-ttu-id="1b2c3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-118">**Type**</span></span>|<span data-ttu-id="1b2c3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b2c3-120">行要素 (ジオメトリ)</span><span class="sxs-lookup"><span data-stu-id="1b2c3-120">Row element (Geometry)</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1b2c3-121">ArcTo_Type</span><span class="sxs-lookup"><span data-stu-id="1b2c3-121">ArcTo_Type</span></span>](arcto_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b2c3-122">X 座標と y 座標、円弧の弓が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-122">Contains the x- and y-coordinates and bow of a circular arc.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b2c3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1b2c3-123">Child elements</span></span>

|<span data-ttu-id="1b2c3-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-124">**Element**</span></span>|<span data-ttu-id="1b2c3-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-125">**Type**</span></span>|<span data-ttu-id="1b2c3-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b2c3-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="1b2c3-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b2c3-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="1b2c3-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b2c3-129">X を含む座標、y 座標、または円弧の弓。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-129">Contains the x coordinate, y coordinate, or bow of a circular arc.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1b2c3-130">属性</span><span class="sxs-lookup"><span data-stu-id="1b2c3-130">Attributes</span></span>

|<span data-ttu-id="1b2c3-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-131">**Attribute**</span></span>|<span data-ttu-id="1b2c3-132">**型**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-132">**Type**</span></span>|<span data-ttu-id="1b2c3-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-133">**Required**</span></span>|<span data-ttu-id="1b2c3-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-134">**Description**</span></span>|<span data-ttu-id="1b2c3-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b2c3-136">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="1b2c3-136">E</span></span>  <br/> |<span data-ttu-id="1b2c3-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b2c3-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1b2c3-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b2c3-138">optional</span></span>  <br/> |<span data-ttu-id="1b2c3-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="1b2c3-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="1b2c3-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="1b2c3-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="1b2c3-142">F</span></span>  <br/> |<span data-ttu-id="1b2c3-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b2c3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1b2c3-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b2c3-144">optional</span></span>  <br/> | <span data-ttu-id="1b2c3-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-145">Represents the element's formula.</span></span> <span data-ttu-id="1b2c3-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="1b2c3-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="1b2c3-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="1b2c3-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="1b2c3-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="1b2c3-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="1b2c3-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="1b2c3-151">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="1b2c3-151">N</span></span>  <br/> |<span data-ttu-id="1b2c3-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b2c3-152">xsd:string</span></span>  <br/> |<span data-ttu-id="1b2c3-153">必須</span><span class="sxs-lookup"><span data-stu-id="1b2c3-153">required</span></span>  <br/> |<span data-ttu-id="1b2c3-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="1b2c3-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="1b2c3-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="1b2c3-157">U</span><span class="sxs-lookup"><span data-stu-id="1b2c3-157">U</span></span>  <br/> |<span data-ttu-id="1b2c3-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b2c3-158">xsd:string</span></span>  <br/> |<span data-ttu-id="1b2c3-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b2c3-159">optional</span></span>  <br/> |<span data-ttu-id="1b2c3-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="1b2c3-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="1b2c3-162">V</span><span class="sxs-lookup"><span data-stu-id="1b2c3-162">V</span></span>  <br/> |<span data-ttu-id="1b2c3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1b2c3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1b2c3-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b2c3-164">optional</span></span>  <br/> |<span data-ttu-id="1b2c3-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="1b2c3-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b2c3-167">備考</span><span class="sxs-lookup"><span data-stu-id="1b2c3-167">Remarks</span></span>

<span data-ttu-id="1b2c3-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="1b2c3-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="1b2c3-170">**値**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-170">**Value**</span></span>|<span data-ttu-id="1b2c3-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-171">**Description**</span></span>|<span data-ttu-id="1b2c3-172">**詳細については**</span><span class="sxs-lookup"><span data-stu-id="1b2c3-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b2c3-173">A</span><span class="sxs-lookup"><span data-stu-id="1b2c3-173">A</span></span>  <br/> |<span data-ttu-id="1b2c3-174">円弧の中点から弦の中点までの距離です。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-174">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |<span data-ttu-id="1b2c3-175">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="1b2c3-175">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="1b2c3-176">X</span><span class="sxs-lookup"><span data-stu-id="1b2c3-176">X</span></span>  <br/> |<span data-ttu-id="1b2c3-177">円弧の終点の x 座標。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-177">The x-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="1b2c3-178">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="1b2c3-178">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
|<span data-ttu-id="1b2c3-179">Y</span><span class="sxs-lookup"><span data-stu-id="1b2c3-179">Y</span></span>  <br/> |<span data-ttu-id="1b2c3-180">円弧の終点の y 座標。</span><span class="sxs-lookup"><span data-stu-id="1b2c3-180">The y-coordinate of the ending vertex of an arc.</span></span>  <br/> |<span data-ttu-id="1b2c3-181">[[ArcTo] 行 ([Geometry] セクション)](arcto-row-geometry-section.md)</span><span class="sxs-lookup"><span data-stu-id="1b2c3-181">[ArcTo Row (Geometry Section)](arcto-row-geometry-section.md)</span></span> <br/> |
   

