---
title: セル要素 (ユーザー定義セル-部分) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ab7a11a0-a413-d4fe-ddf1-0d2e967dc21d
description: 1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。
ms.openlocfilehash: 40555c58e6afdb3eefe5b1a14d4155ad4e57ed6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804975"
---
# <a name="cell-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="d32e6-103">セル要素 (ユーザー定義セル-部分) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d32e6-103">Cell element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="d32e6-104">1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。</span><span class="sxs-lookup"><span data-stu-id="d32e6-104">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d32e6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d32e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d32e6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d32e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d32e6-107">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d32e6-107">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d32e6-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d32e6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d32e6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d32e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d32e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d32e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d32e6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d32e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d32e6-112">document.xml、masters.xml、マスターの # .xml、pages.xml ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="d32e6-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d32e6-113">定義</span><span class="sxs-lookup"><span data-stu-id="d32e6-113">Definition</span></span>

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d32e6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d32e6-114">Elements and attributes</span></span>

<span data-ttu-id="d32e6-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d32e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d32e6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d32e6-116">Parent elements</span></span>

|<span data-ttu-id="d32e6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d32e6-117">**Element**</span></span>|<span data-ttu-id="d32e6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d32e6-118">**Type**</span></span>|<span data-ttu-id="d32e6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d32e6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d32e6-120">[Row 要素 ([ユーザー定義セル] セクション)](row-element-user-defined-cells-sectionvisio-xml.md)</span><span class="sxs-lookup"><span data-stu-id="d32e6-120">[Row element (User-defined Cells Section)](row-element-user-defined-cells-sectionvisio-xml.md)</span></span> <br/> |[<span data-ttu-id="d32e6-121">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="d32e6-121">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d32e6-122">1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。</span><span class="sxs-lookup"><span data-stu-id="d32e6-122">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d32e6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d32e6-123">Child elements</span></span>

|<span data-ttu-id="d32e6-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="d32e6-124">**Element**</span></span>|<span data-ttu-id="d32e6-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d32e6-125">**Type**</span></span>|<span data-ttu-id="d32e6-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d32e6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d32e6-127">RefBy</span><span class="sxs-lookup"><span data-stu-id="d32e6-127">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d32e6-128">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="d32e6-128">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d32e6-129">図面ページへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-129">Specifies a reference to a drawing page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d32e6-130">属性</span><span class="sxs-lookup"><span data-stu-id="d32e6-130">Attributes</span></span>

|<span data-ttu-id="d32e6-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="d32e6-131">**Attribute**</span></span>|<span data-ttu-id="d32e6-132">**型**</span><span class="sxs-lookup"><span data-stu-id="d32e6-132">**Type**</span></span>|<span data-ttu-id="d32e6-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="d32e6-133">**Required**</span></span>|<span data-ttu-id="d32e6-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="d32e6-134">**Description**</span></span>|<span data-ttu-id="d32e6-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d32e6-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d32e6-136">E</span><span class="sxs-lookup"><span data-stu-id="d32e6-136">E</span></span>  <br/> |<span data-ttu-id="d32e6-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d32e6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d32e6-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d32e6-138">optional</span></span>  <br/> |<span data-ttu-id="d32e6-139">数式がエラーが発生することを示します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-139">Indicates that the formula evaluates to an error.</span></span> <span data-ttu-id="d32e6-140">**E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-140">The value of **E** is the current value (an error message string); the value of the **V** attribute is the last valid value.</span></span>  <br/> |<span data-ttu-id="d32e6-141">エラー メッセージの文字列です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-141">An error message string.</span></span>  <br/> |
|<span data-ttu-id="d32e6-142">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="d32e6-142">F</span></span>  <br/> |<span data-ttu-id="d32e6-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d32e6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="d32e6-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="d32e6-144">optional</span></span>  <br/> | <span data-ttu-id="d32e6-145">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-145">Represents the element's formula.</span></span> <span data-ttu-id="d32e6-146">この属性は、次の文字列のいずれかを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d32e6-146">This attribute can contain one of the following strings:</span></span>  <br/>  <span data-ttu-id="d32e6-147">'(いくつかの数式)' の数式がローカルに存在する場合</span><span class="sxs-lookup"><span data-stu-id="d32e6-147">'(some formula)' if the formula exists locally</span></span>  <br/>  <span data-ttu-id="d32e6-148">`No Formula`数式がローカルで削除されるか、ブロックされている場合</span><span class="sxs-lookup"><span data-stu-id="d32e6-148">`No Formula` if the formula is locally deleted or blocked</span></span>  <br/>  <span data-ttu-id="d32e6-149">`Inh`場合は、数式が継承されます。</span><span class="sxs-lookup"><span data-stu-id="d32e6-149">`Inh` if the formula is inherited.</span></span>  <br/> |<span data-ttu-id="d32e6-150">数式です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-150">A formula.</span></span>  <br/> |
|<span data-ttu-id="d32e6-151">N</span><span class="sxs-lookup"><span data-stu-id="d32e6-151">N</span></span>  <br/> |<span data-ttu-id="d32e6-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d32e6-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d32e6-153">必須</span><span class="sxs-lookup"><span data-stu-id="d32e6-153">required</span></span>  <br/> |<span data-ttu-id="d32e6-154">シェイプ シート セルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-154">Represents the name of the ShapeSheet cell.</span></span>  <br/> |<span data-ttu-id="d32e6-155">シェイプ シート セルの名前です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-155">The name of the ShapeSheet cell.</span></span>  <br/> <span data-ttu-id="d32e6-156">以下の「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d32e6-156">See the Remarks section below.</span></span>  <br/> |
|<span data-ttu-id="d32e6-157">U</span><span class="sxs-lookup"><span data-stu-id="d32e6-157">U</span></span>  <br/> |<span data-ttu-id="d32e6-158">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d32e6-158">xsd:string</span></span>  <br/> |<span data-ttu-id="d32e6-159">省略可能</span><span class="sxs-lookup"><span data-stu-id="d32e6-159">optional</span></span>  <br/> |<span data-ttu-id="d32e6-160">既定の測定単位を表しますが、DL です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-160">Represents a unit of measure The default is DL.</span></span>  <br/> |<span data-ttu-id="d32e6-161">セルの単位です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-161">The units of the cell.</span></span>  <br/> |
|<span data-ttu-id="d32e6-162">V</span><span class="sxs-lookup"><span data-stu-id="d32e6-162">V</span></span>  <br/> |<span data-ttu-id="d32e6-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d32e6-163">xsd:string</span></span>  <br/> |<span data-ttu-id="d32e6-164">省略可能</span><span class="sxs-lookup"><span data-stu-id="d32e6-164">optional</span></span>  <br/> |<span data-ttu-id="d32e6-165">セルの値を表します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-165">Represents the value of the cell.</span></span>  <br/> |<span data-ttu-id="d32e6-166">シェイプ シート セルの値です。</span><span class="sxs-lookup"><span data-stu-id="d32e6-166">The value of the ShapeSheet cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d32e6-167">注釈</span><span class="sxs-lookup"><span data-stu-id="d32e6-167">Remarks</span></span>

<span data-ttu-id="d32e6-168">この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d32e6-168">The **N** attribute of this **Cell** element must be one of a limited set of values that correspond to ShapeSheet cells.</span></span> <span data-ttu-id="d32e6-169">この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d32e6-169">Refer to the table below to determine the values of the **N** attribute that are permitted for this **Cell** element.</span></span> 
  
|<span data-ttu-id="d32e6-170">**値**</span><span class="sxs-lookup"><span data-stu-id="d32e6-170">**Value**</span></span>|<span data-ttu-id="d32e6-171">**説明**</span><span class="sxs-lookup"><span data-stu-id="d32e6-171">**Description**</span></span>|<span data-ttu-id="d32e6-172">**詳細情報**</span><span class="sxs-lookup"><span data-stu-id="d32e6-172">**More information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d32e6-173">プロンプト</span><span class="sxs-lookup"><span data-stu-id="d32e6-173">Prompt</span></span>  <br/> |<span data-ttu-id="d32e6-174">ユーザー定義のセルに関する説明プロンプトまたはコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-174">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |<span data-ttu-id="d32e6-175">[[Prompt] セル ([User-Defined Cells] セクション)](prompt-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="d32e6-175">[Prompt Cell (User-Defined Cells Section)](prompt-cell-user-defined-cells-section.md)</span></span> <br/> |
|<span data-ttu-id="d32e6-176">値</span><span class="sxs-lookup"><span data-stu-id="d32e6-176">Value</span></span>  <br/> |<span data-ttu-id="d32e6-177">対応するユーザー定義のセルの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d32e6-177">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |<span data-ttu-id="d32e6-178">[[Value] セル ([User-Defined Cells] セクション)](value-cell-user-defined-cells-section.md)</span><span class="sxs-lookup"><span data-stu-id="d32e6-178">[Value Cell (User-Defined Cells Section)](value-cell-user-defined-cells-section.md)</span></span> <br/> |
   

