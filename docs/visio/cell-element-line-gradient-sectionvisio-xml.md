---
title: セル要素 (ライン グラデーション」のセクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: 色や透明度、線のグラデーションのグラデーション ストップの位置が含まれています。
ms.openlocfilehash: 915341b41849aae2af2285b49f0421798a16cf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392194"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a><span data-ttu-id="256e3-103">セル要素 (ライン グラデーション」のセクション)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="256e3-103">Cell element (Line Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="256e3-104">色や透明度、線のグラデーションのグラデーション ストップの位置が含まれています。</span><span class="sxs-lookup"><span data-stu-id="256e3-104">Contains the color, transparency, or position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="256e3-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="256e3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="256e3-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="256e3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="256e3-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="256e3-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="256e3-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="256e3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="256e3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="256e3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="256e3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="256e3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="256e3-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="256e3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="256e3-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="256e3-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="256e3-113">定義</span><span class="sxs-lookup"><span data-stu-id="256e3-113">Definition</span></span>

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="256e3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="256e3-114">Elements and attributes</span></span>

<span data-ttu-id="256e3-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="256e3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="256e3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="256e3-116">Parent elements</span></span>

|<span data-ttu-id="256e3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="256e3-117">**Element**</span></span>|<span data-ttu-id="256e3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="256e3-118">**Type**</span></span>|<span data-ttu-id="256e3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="256e3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="256e3-120">[Row 要素 ([線のグラデーション] セクション)](row-element-line-gradient-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="256e3-120">[Row element (Line Gradient Section)](row-element-line-gradient-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="256e3-121">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="256e3-121">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="256e3-122">線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="256e3-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="256e3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="256e3-123">Child elements</span></span>

|<span data-ttu-id="256e3-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="256e3-124">**Element**</span></span>|<span data-ttu-id="256e3-125">**型**</span><span class="sxs-lookup"><span data-stu-id="256e3-125">**Type**</span></span>|<span data-ttu-id="256e3-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="256e3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="256e3-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="256e3-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="256e3-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="256e3-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="256e3-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="256e3-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="256e3-130">属性</span><span class="sxs-lookup"><span data-stu-id="256e3-130">Attributes</span></span>

|<span data-ttu-id="256e3-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="256e3-131">**Attribute**</span></span>|<span data-ttu-id="256e3-132">**型**</span><span class="sxs-lookup"><span data-stu-id="256e3-132">**Type**</span></span>|<span data-ttu-id="256e3-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="256e3-133">**Required**</span></span>|<span data-ttu-id="256e3-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="256e3-134">**Description**</span></span>|<span data-ttu-id="256e3-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="256e3-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="256e3-136">E</span><span class="sxs-lookup"><span data-stu-id="256e3-136">E</span></span>  <br/> |<span data-ttu-id="256e3-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="256e3-137">xsd:string</span></span>  <br/> |<span data-ttu-id="256e3-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="256e3-138">optional</span></span>  <br/> |<span data-ttu-id="256e3-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="256e3-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="256e3-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="256e3-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="256e3-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="256e3-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="256e3-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="256e3-142">F</span></span>  <br/> |<span data-ttu-id="256e3-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="256e3-143">xsd:string</span></span>  <br/> |<span data-ttu-id="256e3-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="256e3-144">optional</span></span>  <br/> | <span data-ttu-id="256e3-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="256e3-145">Represents the element's formula.</span></span> <span data-ttu-id="256e3-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="256e3-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="256e3-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="256e3-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="256e3-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="256e3-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="256e3-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="256e3-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="256e3-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="256e3-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="256e3-151">N</span><span class="sxs-lookup"><span data-stu-id="256e3-151">N</span></span>  <br/> |<span data-ttu-id="256e3-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="256e3-152">xsd:string</span></span>  <br/> |<span data-ttu-id="256e3-153">必須</span><span class="sxs-lookup"><span data-stu-id="256e3-153">required</span></span>  <br/> |<span data-ttu-id="256e3-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="256e3-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="256e3-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="256e3-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="256e3-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="256e3-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="256e3-157">U</span><span class="sxs-lookup"><span data-stu-id="256e3-157">U</span></span>  <br/> |<span data-ttu-id="256e3-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="256e3-158">xsd:string</span></span>  <br/> |<span data-ttu-id="256e3-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="256e3-159">optional</span></span>  <br/> |<span data-ttu-id="256e3-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="256e3-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="256e3-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="256e3-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="256e3-162">V</span><span class="sxs-lookup"><span data-stu-id="256e3-162">V</span></span>  <br/> |<span data-ttu-id="256e3-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="256e3-163">xsd:string</span></span>  <br/> |<span data-ttu-id="256e3-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="256e3-164">optional</span></span>  <br/> |<span data-ttu-id="256e3-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="256e3-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="256e3-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="256e3-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="256e3-167">備考</span><span class="sxs-lookup"><span data-stu-id="256e3-167">Remarks</span></span>

<span data-ttu-id="256e3-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="256e3-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="256e3-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="256e3-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="256e3-170">**値**</span><span class="sxs-lookup"><span data-stu-id="256e3-170">**Value**</span></span>|<span data-ttu-id="256e3-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="256e3-171">**Description**</span></span>|<span data-ttu-id="256e3-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="256e3-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="256e3-173">GradientStopColor</span><span class="sxs-lookup"><span data-stu-id="256e3-173">GradientStopColor</span></span>  <br/> |<span data-ttu-id="256e3-174">グラデーション終了位置のカラー値です。</span><span class="sxs-lookup"><span data-stu-id="256e3-174">The color value of the gradient stop.</span></span>  <br/> |<span data-ttu-id="256e3-175">[[Gradient Stop] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="256e3-175">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="256e3-176">GradientStopColorTrans</span><span class="sxs-lookup"><span data-stu-id="256e3-176">GradientStopColorTrans</span></span>  <br/> |<span data-ttu-id="256e3-177">グラデーションの透明部分の量は、割合としての色を停止します。</span><span class="sxs-lookup"><span data-stu-id="256e3-177">The amount of transparency of the gradient stop color, as a percentage.</span></span>  <br/> |<span data-ttu-id="256e3-178">[[Gradient Stop] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="256e3-178">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
|<span data-ttu-id="256e3-179">GradientStopPosition</span><span class="sxs-lookup"><span data-stu-id="256e3-179">GradientStopPosition</span></span>  <br/> |<span data-ttu-id="256e3-180">線のグラデーションの方向、パーセンテージの原点からグラデーションのグラデーションの外側のエッジに沿ったグラデーションの分岐点の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="256e3-180">The position of the gradient stop along the direction of the line gradient, as a percentage from the point of origin of the gradient to the outer edge of the gradient.</span></span>  <br/> |<span data-ttu-id="256e3-181">[[Gradient Stop] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md)</span><span class="sxs-lookup"><span data-stu-id="256e3-181">[Gradient Stop Row (Line Gradient Section)](gradient-stop-row-line-gradient-section.md)</span></span> <br/> |
   

