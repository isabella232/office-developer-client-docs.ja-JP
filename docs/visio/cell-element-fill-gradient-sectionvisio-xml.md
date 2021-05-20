---
title: Cell 要素 (Fill Gradient Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: 塗りつぶしグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: 998c63d5273c39601e5b7293ae03eebbc3b467b2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539552"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="a732a-103">Cell 要素 (Fill Gradient Section) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a732a-103">Cell element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="a732a-104">塗りつぶしグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="a732a-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a732a-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a732a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a732a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a732a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a732a-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a732a-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a732a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a732a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a732a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a732a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a732a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a732a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a732a-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a732a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a732a-112">document.xml、master#.xml、page#.xml</span><span class="sxs-lookup"><span data-stu-id="a732a-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a732a-113">定義</span><span class="sxs-lookup"><span data-stu-id="a732a-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a732a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a732a-114">Elements and attributes</span></span>

<span data-ttu-id="a732a-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a732a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a732a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a732a-116">Parent elements</span></span>

|<span data-ttu-id="a732a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a732a-117">**Element**</span></span>|<span data-ttu-id="a732a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a732a-118">**Type**</span></span>|<span data-ttu-id="a732a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a732a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a732a-120">Row 要素 (FillGradient セクション)</span><span class="sxs-lookup"><span data-stu-id="a732a-120">Row element (FillGradient Section)</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a732a-121">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="a732a-121">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a732a-122">塗りつぶしグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="a732a-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a732a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a732a-123">Child elements</span></span>

|<span data-ttu-id="a732a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a732a-124">**Element**</span></span>|<span data-ttu-id="a732a-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a732a-125">**Type**</span></span>|<span data-ttu-id="a732a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a732a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a732a-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="a732a-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a732a-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="a732a-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a732a-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="a732a-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a732a-130">属性</span><span class="sxs-lookup"><span data-stu-id="a732a-130">Attributes</span></span>

|<span data-ttu-id="a732a-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a732a-131">**Attribute**</span></span>|<span data-ttu-id="a732a-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a732a-132">**Type**</span></span>|<span data-ttu-id="a732a-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a732a-133">**Required**</span></span>|<span data-ttu-id="a732a-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a732a-134">**Description**</span></span>|<span data-ttu-id="a732a-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a732a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a732a-136">E</span><span class="sxs-lookup"><span data-stu-id="a732a-136">E</span></span>  <br/> |<span data-ttu-id="a732a-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a732a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a732a-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a732a-138">optional</span></span>  <br/> |<span data-ttu-id="a732a-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a732a-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="a732a-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="a732a-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="a732a-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="a732a-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="a732a-142">F</span><span class="sxs-lookup"><span data-stu-id="a732a-142">F</span></span>  <br/> |<span data-ttu-id="a732a-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a732a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a732a-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="a732a-144">optional</span></span>  <br/> | <span data-ttu-id="a732a-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="a732a-145">Represents the element's formula.</span></span> <span data-ttu-id="a732a-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="a732a-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="a732a-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="a732a-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="a732a-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="a732a-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="a732a-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="a732a-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="a732a-150">数式。</span><span class="sxs-lookup"><span data-stu-id="a732a-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="a732a-151">N</span><span class="sxs-lookup"><span data-stu-id="a732a-151">N</span></span>  <br/> |<span data-ttu-id="a732a-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a732a-152">xsd:string</span></span>  <br/> |<span data-ttu-id="a732a-153">必須</span><span class="sxs-lookup"><span data-stu-id="a732a-153">required</span></span>  <br/> |<span data-ttu-id="a732a-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="a732a-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="a732a-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a732a-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="a732a-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a732a-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="a732a-157">U</span><span class="sxs-lookup"><span data-stu-id="a732a-157">U</span></span>  <br/> |<span data-ttu-id="a732a-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a732a-158">xsd:string</span></span>  <br/> |<span data-ttu-id="a732a-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="a732a-159">optional</span></span>  <br/> |<span data-ttu-id="a732a-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="a732a-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="a732a-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="a732a-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="a732a-162">V</span><span class="sxs-lookup"><span data-stu-id="a732a-162">V</span></span>  <br/> |<span data-ttu-id="a732a-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a732a-163">xsd:string</span></span>  <br/> |<span data-ttu-id="a732a-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="a732a-164">optional</span></span>  <br/> |<span data-ttu-id="a732a-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="a732a-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="a732a-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a732a-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a732a-167">注釈</span><span class="sxs-lookup"><span data-stu-id="a732a-167">Remarks</span></span>

<span data-ttu-id="a732a-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a732a-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="a732a-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="a732a-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="a732a-170">**値**</span><span class="sxs-lookup"><span data-stu-id="a732a-170">**Value**</span></span>|<span data-ttu-id="a732a-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="a732a-171">**Description**</span></span>|<span data-ttu-id="a732a-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="a732a-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a732a-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="a732a-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="a732a-174">グラデーションの分岐点の色の値。</span><span class="sxs-lookup"><span data-stu-id="a732a-174">The color value of the gradient stop.</span></span> <span data-ttu-id="a732a-175">この値は、ドキュメント パレット内の色のインデックス番号として、または **RGB、THEMEVAL、** または HSL 関数を **使用して表** されます。</span><span class="sxs-lookup"><span data-stu-id="a732a-175">This value can be expressed as the index number of a color in the document palette or by using the **RGB**, **THEMEVAL**, or **HSL** functions.</span></span>  <br/> |<span data-ttu-id="a732a-176">[[グラデーションの停止] 行 ([塗りつぶしのグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="a732a-176">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="a732a-177">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="a732a-177">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="a732a-178">グラデーションの色の透明度をパーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="a732a-178">The amount of transparency of the gradient color stop, as a percentage.</span></span>  <br/> |<span data-ttu-id="a732a-179">[[グラデーションの停止] 行 ([塗りつぶしのグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="a732a-179">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="a732a-180">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="a732a-180">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="a732a-181">グラデーションの位置は、グラデーションの原点からグラデーションの外側の端へのパーセンテージで、線のグラデーションの方向に沿って停止します。</span><span class="sxs-lookup"><span data-stu-id="a732a-181">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |<span data-ttu-id="a732a-182">[[グラデーションの停止] 行 ([塗りつぶしのグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="a732a-182">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
   

