---
title: Cell 要素 ([タブ] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: 図形やスタイルのタブ位置または配置を制御するプロパティを指定します。
ms.openlocfilehash: c3758f34058c08f98f8d99cf5c03f456e855d7df
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539363"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="e2718-103">Cell 要素 ([タブ] セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e2718-103">Cell element (Tabs Section) (Visio XML)</span></span>

<span data-ttu-id="e2718-104">図形やスタイルのタブ位置または配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e2718-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="e2718-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2718-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e2718-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e2718-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e2718-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2718-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e2718-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2718-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e2718-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e2718-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2718-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2718-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="e2718-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e2718-112">document.xml、master#.xml、page#.xml</span><span class="sxs-lookup"><span data-stu-id="e2718-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2718-113">定義</span><span class="sxs-lookup"><span data-stu-id="e2718-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2718-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e2718-114">Elements and attributes</span></span>

<span data-ttu-id="e2718-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2718-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2718-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e2718-116">Parent elements</span></span>

|<span data-ttu-id="e2718-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e2718-117">**Element**</span></span>|<span data-ttu-id="e2718-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e2718-118">**Type**</span></span>|<span data-ttu-id="e2718-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2718-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2718-120">[Row 要素 ([タブ] セクション)](row-element-tabs-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="e2718-120">[Row element (Tabs Section)](row-element-tabs-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="e2718-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="e2718-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2718-122">図形やスタイルのタブ位置または配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2718-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e2718-123">Child elements</span></span>

|<span data-ttu-id="e2718-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2718-124">**Element**</span></span>|<span data-ttu-id="e2718-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e2718-125">**Type**</span></span>|<span data-ttu-id="e2718-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2718-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2718-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="e2718-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2718-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e2718-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2718-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e2718-130">属性</span><span class="sxs-lookup"><span data-stu-id="e2718-130">Attributes</span></span>

|<span data-ttu-id="e2718-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="e2718-131">**Attribute**</span></span>|<span data-ttu-id="e2718-132">**型**</span><span class="sxs-lookup"><span data-stu-id="e2718-132">**Type**</span></span>|<span data-ttu-id="e2718-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="e2718-133">**Required**</span></span>|<span data-ttu-id="e2718-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2718-134">**Description**</span></span>|<span data-ttu-id="e2718-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="e2718-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2718-136">E</span><span class="sxs-lookup"><span data-stu-id="e2718-136">E</span></span>  <br/> |<span data-ttu-id="e2718-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e2718-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e2718-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2718-138">optional</span></span>  <br/> |<span data-ttu-id="e2718-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e2718-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="e2718-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="e2718-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="e2718-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="e2718-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="e2718-142">F</span><span class="sxs-lookup"><span data-stu-id="e2718-142">F</span></span>  <br/> |<span data-ttu-id="e2718-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e2718-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e2718-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2718-144">optional</span></span>  <br/> | <span data-ttu-id="e2718-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="e2718-145">Represents the element's formula.</span></span> <span data-ttu-id="e2718-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="e2718-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="e2718-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="e2718-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="e2718-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="e2718-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="e2718-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="e2718-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="e2718-150">数式。</span><span class="sxs-lookup"><span data-stu-id="e2718-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="e2718-151">N</span><span class="sxs-lookup"><span data-stu-id="e2718-151">N</span></span>  <br/> |<span data-ttu-id="e2718-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e2718-152">xsd:string</span></span>  <br/> |<span data-ttu-id="e2718-153">必須</span><span class="sxs-lookup"><span data-stu-id="e2718-153">required</span></span>  <br/> |<span data-ttu-id="e2718-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="e2718-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="e2718-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="e2718-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2718-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="e2718-157">U</span><span class="sxs-lookup"><span data-stu-id="e2718-157">U</span></span>  <br/> |<span data-ttu-id="e2718-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e2718-158">xsd:string</span></span>  <br/> |<span data-ttu-id="e2718-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2718-159">optional</span></span>  <br/> |<span data-ttu-id="e2718-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="e2718-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="e2718-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="e2718-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="e2718-162">V</span><span class="sxs-lookup"><span data-stu-id="e2718-162">V</span></span>  <br/> |<span data-ttu-id="e2718-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e2718-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e2718-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2718-164">optional</span></span>  <br/> |<span data-ttu-id="e2718-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="e2718-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="e2718-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2718-167">注釈</span><span class="sxs-lookup"><span data-stu-id="e2718-167">Remarks</span></span>

<span data-ttu-id="e2718-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2718-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="e2718-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="e2718-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="e2718-170">**値**</span><span class="sxs-lookup"><span data-stu-id="e2718-170">**Value**</span></span>|<span data-ttu-id="e2718-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="e2718-171">**Description**</span></span>|<span data-ttu-id="e2718-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="e2718-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2718-173">Alignment</span><span class="sxs-lookup"><span data-stu-id="e2718-173">Alignment</span></span>  <br/> |<span data-ttu-id="e2718-174">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2718-174">Specifies the tab alignment.</span></span>  <br/> |<span data-ttu-id="e2718-175">[[Alignment] セル ([Tabs] セクション)](alignment-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="e2718-175">[Alignment Cell (Tabs Section)](alignment-cell-tabs-section.md)</span></span> <br/> |
|<span data-ttu-id="e2718-176">Position</span><span class="sxs-lookup"><span data-stu-id="e2718-176">Position</span></span>  <br/> |<span data-ttu-id="e2718-p104">タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。</span><span class="sxs-lookup"><span data-stu-id="e2718-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |<span data-ttu-id="e2718-180">[[Position] セル ([Tabs] セクション)](position-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="e2718-180">[Position Cell (Tabs Section)](position-cell-tabs-section.md)</span></span> <br/> |
   

