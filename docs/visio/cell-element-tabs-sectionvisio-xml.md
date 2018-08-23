---
title: セル要素 ([Tabs] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: 図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。
ms.openlocfilehash: da2fb31688227180bb38a4366c3293a2e16600c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804982"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="92f89-103">セル要素 ([Tabs] セクション) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="92f89-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="92f89-104">図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="92f89-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="92f89-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="92f89-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92f89-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="92f89-106">**Element type**</span></span> <br/> |[<span data-ttu-id="92f89-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="92f89-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="92f89-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="92f89-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="92f89-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="92f89-109">**Schema file**</span></span> <br/> |<span data-ttu-id="92f89-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="92f89-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="92f89-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="92f89-111">**Document parts**</span></span> <br/> |<span data-ttu-id="92f89-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="92f89-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92f89-113">定義</span><span class="sxs-lookup"><span data-stu-id="92f89-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92f89-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="92f89-114">Elements and attributes</span></span>

<span data-ttu-id="92f89-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f89-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="92f89-116">親要素</span><span class="sxs-lookup"><span data-stu-id="92f89-116">Parent elements</span></span>

|<span data-ttu-id="92f89-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="92f89-117">**Element**</span></span>|<span data-ttu-id="92f89-118">**型**</span><span class="sxs-lookup"><span data-stu-id="92f89-118">**Type**</span></span>|<span data-ttu-id="92f89-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="92f89-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92f89-120">[Row 要素 ([タブ] セクション)](row-element-tabs-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="92f89-120">[Row element (Tabs Section)](row-element-tabs-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="92f89-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="92f89-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92f89-122">図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="92f89-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92f89-123">子要素</span><span class="sxs-lookup"><span data-stu-id="92f89-123">Child elements</span></span>

|<span data-ttu-id="92f89-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="92f89-124">**Element**</span></span>|<span data-ttu-id="92f89-125">**型**</span><span class="sxs-lookup"><span data-stu-id="92f89-125">**Type**</span></span>|<span data-ttu-id="92f89-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="92f89-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92f89-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="92f89-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92f89-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="92f89-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92f89-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="92f89-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="92f89-130">属性</span><span class="sxs-lookup"><span data-stu-id="92f89-130">Attributes</span></span>

|<span data-ttu-id="92f89-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="92f89-131">**Attribute**</span></span>|<span data-ttu-id="92f89-132">**型**</span><span class="sxs-lookup"><span data-stu-id="92f89-132">**Type**</span></span>|<span data-ttu-id="92f89-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="92f89-133">**Required**</span></span>|<span data-ttu-id="92f89-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="92f89-134">**Description**</span></span>|<span data-ttu-id="92f89-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="92f89-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92f89-136">E</span><span class="sxs-lookup"><span data-stu-id="92f89-136">E</span></span>  <br/> |<span data-ttu-id="92f89-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92f89-137">xsd:string</span></span>  <br/> |<span data-ttu-id="92f89-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="92f89-138">optional</span></span>  <br/> |<span data-ttu-id="92f89-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="92f89-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="92f89-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="92f89-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="92f89-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="92f89-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="92f89-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="92f89-142">F</span></span>  <br/> |<span data-ttu-id="92f89-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92f89-143">xsd:string</span></span>  <br/> |<span data-ttu-id="92f89-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="92f89-144">optional</span></span>  <br/> | <span data-ttu-id="92f89-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="92f89-145">Represents the element's formula.</span></span> <span data-ttu-id="92f89-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="92f89-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="92f89-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="92f89-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="92f89-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="92f89-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="92f89-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="92f89-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="92f89-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="92f89-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="92f89-151">N</span><span class="sxs-lookup"><span data-stu-id="92f89-151">N</span></span>  <br/> |<span data-ttu-id="92f89-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92f89-152">xsd:string</span></span>  <br/> |<span data-ttu-id="92f89-153">必須</span><span class="sxs-lookup"><span data-stu-id="92f89-153">required</span></span>  <br/> |<span data-ttu-id="92f89-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="92f89-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="92f89-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="92f89-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="92f89-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f89-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="92f89-157">U</span><span class="sxs-lookup"><span data-stu-id="92f89-157">U</span></span>  <br/> |<span data-ttu-id="92f89-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92f89-158">xsd:string</span></span>  <br/> |<span data-ttu-id="92f89-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="92f89-159">optional</span></span>  <br/> |<span data-ttu-id="92f89-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="92f89-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="92f89-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="92f89-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="92f89-162">V</span><span class="sxs-lookup"><span data-stu-id="92f89-162">V</span></span>  <br/> |<span data-ttu-id="92f89-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92f89-163">xsd:string</span></span>  <br/> |<span data-ttu-id="92f89-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="92f89-164">optional</span></span>  <br/> |<span data-ttu-id="92f89-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="92f89-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="92f89-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="92f89-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92f89-167">注釈</span><span class="sxs-lookup"><span data-stu-id="92f89-167">Remarks</span></span>

<span data-ttu-id="92f89-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="92f89-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="92f89-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92f89-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="92f89-170">**値**</span><span class="sxs-lookup"><span data-stu-id="92f89-170">**Value**</span></span>|<span data-ttu-id="92f89-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="92f89-171">**Description**</span></span>|<span data-ttu-id="92f89-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="92f89-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92f89-173">位置揃え</span><span class="sxs-lookup"><span data-stu-id="92f89-173">Alignment</span></span>  <br/> |<span data-ttu-id="92f89-174">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="92f89-174">Specifies the tab alignment.</span></span>  <br/> |<span data-ttu-id="92f89-175">[[Alignment] セル ([Tabs] セクション)](alignment-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="92f89-175">[Alignment Cell (Tabs Section)](alignment-cell-tabs-section.md)</span></span> <br/> |
|<span data-ttu-id="92f89-176">Position</span><span class="sxs-lookup"><span data-stu-id="92f89-176">Position</span></span>  <br/> |<span data-ttu-id="92f89-p104">タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。</span><span class="sxs-lookup"><span data-stu-id="92f89-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |<span data-ttu-id="92f89-180">[[Position] セル ([Tabs] セクション)](position-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="92f89-180">[Position Cell (Tabs Section)](position-cell-tabs-section.md)</span></span> <br/> |
   

