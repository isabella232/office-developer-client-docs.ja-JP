---
title: セル要素 (塗りつぶしグラデーション]) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d085f83a-f77b-9bf9-07dc-4561b83e288c
description: 塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: 3c4cdf1f60f68748fd2500b2dec0b5a5ad553ff5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386356"
---
# <a name="cell-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="9759d-103">セル要素 (塗りつぶしグラデーション]) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9759d-103">Cell element (Fill Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="9759d-104">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="9759d-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9759d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9759d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9759d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9759d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9759d-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9759d-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9759d-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9759d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9759d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9759d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9759d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9759d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9759d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9759d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9759d-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="9759d-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9759d-113">定義</span><span class="sxs-lookup"><span data-stu-id="9759d-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9759d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9759d-114">Elements and attributes</span></span>

<span data-ttu-id="9759d-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9759d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9759d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9759d-116">Parent elements</span></span>

|<span data-ttu-id="9759d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9759d-117">**Element**</span></span>|<span data-ttu-id="9759d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9759d-118">**Type**</span></span>|<span data-ttu-id="9759d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9759d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9759d-120">[行要素 ([FillGradient] セクション)](row-element-fill-gradient-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="9759d-120">[Row element (FillGradient Section)](row-element-fill-gradient-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="9759d-121">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="9759d-121">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9759d-122">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="9759d-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9759d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9759d-123">Child elements</span></span>

|<span data-ttu-id="9759d-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="9759d-124">**Element**</span></span>|<span data-ttu-id="9759d-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9759d-125">**Type**</span></span>|<span data-ttu-id="9759d-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9759d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9759d-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="9759d-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9759d-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9759d-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9759d-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="9759d-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9759d-130">属性</span><span class="sxs-lookup"><span data-stu-id="9759d-130">Attributes</span></span>

|<span data-ttu-id="9759d-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="9759d-131">**Attribute**</span></span>|<span data-ttu-id="9759d-132">**型**</span><span class="sxs-lookup"><span data-stu-id="9759d-132">**Type**</span></span>|<span data-ttu-id="9759d-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="9759d-133">**Required**</span></span>|<span data-ttu-id="9759d-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="9759d-134">**Description**</span></span>|<span data-ttu-id="9759d-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9759d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9759d-136">E</span><span class="sxs-lookup"><span data-stu-id="9759d-136">E</span></span>  <br/> |<span data-ttu-id="9759d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9759d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9759d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="9759d-138">optional</span></span>  <br/> |<span data-ttu-id="9759d-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="9759d-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="9759d-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="9759d-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="9759d-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="9759d-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="9759d-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="9759d-142">F</span></span>  <br/> |<span data-ttu-id="9759d-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9759d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="9759d-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="9759d-144">optional</span></span>  <br/> | <span data-ttu-id="9759d-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="9759d-145">Represents the element's formula.</span></span> <span data-ttu-id="9759d-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9759d-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="9759d-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="9759d-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="9759d-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="9759d-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="9759d-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="9759d-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="9759d-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="9759d-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="9759d-151">N</span><span class="sxs-lookup"><span data-stu-id="9759d-151">N</span></span>  <br/> |<span data-ttu-id="9759d-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9759d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="9759d-153">必須</span><span class="sxs-lookup"><span data-stu-id="9759d-153">required</span></span>  <br/> |<span data-ttu-id="9759d-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="9759d-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="9759d-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="9759d-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="9759d-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9759d-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="9759d-157">U</span><span class="sxs-lookup"><span data-stu-id="9759d-157">U</span></span>  <br/> |<span data-ttu-id="9759d-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9759d-158">xsd:string</span></span>  <br/> |<span data-ttu-id="9759d-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="9759d-159">optional</span></span>  <br/> |<span data-ttu-id="9759d-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="9759d-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="9759d-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="9759d-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="9759d-162">V</span><span class="sxs-lookup"><span data-stu-id="9759d-162">V</span></span>  <br/> |<span data-ttu-id="9759d-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9759d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9759d-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="9759d-164">optional</span></span>  <br/> |<span data-ttu-id="9759d-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="9759d-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="9759d-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="9759d-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9759d-167">備考</span><span class="sxs-lookup"><span data-stu-id="9759d-167">Remarks</span></span>

<span data-ttu-id="9759d-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9759d-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="9759d-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9759d-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="9759d-170">**値**</span><span class="sxs-lookup"><span data-stu-id="9759d-170">**Value**</span></span>|<span data-ttu-id="9759d-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="9759d-171">**Description**</span></span>|<span data-ttu-id="9759d-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="9759d-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9759d-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="9759d-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="9759d-174">グラデーション終了位置のカラー値です。</span><span class="sxs-lookup"><span data-stu-id="9759d-174">The color value of the gradient stop.</span></span> <span data-ttu-id="9759d-175">または**RGB**、 **THEMEVAL**、または**HSL**関数を使用してドキュメント パレットの色のインデックス番号としては、この値を表現できます。</span><span class="sxs-lookup"><span data-stu-id="9759d-175">This value can be expressed as the index number of a color in the document palette or by using the **RGB**, **THEMEVAL**, or **HSL** functions.</span></span>  <br/> |<span data-ttu-id="9759d-176">[[Gradient Stop] 行 ([塗りつぶしグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="9759d-176">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="9759d-177">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="9759d-177">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="9759d-178">色のグラデーションの分岐点の透明度をパーセントでの金額です。</span><span class="sxs-lookup"><span data-stu-id="9759d-178">The amount of transparency of the gradient color stop, as a percentage.</span></span>  <br/> |<span data-ttu-id="9759d-179">[[Gradient Stop] 行 ([塗りつぶしグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="9759d-179">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="9759d-180">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="9759d-180">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="9759d-181">線のグラデーションの方向、パーセンテージの原点からグラデーションのグラデーションの外側のエッジに沿ったグラデーションの分岐点の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="9759d-181">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |<span data-ttu-id="9759d-182">[[Gradient Stop] 行 ([塗りつぶしのグラデーション] セクション)](gradient-stop-row-fill-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="9759d-182">[Gradient Stop Row (Fill Gradient Section)](gradient-stop-row-fill-gradient-section.md)</span></span> <br/> |
   

