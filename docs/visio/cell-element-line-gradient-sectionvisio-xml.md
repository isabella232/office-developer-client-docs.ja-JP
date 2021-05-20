---
title: Cell 要素 ([線のグラデーション] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: 線のグラデーションについて、グラデーションの分岐点の色、透過性、または位置を格納します。
ms.openlocfilehash: d8ac664285d24e47a142c22b1483e2ff435aef48
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539503"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a><span data-ttu-id="5ddcb-103">Cell 要素 ([線のグラデーション] セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5ddcb-103">Cell element (Line Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="5ddcb-104">線のグラデーションについて、グラデーションの分岐点の色、透過性、または位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-104">Contains the color, transparency, or position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ddcb-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="5ddcb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ddcb-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5ddcb-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="5ddcb-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5ddcb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5ddcb-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5ddcb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5ddcb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5ddcb-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5ddcb-112">document.xml、master#.xml、page#.xml</span><span class="sxs-lookup"><span data-stu-id="5ddcb-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ddcb-113">定義</span><span class="sxs-lookup"><span data-stu-id="5ddcb-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5ddcb-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5ddcb-114">Elements and attributes</span></span>

<span data-ttu-id="5ddcb-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5ddcb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5ddcb-116">Parent elements</span></span>

|<span data-ttu-id="5ddcb-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-117">**Element**</span></span>|<span data-ttu-id="5ddcb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-118">**Type**</span></span>|<span data-ttu-id="5ddcb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ddcb-120">[Row 要素 ([線のグラデーション] セクション)](row-element-line-gradient-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="5ddcb-120">[Row element (Line Gradient Section)](row-element-line-gradient-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="5ddcb-121">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="5ddcb-121">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ddcb-122">線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ddcb-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5ddcb-123">Child elements</span></span>

|<span data-ttu-id="5ddcb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-124">**Element**</span></span>|<span data-ttu-id="5ddcb-125">**型**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-125">**Type**</span></span>|<span data-ttu-id="5ddcb-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ddcb-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="5ddcb-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5ddcb-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="5ddcb-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ddcb-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5ddcb-130">属性</span><span class="sxs-lookup"><span data-stu-id="5ddcb-130">Attributes</span></span>

|<span data-ttu-id="5ddcb-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-131">**Attribute**</span></span>|<span data-ttu-id="5ddcb-132">**型**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-132">**Type**</span></span>|<span data-ttu-id="5ddcb-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-133">**Required**</span></span>|<span data-ttu-id="5ddcb-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-134">**Description**</span></span>|<span data-ttu-id="5ddcb-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5ddcb-136">E</span><span class="sxs-lookup"><span data-stu-id="5ddcb-136">E</span></span>  <br/> |<span data-ttu-id="5ddcb-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ddcb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcb-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="5ddcb-138">optional</span></span>  <br/> |<span data-ttu-id="5ddcb-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="5ddcb-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="5ddcb-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="5ddcb-142">F</span><span class="sxs-lookup"><span data-stu-id="5ddcb-142">F</span></span>  <br/> |<span data-ttu-id="5ddcb-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ddcb-143">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcb-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="5ddcb-144">optional</span></span>  <br/> | <span data-ttu-id="5ddcb-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-145">Represents the element's formula.</span></span> <span data-ttu-id="5ddcb-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="5ddcb-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="5ddcb-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="5ddcb-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="5ddcb-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="5ddcb-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="5ddcb-150">数式。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="5ddcb-151">N</span><span class="sxs-lookup"><span data-stu-id="5ddcb-151">N</span></span>  <br/> |<span data-ttu-id="5ddcb-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ddcb-152">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcb-153">必須</span><span class="sxs-lookup"><span data-stu-id="5ddcb-153">required</span></span>  <br/> |<span data-ttu-id="5ddcb-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="5ddcb-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="5ddcb-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="5ddcb-157">U</span><span class="sxs-lookup"><span data-stu-id="5ddcb-157">U</span></span>  <br/> |<span data-ttu-id="5ddcb-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ddcb-158">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcb-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="5ddcb-159">optional</span></span>  <br/> |<span data-ttu-id="5ddcb-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="5ddcb-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="5ddcb-162">V</span><span class="sxs-lookup"><span data-stu-id="5ddcb-162">V</span></span>  <br/> |<span data-ttu-id="5ddcb-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="5ddcb-163">xsd:string</span></span>  <br/> |<span data-ttu-id="5ddcb-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="5ddcb-164">optional</span></span>  <br/> |<span data-ttu-id="5ddcb-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="5ddcb-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ddcb-167">注釈</span><span class="sxs-lookup"><span data-stu-id="5ddcb-167">Remarks</span></span>

<span data-ttu-id="5ddcb-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="5ddcb-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="5ddcb-170">**値**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-170">**Value**</span></span>|<span data-ttu-id="5ddcb-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-171">**Description**</span></span>|<span data-ttu-id="5ddcb-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="5ddcb-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ddcb-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="5ddcb-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="5ddcb-174">グラデーションの分岐点の色の値。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-174">The color value of the gradient stop.</span></span>  <br/> |<span data-ttu-id="5ddcb-175">[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="5ddcb-175">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="5ddcb-176">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="5ddcb-176">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="5ddcb-177">グラデーションの停止色の透明度をパーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-177">The amount of transparency of the gradient stop color, as a percentage.</span></span>  <br/> |<span data-ttu-id="5ddcb-178">[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="5ddcb-178">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="5ddcb-179">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="5ddcb-179">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="5ddcb-180">グラデーションの位置は、グラデーションの原点からグラデーションの外側の端へのパーセンテージで、線のグラデーションの方向に沿って停止します。</span><span class="sxs-lookup"><span data-stu-id="5ddcb-180">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |<span data-ttu-id="5ddcb-181">[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="5ddcb-181">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
   

