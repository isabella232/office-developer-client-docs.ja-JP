---
title: Cell 要素 ([タブ] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: 図形およびスタイルタブの終了位置または配置を制御するプロパティを指定します。
ms.openlocfilehash: c6641c452144544dc769616130c96d6cf89aca23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339642"
---
# <a name="cell-element-tabs-section-visio-xml"></a><span data-ttu-id="3af6b-103">Cell 要素 ([タブ] セクション) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3af6b-103">Cell element (Tabs Section) ('Visio XML')</span></span>

<span data-ttu-id="3af6b-104">図形およびスタイルタブの終了位置または配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-104">Specifies a property that controls shape and style tab stop position or alignment.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3af6b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3af6b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3af6b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3af6b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3af6b-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3af6b-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3af6b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3af6b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3af6b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3af6b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3af6b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3af6b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3af6b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3af6b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3af6b-112">文書 .xml、master # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="3af6b-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3af6b-113">定義</span><span class="sxs-lookup"><span data-stu-id="3af6b-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3af6b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3af6b-114">Elements and attributes</span></span>

<span data-ttu-id="3af6b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3af6b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3af6b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3af6b-116">Parent elements</span></span>

|<span data-ttu-id="3af6b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3af6b-117">**Element**</span></span>|<span data-ttu-id="3af6b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3af6b-118">**Type**</span></span>|<span data-ttu-id="3af6b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3af6b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3af6b-120">Row 要素 (Tabs セクション)</span><span class="sxs-lookup"><span data-stu-id="3af6b-120">Row element (Tabs Section)</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="3af6b-121">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="3af6b-121">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3af6b-122">図形およびスタイルタブの終了位置または配置を制御するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-122">Specifies a property that controls shape and style tab stop position or alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3af6b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3af6b-123">Child elements</span></span>

|<span data-ttu-id="3af6b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3af6b-124">**Element**</span></span>|<span data-ttu-id="3af6b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="3af6b-125">**Type**</span></span>|<span data-ttu-id="3af6b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="3af6b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3af6b-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="3af6b-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3af6b-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="3af6b-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3af6b-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3af6b-130">属性</span><span class="sxs-lookup"><span data-stu-id="3af6b-130">Attributes</span></span>

|<span data-ttu-id="3af6b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="3af6b-131">**Attribute**</span></span>|<span data-ttu-id="3af6b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="3af6b-132">**Type**</span></span>|<span data-ttu-id="3af6b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="3af6b-133">**Required**</span></span>|<span data-ttu-id="3af6b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="3af6b-134">**Description**</span></span>|<span data-ttu-id="3af6b-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3af6b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3af6b-136">E</span><span class="sxs-lookup"><span data-stu-id="3af6b-136">E</span></span>  <br/> |<span data-ttu-id="3af6b-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3af6b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3af6b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="3af6b-138">optional</span></span>  <br/> |<span data-ttu-id="3af6b-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="3af6b-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="3af6b-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="3af6b-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="3af6b-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="3af6b-142">F</span><span class="sxs-lookup"><span data-stu-id="3af6b-142">F</span></span>  <br/> |<span data-ttu-id="3af6b-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3af6b-143">xsd:string</span></span>  <br/> |<span data-ttu-id="3af6b-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="3af6b-144">optional</span></span>  <br/> | <span data-ttu-id="3af6b-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-145">Represents the element's formula.</span></span> <span data-ttu-id="3af6b-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3af6b-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="3af6b-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="3af6b-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="3af6b-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="3af6b-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="3af6b-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="3af6b-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="3af6b-150">数式。</span><span class="sxs-lookup"><span data-stu-id="3af6b-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="3af6b-151">N</span><span class="sxs-lookup"><span data-stu-id="3af6b-151">N</span></span>  <br/> |<span data-ttu-id="3af6b-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3af6b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="3af6b-153">必須</span><span class="sxs-lookup"><span data-stu-id="3af6b-153">required</span></span>  <br/> |<span data-ttu-id="3af6b-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="3af6b-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="3af6b-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3af6b-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="3af6b-157">U</span><span class="sxs-lookup"><span data-stu-id="3af6b-157">U</span></span>  <br/> |<span data-ttu-id="3af6b-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3af6b-158">xsd:string</span></span>  <br/> |<span data-ttu-id="3af6b-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="3af6b-159">optional</span></span>  <br/> |<span data-ttu-id="3af6b-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="3af6b-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="3af6b-162">V</span><span class="sxs-lookup"><span data-stu-id="3af6b-162">V</span></span>  <br/> |<span data-ttu-id="3af6b-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3af6b-163">xsd:string</span></span>  <br/> |<span data-ttu-id="3af6b-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="3af6b-164">optional</span></span>  <br/> |<span data-ttu-id="3af6b-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="3af6b-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3af6b-167">解説</span><span class="sxs-lookup"><span data-stu-id="3af6b-167">Remarks</span></span>

<span data-ttu-id="3af6b-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3af6b-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="3af6b-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3af6b-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="3af6b-170">**値**</span><span class="sxs-lookup"><span data-stu-id="3af6b-170">**Value**</span></span>|<span data-ttu-id="3af6b-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="3af6b-171">**Description**</span></span>|<span data-ttu-id="3af6b-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="3af6b-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3af6b-173">Alignment</span><span class="sxs-lookup"><span data-stu-id="3af6b-173">Alignment</span></span>  <br/> |<span data-ttu-id="3af6b-174">タブの整列方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="3af6b-174">Specifies the tab alignment.</span></span>  <br/> |<span data-ttu-id="3af6b-175">[[Alignment] セル ([Tabs] セクション)](alignment-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="3af6b-175">[Alignment Cell (Tabs Section)](alignment-cell-tabs-section.md)</span></span> <br/> |
|<span data-ttu-id="3af6b-176">Position</span><span class="sxs-lookup"><span data-stu-id="3af6b-176">Position</span></span>  <br/> |<span data-ttu-id="3af6b-p104">タブ位置を指定します。タブ位置は図面の縮尺による影響を受けません。図面の縮尺を変更しても、タブ位置は変わりません。</span><span class="sxs-lookup"><span data-stu-id="3af6b-p104">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>  <br/> |<span data-ttu-id="3af6b-180">[[Position] セル ([Tabs] セクション)](position-cell-tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="3af6b-180">[Position Cell (Tabs Section)](position-cell-tabs-section.md)</span></span> <br/> |
   

