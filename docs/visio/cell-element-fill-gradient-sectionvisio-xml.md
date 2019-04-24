---
title: Cell 要素 ([塗りつぶしグラデーション] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: 塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: 3c4cdf1f60f68748fd2500b2dec0b5a5ad553ff5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356099"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="4cf10-103">Cell 要素 ([塗りつぶしグラデーション] セクション) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="4cf10-103">Cell element (Fill Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="4cf10-104">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cf10-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4cf10-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cf10-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4cf10-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4cf10-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4cf10-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4cf10-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4cf10-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4cf10-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4cf10-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4cf10-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4cf10-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4cf10-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4cf10-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4cf10-112">文書 .xml、master # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="4cf10-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4cf10-113">定義</span><span class="sxs-lookup"><span data-stu-id="4cf10-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4cf10-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4cf10-114">Elements and attributes</span></span>

<span data-ttu-id="4cf10-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cf10-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4cf10-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4cf10-116">Parent elements</span></span>

|<span data-ttu-id="4cf10-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4cf10-117">**Element**</span></span>|<span data-ttu-id="4cf10-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4cf10-118">**Type**</span></span>|<span data-ttu-id="4cf10-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cf10-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4cf10-120">Row 要素 (fillgradient セクション)</span><span class="sxs-lookup"><span data-stu-id="4cf10-120">Row element (FillGradient Section)</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4cf10-121">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="4cf10-121">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4cf10-122">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4cf10-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4cf10-123">Child elements</span></span>

|<span data-ttu-id="4cf10-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cf10-124">**Element**</span></span>|<span data-ttu-id="4cf10-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4cf10-125">**Type**</span></span>|<span data-ttu-id="4cf10-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cf10-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4cf10-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="4cf10-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4cf10-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4cf10-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4cf10-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4cf10-130">属性</span><span class="sxs-lookup"><span data-stu-id="4cf10-130">Attributes</span></span>

|<span data-ttu-id="4cf10-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="4cf10-131">**Attribute**</span></span>|<span data-ttu-id="4cf10-132">**型**</span><span class="sxs-lookup"><span data-stu-id="4cf10-132">**Type**</span></span>|<span data-ttu-id="4cf10-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="4cf10-133">**Required**</span></span>|<span data-ttu-id="4cf10-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cf10-134">**Description**</span></span>|<span data-ttu-id="4cf10-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="4cf10-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4cf10-136">E</span><span class="sxs-lookup"><span data-stu-id="4cf10-136">E</span></span>  <br/> |<span data-ttu-id="4cf10-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4cf10-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4cf10-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cf10-138">optional</span></span>  <br/> |<span data-ttu-id="4cf10-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="4cf10-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="4cf10-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="4cf10-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="4cf10-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="4cf10-142">F</span><span class="sxs-lookup"><span data-stu-id="4cf10-142">F</span></span>  <br/> |<span data-ttu-id="4cf10-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4cf10-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4cf10-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cf10-144">optional</span></span>  <br/> | <span data-ttu-id="4cf10-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-145">Represents the element's formula.</span></span> <span data-ttu-id="4cf10-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4cf10-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="4cf10-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="4cf10-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="4cf10-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="4cf10-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="4cf10-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="4cf10-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="4cf10-150">数式。</span><span class="sxs-lookup"><span data-stu-id="4cf10-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="4cf10-151">N</span><span class="sxs-lookup"><span data-stu-id="4cf10-151">N</span></span>  <br/> |<span data-ttu-id="4cf10-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4cf10-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4cf10-153">必須</span><span class="sxs-lookup"><span data-stu-id="4cf10-153">required</span></span>  <br/> |<span data-ttu-id="4cf10-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="4cf10-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="4cf10-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cf10-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="4cf10-157">U</span><span class="sxs-lookup"><span data-stu-id="4cf10-157">U</span></span>  <br/> |<span data-ttu-id="4cf10-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4cf10-158">xsd:string</span></span>  <br/> |<span data-ttu-id="4cf10-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cf10-159">optional</span></span>  <br/> |<span data-ttu-id="4cf10-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="4cf10-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="4cf10-162">V</span><span class="sxs-lookup"><span data-stu-id="4cf10-162">V</span></span>  <br/> |<span data-ttu-id="4cf10-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="4cf10-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4cf10-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="4cf10-164">optional</span></span>  <br/> |<span data-ttu-id="4cf10-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="4cf10-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cf10-167">解説</span><span class="sxs-lookup"><span data-stu-id="4cf10-167">Remarks</span></span>

<span data-ttu-id="4cf10-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cf10-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="4cf10-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cf10-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="4cf10-170">**値**</span><span class="sxs-lookup"><span data-stu-id="4cf10-170">**Value**</span></span>|<span data-ttu-id="4cf10-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="4cf10-171">**Description**</span></span>|<span data-ttu-id="4cf10-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="4cf10-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4cf10-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="4cf10-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="4cf10-174">グラデーションの分岐点の色の値。</span><span class="sxs-lookup"><span data-stu-id="4cf10-174">The color value of the gradient stop.</span></span> <span data-ttu-id="4cf10-175">この値は、ドキュメントパレット内の色のインデックス番号、または**RGB**関数、または**HSL**関数\*\*\*\* を使用して表すことができます。</span><span class="sxs-lookup"><span data-stu-id="4cf10-175">This value can be expressed as the index number of a color in the document palette or by using the **RGB**, **THEMEVAL**, or **HSL** functions.</span></span>  <br/> |[<span data-ttu-id="4cf10-176">グラデーションの分岐点の行 (塗りつぶしのグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="4cf10-176">Gradient Stop Row (Fill Gradient Section)</span></span>](gradient-stop-row-fill-gradient-section.md) <br/> |
|<span data-ttu-id="4cf10-177">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="4cf10-177">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="4cf10-178">グラデーションの分岐点の透明度をパーセンテージで示します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-178">The amount of transparency of the gradient color stop, as a percentage.</span></span>  <br/> |[<span data-ttu-id="4cf10-179">グラデーションの分岐点の行 (塗りつぶしのグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="4cf10-179">Gradient Stop Row (Fill Gradient Section)</span></span>](gradient-stop-row-fill-gradient-section.md) <br/> |
|<span data-ttu-id="4cf10-180">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="4cf10-180">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="4cf10-181">線のグラデーションの方向に沿ったグラデーションの分岐点の位置を、グラデーションの原点からグラデーションの外側の端までのパーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="4cf10-181">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |[<span data-ttu-id="4cf10-182">グラデーションの分岐点の行 (塗りつぶしのグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="4cf10-182">Gradient Stop Row (Fill Gradient Section)</span></span>](gradient-stop-row-fill-gradient-section.md) <br/> |
   

