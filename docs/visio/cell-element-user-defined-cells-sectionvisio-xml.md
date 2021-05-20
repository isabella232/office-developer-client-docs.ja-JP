---
title: Cell 要素 ([ユーザー定義のセル] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: 他のセルおよびアドオン ツールによって参照できる、ユーザー指定の情報の 1 つのプロパティ。
ms.openlocfilehash: 5b7e3eb1f4550430e4df51098b86862fcc7400da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539315"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="1e5a5-103">Cell 要素 ([ユーザー定義のセル] セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1e5a5-103">Cell element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="1e5a5-104">他のセルおよびアドオン ツールによって参照できる、ユーザー指定の情報の 1 つのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-104">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e5a5-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="1e5a5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e5a5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1e5a5-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="1e5a5-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1e5a5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1e5a5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1e5a5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1e5a5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1e5a5-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1e5a5-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="1e5a5-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e5a5-113">定義</span><span class="sxs-lookup"><span data-stu-id="1e5a5-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e5a5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1e5a5-114">Elements and attributes</span></span>

<span data-ttu-id="1e5a5-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1e5a5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1e5a5-116">Parent elements</span></span>

|<span data-ttu-id="1e5a5-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-117">**Element**</span></span>|<span data-ttu-id="1e5a5-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-118">**Type**</span></span>|<span data-ttu-id="1e5a5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e5a5-120">[Row 要素 ([ユーザー定義のセル] セクション)](row-element-user-defined-cells-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="1e5a5-120">[Row element (User-defined Cells Section)](row-element-user-defined-cells-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="1e5a5-121">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="1e5a5-121">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e5a5-122">他のセルおよびアドオン ツールによって参照できる、ユーザー指定の情報の 1 つのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-122">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e5a5-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1e5a5-123">Child elements</span></span>

|<span data-ttu-id="1e5a5-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-124">**Element**</span></span>|<span data-ttu-id="1e5a5-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-125">**Type**</span></span>|<span data-ttu-id="1e5a5-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e5a5-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="1e5a5-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e5a5-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="1e5a5-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e5a5-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1e5a5-130">属性</span><span class="sxs-lookup"><span data-stu-id="1e5a5-130">Attributes</span></span>

|<span data-ttu-id="1e5a5-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-131">**Attribute**</span></span>|<span data-ttu-id="1e5a5-132">**型**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-132">**Type**</span></span>|<span data-ttu-id="1e5a5-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-133">**Required**</span></span>|<span data-ttu-id="1e5a5-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-134">**Description**</span></span>|<span data-ttu-id="1e5a5-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e5a5-136">E</span><span class="sxs-lookup"><span data-stu-id="1e5a5-136">E</span></span>  <br/> |<span data-ttu-id="1e5a5-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e5a5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1e5a5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e5a5-138">optional</span></span>  <br/> |<span data-ttu-id="1e5a5-139">数式がエラーと評価されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="1e5a5-140">E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="1e5a5-141">エラー メッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="1e5a5-142">F</span><span class="sxs-lookup"><span data-stu-id="1e5a5-142">F</span></span>  <br/> |<span data-ttu-id="1e5a5-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e5a5-143">xsd:string</span></span>  <br/> |<span data-ttu-id="1e5a5-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e5a5-144">optional</span></span>  <br/> | <span data-ttu-id="1e5a5-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-145">Represents the element's formula.</span></span> <span data-ttu-id="1e5a5-146">この属性には、次のいずれかの文字列を含めできます。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="1e5a5-147">式がローカルに存在する場合は'(一部の数式)'</span><span class="sxs-lookup"><span data-stu-id="1e5a5-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="1e5a5-148">`No Formula` 数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="1e5a5-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="1e5a5-149">`Inh` 数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="1e5a5-150">数式。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="1e5a5-151">N</span><span class="sxs-lookup"><span data-stu-id="1e5a5-151">N</span></span>  <br/> |<span data-ttu-id="1e5a5-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e5a5-152">xsd:string</span></span>  <br/> |<span data-ttu-id="1e5a5-153">必須</span><span class="sxs-lookup"><span data-stu-id="1e5a5-153">required</span></span>  <br/> |<span data-ttu-id="1e5a5-154">[シェイプシート] セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="1e5a5-155">[シェイプシート] セルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="1e5a5-156">以下の「備考」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="1e5a5-157">U</span><span class="sxs-lookup"><span data-stu-id="1e5a5-157">U</span></span>  <br/> |<span data-ttu-id="1e5a5-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e5a5-158">xsd:string</span></span>  <br/> |<span data-ttu-id="1e5a5-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e5a5-159">optional</span></span>  <br/> |<span data-ttu-id="1e5a5-160">測定単位を表します 既定は DL です。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="1e5a5-161">セルの単位。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="1e5a5-162">V</span><span class="sxs-lookup"><span data-stu-id="1e5a5-162">V</span></span>  <br/> |<span data-ttu-id="1e5a5-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1e5a5-163">xsd:string</span></span>  <br/> |<span data-ttu-id="1e5a5-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e5a5-164">optional</span></span>  <br/> |<span data-ttu-id="1e5a5-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="1e5a5-166">[シェイプシート] セルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e5a5-167">注釈</span><span class="sxs-lookup"><span data-stu-id="1e5a5-167">Remarks</span></span>

<span data-ttu-id="1e5a5-168">この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="1e5a5-169">次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="1e5a5-170">**値**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-170">**Value**</span></span>|<span data-ttu-id="1e5a5-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-171">**Description**</span></span>|<span data-ttu-id="1e5a5-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="1e5a5-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1e5a5-173">プロンプト</span><span class="sxs-lookup"><span data-stu-id="1e5a5-173">Prompt</span></span>  <br/> |<span data-ttu-id="1e5a5-174">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-174">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |<span data-ttu-id="1e5a5-175">[[Prompt] セル ([User-Defined Cells] セクション)](prompt-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="1e5a5-175">[Prompt Cell (User-Defined Cells Section)](prompt-cell-user-defined-cells-section.md)</span></span> <br/> |
|<span data-ttu-id="1e5a5-176">値</span><span class="sxs-lookup"><span data-stu-id="1e5a5-176">Value</span></span>  <br/> |<span data-ttu-id="1e5a5-177">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1e5a5-177">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |<span data-ttu-id="1e5a5-178">[[Value] セル ([User-Defined Cells] セクション)](value-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="1e5a5-178">[Value Cell (User-Defined Cells Section)](value-cell-user-defined-cells-section.md)</span></span> <br/> |
   

