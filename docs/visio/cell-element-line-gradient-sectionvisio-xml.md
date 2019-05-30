---
title: Cell 要素 (線のグラデーションセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: 線のグラデーションのグラデーションの分岐点の色、透過性、または位置を含みます。
ms.openlocfilehash: d8ac664285d24e47a142c22b1483e2ff435aef48
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539503"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a><span data-ttu-id="a4477-103">Cell 要素 (線のグラデーションセクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a4477-103">Cell element (Line Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="a4477-104">線のグラデーションのグラデーションの分岐点の色、透過性、または位置を含みます。</span><span class="sxs-lookup"><span data-stu-id="a4477-104">Contains the color, transparency, or position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4477-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a4477-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4477-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a4477-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a4477-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a4477-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a4477-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a4477-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a4477-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a4477-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a4477-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="a4477-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a4477-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a4477-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a4477-112">文書 .xml、master # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="a4477-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4477-113">定義</span><span class="sxs-lookup"><span data-stu-id="a4477-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4477-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a4477-114">Elements and attributes</span></span>

<span data-ttu-id="a4477-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4477-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4477-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a4477-116">Parent elements</span></span>

|<span data-ttu-id="a4477-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a4477-117">**Element**</span></span>|<span data-ttu-id="a4477-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a4477-118">**Type**</span></span>|<span data-ttu-id="a4477-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4477-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4477-120">Row 要素 (線のグラデーションセクション)</span><span class="sxs-lookup"><span data-stu-id="a4477-120">Row element (Line Gradient Section)</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a4477-121">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="a4477-121">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4477-122">線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="a4477-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4477-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a4477-123">Child elements</span></span>

|<span data-ttu-id="a4477-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4477-124">**Element**</span></span>|<span data-ttu-id="a4477-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a4477-125">**Type**</span></span>|<span data-ttu-id="a4477-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4477-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4477-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="a4477-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a4477-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a4477-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4477-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4477-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a4477-130">属性</span><span class="sxs-lookup"><span data-stu-id="a4477-130">Attributes</span></span>

|<span data-ttu-id="a4477-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a4477-131">**Attribute**</span></span>|<span data-ttu-id="a4477-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a4477-132">**Type**</span></span>|<span data-ttu-id="a4477-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a4477-133">**Required**</span></span>|<span data-ttu-id="a4477-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4477-134">**Description**</span></span>|<span data-ttu-id="a4477-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a4477-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4477-136">E</span><span class="sxs-lookup"><span data-stu-id="a4477-136">E</span></span>  <br/> |<span data-ttu-id="a4477-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a4477-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a4477-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4477-138">optional</span></span>  <br/> |<span data-ttu-id="a4477-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="a4477-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a4477-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="a4477-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a4477-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="a4477-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a4477-142">F</span><span class="sxs-lookup"><span data-stu-id="a4477-142">F</span></span>  <br/> |<span data-ttu-id="a4477-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a4477-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a4477-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4477-144">optional</span></span>  <br/> | <span data-ttu-id="a4477-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="a4477-145">Represents the element's formula.</span></span> <span data-ttu-id="a4477-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a4477-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a4477-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="a4477-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a4477-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="a4477-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a4477-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="a4477-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a4477-150">数式。</span><span class="sxs-lookup"><span data-stu-id="a4477-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="a4477-151">N</span><span class="sxs-lookup"><span data-stu-id="a4477-151">N</span></span>  <br/> |<span data-ttu-id="a4477-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a4477-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a4477-153">必須</span><span class="sxs-lookup"><span data-stu-id="a4477-153">required</span></span>  <br/> |<span data-ttu-id="a4477-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="a4477-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a4477-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4477-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a4477-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4477-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a4477-157">U</span><span class="sxs-lookup"><span data-stu-id="a4477-157">U</span></span>  <br/> |<span data-ttu-id="a4477-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a4477-158">xsd:string</span></span>  <br/> |<span data-ttu-id="a4477-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4477-159">optional</span></span>  <br/> |<span data-ttu-id="a4477-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="a4477-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a4477-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="a4477-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a4477-162">V</span><span class="sxs-lookup"><span data-stu-id="a4477-162">V</span></span>  <br/> |<span data-ttu-id="a4477-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a4477-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a4477-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4477-164">optional</span></span>  <br/> |<span data-ttu-id="a4477-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="a4477-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a4477-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4477-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4477-167">注釈</span><span class="sxs-lookup"><span data-stu-id="a4477-167">Remarks</span></span>

<span data-ttu-id="a4477-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4477-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a4477-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4477-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a4477-170">**値**</span><span class="sxs-lookup"><span data-stu-id="a4477-170">**Value**</span></span>|<span data-ttu-id="a4477-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4477-171">**Description**</span></span>|<span data-ttu-id="a4477-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="a4477-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4477-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="a4477-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="a4477-174">グラデーションの分岐点の色の値。</span><span class="sxs-lookup"><span data-stu-id="a4477-174">The color value of the gradient stop.</span></span>  <br/> |[<span data-ttu-id="a4477-175">グラデーションの分岐点の行 (線のグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="a4477-175">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
|<span data-ttu-id="a4477-176">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="a4477-176">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="a4477-177">グラデーションの終了色の透明度をパーセンテージで示します。</span><span class="sxs-lookup"><span data-stu-id="a4477-177">The amount of transparency of the gradient stop color, as a percentage.</span></span>  <br/> |[<span data-ttu-id="a4477-178">グラデーションの分岐点の行 (線のグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="a4477-178">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
|<span data-ttu-id="a4477-179">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="a4477-179">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="a4477-180">線のグラデーションの方向に沿ったグラデーションの分岐点の位置を、グラデーションの原点からグラデーションの外側の端までのパーセントで指定します。</span><span class="sxs-lookup"><span data-stu-id="a4477-180">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |[<span data-ttu-id="a4477-181">グラデーションの分岐点の行 (線のグラデーションのセクション)</span><span class="sxs-lookup"><span data-stu-id="a4477-181">Gradient Stop Row (Line Gradient Section)</span></span>](gradient-stop-row-line-gradient-section.md) <br/> |
   

