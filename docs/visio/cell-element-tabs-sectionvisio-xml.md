---
title: セル要素 ([Tabs] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: 図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。
ms.openlocfilehash: c6641c452144544dc769616130c96d6cf89aca23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395064"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="4192f-103">セル要素 ([Tabs] セクション) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4192f-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="4192f-104">図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4192f-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4192f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4192f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4192f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4192f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4192f-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4192f-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4192f-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4192f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4192f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4192f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4192f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4192f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4192f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4192f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4192f-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="4192f-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4192f-113">定義</span><span class="sxs-lookup"><span data-stu-id="4192f-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4192f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4192f-114">Elements and attributes</span></span>

<span data-ttu-id="4192f-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4192f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4192f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4192f-116">Parent elements</span></span>

|<span data-ttu-id="4192f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4192f-117">**Element**</span></span>|<span data-ttu-id="4192f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4192f-118">**Type**</span></span>|<span data-ttu-id="4192f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4192f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4192f-120">[Row 要素 ([タブ] セクション)](row-element-tabs-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="4192f-120">[Row element (Tabs Section)](row-element-tabs-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="4192f-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="4192f-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4192f-122">図形および [スタイル] タブの停止位置や配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="4192f-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4192f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4192f-123">Child elements</span></span>

|<span data-ttu-id="4192f-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="4192f-124">**Element**</span></span>|<span data-ttu-id="4192f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4192f-125">**Type**</span></span>|<span data-ttu-id="4192f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4192f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4192f-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="4192f-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4192f-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="4192f-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4192f-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="4192f-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4192f-130">属性</span><span class="sxs-lookup"><span data-stu-id="4192f-130">Attributes</span></span>

|<span data-ttu-id="4192f-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="4192f-131">**Attribute**</span></span>|<span data-ttu-id="4192f-132">**型**</span><span class="sxs-lookup"><span data-stu-id="4192f-132">**Type**</span></span>|<span data-ttu-id="4192f-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="4192f-133">**Required**</span></span>|<span data-ttu-id="4192f-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="4192f-134">**Description**</span></span>|<span data-ttu-id="4192f-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4192f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4192f-136">E</span><span class="sxs-lookup"><span data-stu-id="4192f-136">E</span></span>  <br/> |<span data-ttu-id="4192f-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4192f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="4192f-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4192f-138">optional</span></span>  <br/> |<span data-ttu-id="4192f-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="4192f-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="4192f-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="4192f-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="4192f-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="4192f-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="4192f-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="4192f-142">F</span></span>  <br/> |<span data-ttu-id="4192f-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4192f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4192f-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="4192f-144">optional</span></span>  <br/> | <span data-ttu-id="4192f-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="4192f-145">Represents the element's formula.</span></span> <span data-ttu-id="4192f-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4192f-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="4192f-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="4192f-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="4192f-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="4192f-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="4192f-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="4192f-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="4192f-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="4192f-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="4192f-151">N</span><span class="sxs-lookup"><span data-stu-id="4192f-151">N</span></span>  <br/> |<span data-ttu-id="4192f-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4192f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="4192f-153">必須</span><span class="sxs-lookup"><span data-stu-id="4192f-153">required</span></span>  <br/> |<span data-ttu-id="4192f-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="4192f-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="4192f-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="4192f-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="4192f-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4192f-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="4192f-157">U</span><span class="sxs-lookup"><span data-stu-id="4192f-157">U</span></span>  <br/> |<span data-ttu-id="4192f-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4192f-158">xsd:string</span></span>  <br/> |<span data-ttu-id="4192f-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="4192f-159">optional</span></span>  <br/> |<span data-ttu-id="4192f-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="4192f-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="4192f-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="4192f-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="4192f-162">V</span><span class="sxs-lookup"><span data-stu-id="4192f-162">V</span></span>  <br/> |<span data-ttu-id="4192f-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4192f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="4192f-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="4192f-164">optional</span></span>  <br/> |<span data-ttu-id="4192f-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="4192f-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="4192f-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="4192f-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4192f-167">備考</span><span class="sxs-lookup"><span data-stu-id="4192f-167">Remarks</span></span>

<span data-ttu-id="4192f-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4192f-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="4192f-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4192f-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="4192f-170">**値**</span><span class="sxs-lookup"><span data-stu-id="4192f-170">**Value**</span></span>|<span data-ttu-id="4192f-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="4192f-171">**Description**</span></span>|<span data-ttu-id="4192f-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="4192f-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4192f-173">位置揃え</span><span class="sxs-lookup"><span data-stu-id="4192f-173">Alignment</span></span>  <br/> |<span data-ttu-id="4192f-174">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="4192f-174">Specifies the tab alignment.</span></span>  <br/> |<span data-ttu-id="4192f-175">[[Alignment] セル ([Tabs] セクション)](alignment-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="4192f-175">[Alignment Cell (Tabs Section)](alignment-cell-tabs-section.md)</span></span> <br/> |
|<span data-ttu-id="4192f-176">Position</span><span class="sxs-lookup"><span data-stu-id="4192f-176">Position</span></span>  <br/> |<span data-ttu-id="4192f-p104">タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。</span><span class="sxs-lookup"><span data-stu-id="4192f-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |<span data-ttu-id="4192f-180">[[Position] セル ([Tabs] セクション)](position-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="4192f-180">[Position Cell (Tabs Section)](position-cell-tabs-section.md)</span></span> <br/> |
   

