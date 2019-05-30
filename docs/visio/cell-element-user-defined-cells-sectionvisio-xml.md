---
title: Cell 要素 (ユーザー定義セルセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: ユーザーが指定した一連の情報の1つのプロパティ。他のセルとアドオンツールで参照できます。
ms.openlocfilehash: 5b7e3eb1f4550430e4df51098b86862fcc7400da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539315"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="248ce-103">Cell 要素 (ユーザー定義セルセクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="248ce-103">Cell element (User-defined Cells Section) (Visio XML)</span></span>

<span data-ttu-id="248ce-104">ユーザーが指定した一連の情報の1つのプロパティ。他のセルとアドオンツールで参照できます。</span><span class="sxs-lookup"><span data-stu-id="248ce-104">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="248ce-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="248ce-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="248ce-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="248ce-106">**Element type**</span></span> <br/> |[<span data-ttu-id="248ce-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="248ce-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="248ce-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="248ce-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="248ce-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="248ce-109">**Schema file**</span></span> <br/> |<span data-ttu-id="248ce-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="248ce-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="248ce-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="248ce-111">**Document parts**</span></span> <br/> |<span data-ttu-id="248ce-112">文書 .xml、masters、.master、xml、ページ # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="248ce-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="248ce-113">定義</span><span class="sxs-lookup"><span data-stu-id="248ce-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="248ce-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="248ce-114">Elements and attributes</span></span>

<span data-ttu-id="248ce-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="248ce-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="248ce-116">親要素</span><span class="sxs-lookup"><span data-stu-id="248ce-116">Parent elements</span></span>

|<span data-ttu-id="248ce-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="248ce-117">**Element**</span></span>|<span data-ttu-id="248ce-118">**型**</span><span class="sxs-lookup"><span data-stu-id="248ce-118">**Type**</span></span>|<span data-ttu-id="248ce-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="248ce-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="248ce-120">Row 要素 (ユーザー定義セルセクション)</span><span class="sxs-lookup"><span data-stu-id="248ce-120">Row element (User-defined Cells Section)</span></span>](row-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="248ce-121">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="248ce-121">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="248ce-122">ユーザーが指定した一連の情報の1つのプロパティ。他のセルとアドオンツールで参照できます。</span><span class="sxs-lookup"><span data-stu-id="248ce-122">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="248ce-123">子要素</span><span class="sxs-lookup"><span data-stu-id="248ce-123">Child elements</span></span>

|<span data-ttu-id="248ce-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="248ce-124">**Element**</span></span>|<span data-ttu-id="248ce-125">**型**</span><span class="sxs-lookup"><span data-stu-id="248ce-125">**Type**</span></span>|<span data-ttu-id="248ce-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="248ce-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="248ce-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="248ce-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="248ce-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="248ce-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="248ce-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="248ce-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="248ce-130">属性</span><span class="sxs-lookup"><span data-stu-id="248ce-130">Attributes</span></span>

|<span data-ttu-id="248ce-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="248ce-131">**Attribute**</span></span>|<span data-ttu-id="248ce-132">**型**</span><span class="sxs-lookup"><span data-stu-id="248ce-132">**Type**</span></span>|<span data-ttu-id="248ce-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="248ce-133">**Required**</span></span>|<span data-ttu-id="248ce-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="248ce-134">**Description**</span></span>|<span data-ttu-id="248ce-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="248ce-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="248ce-136">E</span><span class="sxs-lookup"><span data-stu-id="248ce-136">E</span></span>  <br/> |<span data-ttu-id="248ce-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="248ce-137">xsd:string</span></span>  <br/> |<span data-ttu-id="248ce-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="248ce-138">optional</span></span>  <br/> |<span data-ttu-id="248ce-139">数式がエラーとして評価されることを示します。</span><span class="sxs-lookup"><span data-stu-id="248ce-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="248ce-140">**E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="248ce-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="248ce-141">エラーメッセージ文字列。</span><span class="sxs-lookup"><span data-stu-id="248ce-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="248ce-142">F</span><span class="sxs-lookup"><span data-stu-id="248ce-142">F</span></span>  <br/> |<span data-ttu-id="248ce-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="248ce-143">xsd:string</span></span>  <br/> |<span data-ttu-id="248ce-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="248ce-144">optional</span></span>  <br/> | <span data-ttu-id="248ce-145">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="248ce-145">Represents the element's formula.</span></span> <span data-ttu-id="248ce-146">この属性には、次のいずれかの文字列を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="248ce-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="248ce-147">' (一部の数式) ' (数式がローカルに存在する場合)</span><span class="sxs-lookup"><span data-stu-id="248ce-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="248ce-148">`No Formula`数式がローカルで削除またはブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="248ce-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="248ce-149">`Inh`数式が継承されている場合。</span><span class="sxs-lookup"><span data-stu-id="248ce-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="248ce-150">数式。</span><span class="sxs-lookup"><span data-stu-id="248ce-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="248ce-151">N</span><span class="sxs-lookup"><span data-stu-id="248ce-151">N</span></span>  <br/> |<span data-ttu-id="248ce-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="248ce-152">xsd:string</span></span>  <br/> |<span data-ttu-id="248ce-153">必須</span><span class="sxs-lookup"><span data-stu-id="248ce-153">required</span></span>  <br/> |<span data-ttu-id="248ce-154">シェイプシートセルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="248ce-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="248ce-155">シェイプシートセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="248ce-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="248ce-156">下記の「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="248ce-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="248ce-157">U</span><span class="sxs-lookup"><span data-stu-id="248ce-157">U</span></span>  <br/> |<span data-ttu-id="248ce-158">xsd: string</span><span class="sxs-lookup"><span data-stu-id="248ce-158">xsd:string</span></span>  <br/> |<span data-ttu-id="248ce-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="248ce-159">optional</span></span>  <br/> |<span data-ttu-id="248ce-160">既定値は DL である計量単位を表します。</span><span class="sxs-lookup"><span data-stu-id="248ce-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="248ce-161">セルの単位を示します。</span><span class="sxs-lookup"><span data-stu-id="248ce-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="248ce-162">V</span><span class="sxs-lookup"><span data-stu-id="248ce-162">V</span></span>  <br/> |<span data-ttu-id="248ce-163">xsd: string</span><span class="sxs-lookup"><span data-stu-id="248ce-163">xsd:string</span></span>  <br/> |<span data-ttu-id="248ce-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="248ce-164">optional</span></span>  <br/> |<span data-ttu-id="248ce-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="248ce-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="248ce-166">シェイプシートセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="248ce-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="248ce-167">注釈</span><span class="sxs-lookup"><span data-stu-id="248ce-167">Remarks</span></span>

<span data-ttu-id="248ce-168">この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="248ce-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="248ce-169">この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="248ce-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="248ce-170">**値**</span><span class="sxs-lookup"><span data-stu-id="248ce-170">**Value**</span></span>|<span data-ttu-id="248ce-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="248ce-171">**Description**</span></span>|<span data-ttu-id="248ce-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="248ce-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="248ce-173">プロンプト</span><span class="sxs-lookup"><span data-stu-id="248ce-173">Prompt</span></span>  <br/> |<span data-ttu-id="248ce-174">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="248ce-174">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |<span data-ttu-id="248ce-175">[[Prompt] セル ([User-Defined Cells] セクション)](prompt-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="248ce-175">[Prompt Cell (User-Defined Cells Section)](prompt-cell-user-defined-cells-section.md)</span></span> <br/> |
|<span data-ttu-id="248ce-176">値</span><span class="sxs-lookup"><span data-stu-id="248ce-176">Value</span></span>  <br/> |<span data-ttu-id="248ce-177">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="248ce-177">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |<span data-ttu-id="248ce-178">[[Value] セル ([User-Defined Cells] セクション)](value-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="248ce-178">[Value Cell (User-Defined Cells Section)](value-cell-user-defined-cells-section.md)</span></span> <br/> |
   

