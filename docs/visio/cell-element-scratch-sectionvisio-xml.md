---
title: Cell 要素 (スクラッチセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: 他のセルから参照できる数式を入力およびテストするための作業領域を指定します。
ms.openlocfilehash: 32e7eb2cfe13221ced2a8096acde412625d3ad33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542325"
---
# <a name="cell-element-scratch-section-visio-xml"></a><span data-ttu-id="9a13d-103">Cell 要素 (スクラッチセクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9a13d-103">Cell element (Scratch Section) (Visio XML)</span></span>

<span data-ttu-id="9a13d-104">他のセルから参照できる数式を入力およびテストするための作業領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-104">Specifies a work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a13d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9a13d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a13d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9a13d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9a13d-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="9a13d-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9a13d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a13d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9a13d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9a13d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9a13d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9a13d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9a13d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9a13d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9a13d-112">文書 .xml、masters、.master、xml、ページ # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="9a13d-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a13d-113">定義</span><span class="sxs-lookup"><span data-stu-id="9a13d-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a13d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9a13d-114">Elements and attributes</span></span>

<span data-ttu-id="9a13d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a13d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9a13d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9a13d-116">Parent elements</span></span>

|<span data-ttu-id="9a13d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9a13d-117">**Element**</span></span>|<span data-ttu-id="9a13d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9a13d-118">**Type**</span></span>|<span data-ttu-id="9a13d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a13d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a13d-120">Row 要素 (スクラッチセクション)</span><span class="sxs-lookup"><span data-stu-id="9a13d-120">Row element (Scratch Section)</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9a13d-121">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="9a13d-121">ScratchRow_Type</span></span>](scratch_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a13d-122">他のセルから参照できる数式を入力およびテストするための作業領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-122">Specifies a work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9a13d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9a13d-123">Child elements</span></span>

|<span data-ttu-id="9a13d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a13d-124">**Element**</span></span>|<span data-ttu-id="9a13d-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9a13d-125">**Type**</span></span>|<span data-ttu-id="9a13d-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a13d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a13d-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="9a13d-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a13d-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="9a13d-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9a13d-129">ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-129">Specifies a reference to a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9a13d-130">属性</span><span class="sxs-lookup"><span data-stu-id="9a13d-130">Attributes</span></span>

|<span data-ttu-id="9a13d-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="9a13d-131">**Attribute**</span></span>|<span data-ttu-id="9a13d-132">**型**</span><span class="sxs-lookup"><span data-stu-id="9a13d-132">**Type**</span></span>|<span data-ttu-id="9a13d-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="9a13d-133">**Required**</span></span>|<span data-ttu-id="9a13d-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a13d-134">**Description**</span></span>|<span data-ttu-id="9a13d-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="9a13d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a13d-136">E</span><span class="sxs-lookup"><span data-stu-id="9a13d-136">E</span></span>  <br/> |<span data-ttu-id="9a13d-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9a13d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="9a13d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a13d-138">optional</span></span>  <br/> |<span data-ttu-id="9a13d-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="9a13d-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="9a13d-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="9a13d-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="9a13d-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="9a13d-142">F</span><span class="sxs-lookup"><span data-stu-id="9a13d-142">F</span></span>  <br/> |<span data-ttu-id="9a13d-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9a13d-143">xsd:string</span></span>  <br/> |<span data-ttu-id="9a13d-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a13d-144">optional</span></span>  <br/> | <span data-ttu-id="9a13d-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-145">Represents the element's formula.</span></span> <span data-ttu-id="9a13d-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9a13d-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="9a13d-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="9a13d-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="9a13d-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="9a13d-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="9a13d-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="9a13d-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="9a13d-150">数式。</span><span class="sxs-lookup"><span data-stu-id="9a13d-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="9a13d-151">N</span><span class="sxs-lookup"><span data-stu-id="9a13d-151">N</span></span>  <br/> |<span data-ttu-id="9a13d-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9a13d-152">xsd:string</span></span>  <br/> |<span data-ttu-id="9a13d-153">必須</span><span class="sxs-lookup"><span data-stu-id="9a13d-153">required</span></span>  <br/> |<span data-ttu-id="9a13d-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="9a13d-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="9a13d-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a13d-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="9a13d-157">U</span><span class="sxs-lookup"><span data-stu-id="9a13d-157">U</span></span>  <br/> |<span data-ttu-id="9a13d-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9a13d-158">xsd:string</span></span>  <br/> |<span data-ttu-id="9a13d-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a13d-159">optional</span></span>  <br/> |<span data-ttu-id="9a13d-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="9a13d-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="9a13d-162">V</span><span class="sxs-lookup"><span data-stu-id="9a13d-162">V</span></span>  <br/> |<span data-ttu-id="9a13d-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="9a13d-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9a13d-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="9a13d-164">optional</span></span>  <br/> |<span data-ttu-id="9a13d-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="9a13d-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a13d-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
### <a name="remarks"></a><span data-ttu-id="9a13d-167">注釈</span><span class="sxs-lookup"><span data-stu-id="9a13d-167">Remarks</span></span>

<span data-ttu-id="9a13d-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a13d-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="9a13d-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a13d-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="9a13d-170">**値**</span><span class="sxs-lookup"><span data-stu-id="9a13d-170">**Value**</span></span>|<span data-ttu-id="9a13d-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a13d-171">**Description**</span></span>|<span data-ttu-id="9a13d-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="9a13d-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a13d-173">A</span><span class="sxs-lookup"><span data-stu-id="9a13d-173">A</span></span>  <br/> |<span data-ttu-id="9a13d-174">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-174">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-175">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-175">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="9a13d-176">B</span><span class="sxs-lookup"><span data-stu-id="9a13d-176">B</span></span>  <br/> |<span data-ttu-id="9a13d-177">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-177">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-178">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-178">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="9a13d-179">C</span><span class="sxs-lookup"><span data-stu-id="9a13d-179">C</span></span>  <br/> |<span data-ttu-id="9a13d-180">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-180">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-181">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-181">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="9a13d-182">D</span><span class="sxs-lookup"><span data-stu-id="9a13d-182">D</span></span>  <br/> |<span data-ttu-id="9a13d-183">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-183">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-184">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-184">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="9a13d-185">X</span><span class="sxs-lookup"><span data-stu-id="9a13d-185">X</span></span>  <br/> |<span data-ttu-id="9a13d-186">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-186">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-187">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-187">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="9a13d-188">Y</span><span class="sxs-lookup"><span data-stu-id="9a13d-188">Y</span></span>  <br/> |<span data-ttu-id="9a13d-189">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="9a13d-189">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="9a13d-190">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="9a13d-190">[Scratch Section](scratch-section.md)</span></span> <br/> |
   

