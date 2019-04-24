---
title: Cell 要素 ([スクラッチ] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af17b1c5-51ee-f46f-79d0-4f33369b66f1
description: 他のセルから参照できる数式を入力およびテストするための作業領域を指定します。
ms.openlocfilehash: 147cc152ec20e3e2b032b91f6387ec06a3cb1d6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339530"
---
# <a name="cell-element-scratch-section-visio-xml"></a><span data-ttu-id="2026e-103">Cell 要素 ([スクラッチ] セクション) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2026e-103">Cell element (Scratch Section) ('Visio XML')</span></span>

<span data-ttu-id="2026e-104">他のセルから参照できる数式を入力およびテストするための作業領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="2026e-104">Specifies a work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2026e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="2026e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2026e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2026e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2026e-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2026e-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2026e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2026e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2026e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2026e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2026e-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="2026e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2026e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="2026e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2026e-112">文書 .xml、masters、.master、xml、ページ # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="2026e-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2026e-113">定義</span><span class="sxs-lookup"><span data-stu-id="2026e-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2026e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2026e-114">Elements and attributes</span></span>

<span data-ttu-id="2026e-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2026e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2026e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="2026e-116">Parent elements</span></span>

|<span data-ttu-id="2026e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="2026e-117">**Element**</span></span>|<span data-ttu-id="2026e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2026e-118">**Type**</span></span>|<span data-ttu-id="2026e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="2026e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2026e-120">Row 要素 (スクラッチセクション)</span><span class="sxs-lookup"><span data-stu-id="2026e-120">Row element (Scratch Section)</span></span>](row-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2026e-121">ScratchRow_Type</span><span class="sxs-lookup"><span data-stu-id="2026e-121">ScratchRow_Type</span></span>](scratch_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2026e-122">他のセルから参照できる数式を入力およびテストするための作業領域を指定します。</span><span class="sxs-lookup"><span data-stu-id="2026e-122">Specifies a work area for entering and testing formulas that can be referred to by other cells.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2026e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="2026e-123">Child elements</span></span>

|<span data-ttu-id="2026e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2026e-124">**Element**</span></span>|<span data-ttu-id="2026e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="2026e-125">**Type**</span></span>|<span data-ttu-id="2026e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="2026e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2026e-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="2026e-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2026e-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="2026e-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2026e-129">ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="2026e-129">Specifies a reference to a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2026e-130">属性</span><span class="sxs-lookup"><span data-stu-id="2026e-130">Attributes</span></span>

|<span data-ttu-id="2026e-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="2026e-131">**Attribute**</span></span>|<span data-ttu-id="2026e-132">**型**</span><span class="sxs-lookup"><span data-stu-id="2026e-132">**Type**</span></span>|<span data-ttu-id="2026e-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="2026e-133">**Required**</span></span>|<span data-ttu-id="2026e-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="2026e-134">**Description**</span></span>|<span data-ttu-id="2026e-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="2026e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2026e-136">E</span><span class="sxs-lookup"><span data-stu-id="2026e-136">E</span></span>  <br/> |<span data-ttu-id="2026e-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2026e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2026e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="2026e-138">optional</span></span>  <br/> |<span data-ttu-id="2026e-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="2026e-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="2026e-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="2026e-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="2026e-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="2026e-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="2026e-142">F</span><span class="sxs-lookup"><span data-stu-id="2026e-142">F</span></span>  <br/> |<span data-ttu-id="2026e-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2026e-143">xsd:string</span></span>  <br/> |<span data-ttu-id="2026e-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="2026e-144">optional</span></span>  <br/> | <span data-ttu-id="2026e-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="2026e-145">Represents the element's formula.</span></span> <span data-ttu-id="2026e-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2026e-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="2026e-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="2026e-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="2026e-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="2026e-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="2026e-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="2026e-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="2026e-150">数式。</span><span class="sxs-lookup"><span data-stu-id="2026e-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="2026e-151">N</span><span class="sxs-lookup"><span data-stu-id="2026e-151">N</span></span>  <br/> |<span data-ttu-id="2026e-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2026e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="2026e-153">必須</span><span class="sxs-lookup"><span data-stu-id="2026e-153">required</span></span>  <br/> |<span data-ttu-id="2026e-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="2026e-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="2026e-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="2026e-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="2026e-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2026e-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="2026e-157">U</span><span class="sxs-lookup"><span data-stu-id="2026e-157">U</span></span>  <br/> |<span data-ttu-id="2026e-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2026e-158">xsd:string</span></span>  <br/> |<span data-ttu-id="2026e-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="2026e-159">optional</span></span>  <br/> |<span data-ttu-id="2026e-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="2026e-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="2026e-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="2026e-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="2026e-162">V</span><span class="sxs-lookup"><span data-stu-id="2026e-162">V</span></span>  <br/> |<span data-ttu-id="2026e-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2026e-163">xsd:string</span></span>  <br/> |<span data-ttu-id="2026e-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="2026e-164">optional</span></span>  <br/> |<span data-ttu-id="2026e-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="2026e-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="2026e-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2026e-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
### <a name="remarks"></a><span data-ttu-id="2026e-167">解説</span><span class="sxs-lookup"><span data-stu-id="2026e-167">Remarks</span></span>

<span data-ttu-id="2026e-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="2026e-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="2026e-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2026e-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="2026e-170">**値**</span><span class="sxs-lookup"><span data-stu-id="2026e-170">**Value**</span></span>|<span data-ttu-id="2026e-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="2026e-171">**Description**</span></span>|<span data-ttu-id="2026e-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="2026e-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2026e-173">A</span><span class="sxs-lookup"><span data-stu-id="2026e-173">A</span></span>  <br/> |<span data-ttu-id="2026e-174">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-174">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-175">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-175">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="2026e-176">B</span><span class="sxs-lookup"><span data-stu-id="2026e-176">B</span></span>  <br/> |<span data-ttu-id="2026e-177">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-177">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-178">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-178">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="2026e-179">C</span><span class="sxs-lookup"><span data-stu-id="2026e-179">C</span></span>  <br/> |<span data-ttu-id="2026e-180">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-180">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-181">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-181">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="2026e-182">D</span><span class="sxs-lookup"><span data-stu-id="2026e-182">D</span></span>  <br/> |<span data-ttu-id="2026e-183">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-183">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-184">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-184">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="2026e-185">X</span><span class="sxs-lookup"><span data-stu-id="2026e-185">X</span></span>  <br/> |<span data-ttu-id="2026e-186">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-186">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-187">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-187">[Scratch Section](scratch-section.md)</span></span> <br/> |
|<span data-ttu-id="2026e-188">Y</span><span class="sxs-lookup"><span data-stu-id="2026e-188">Y</span></span>  <br/> |<span data-ttu-id="2026e-189">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="2026e-189">A scratch cell that you can use for entering or testing formulas.</span></span>  <br/> |<span data-ttu-id="2026e-190">[[Scratch] セクション](scratch-section.md)</span><span class="sxs-lookup"><span data-stu-id="2026e-190">[Scratch Section](scratch-section.md)</span></span> <br/> |
   

