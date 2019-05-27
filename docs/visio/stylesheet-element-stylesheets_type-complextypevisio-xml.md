---
title: StyleSheet 要素 (StyleSheets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 文書内で定義されたスタイルを表します。
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329800"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="a3c47-103">StyleSheet 要素 (StyleSheets_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a3c47-103">StyleSheet element (StyleSheets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a3c47-104">文書内で定義されたスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="a3c47-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3c47-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a3c47-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3c47-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a3c47-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a3c47-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a3c47-107">StyleSheet_Type complexType</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3c47-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a3c47-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3c47-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a3c47-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a3c47-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a3c47-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3c47-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a3c47-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="a3c47-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="a3c47-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3c47-113">定義</span><span class="sxs-lookup"><span data-stu-id="a3c47-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3c47-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a3c47-114">Elements and attributes</span></span>

<span data-ttu-id="a3c47-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c47-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3c47-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a3c47-116">Parent elements</span></span>

|<span data-ttu-id="a3c47-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a3c47-117">**Element**</span></span>|<span data-ttu-id="a3c47-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a3c47-118">**Type**</span></span>|<span data-ttu-id="a3c47-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3c47-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3c47-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="a3c47-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3c47-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="a3c47-121">StyleSheets_Type complexType</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3c47-122">ドキュメントの **StyleSheet** 要素のコレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3c47-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3c47-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a3c47-123">Child elements</span></span>

|<span data-ttu-id="a3c47-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3c47-124">**Element**</span></span>|<span data-ttu-id="a3c47-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a3c47-125">**Type**</span></span>|<span data-ttu-id="a3c47-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3c47-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3c47-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a3c47-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="a3c47-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a3c47-128">Cell_Type complexType</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3c47-129">1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a3c47-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="a3c47-130">セクション</span><span class="sxs-lookup"><span data-stu-id="a3c47-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3c47-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a3c47-131">Section_Type complexType</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3c47-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="a3c47-132">Specifies a collection of managed properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a3c47-133">属性</span><span class="sxs-lookup"><span data-stu-id="a3c47-133">Attributes</span></span>

|<span data-ttu-id="a3c47-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="a3c47-134">**Attribute**</span></span>|<span data-ttu-id="a3c47-135">**型**</span><span class="sxs-lookup"><span data-stu-id="a3c47-135">**Type**</span></span>|<span data-ttu-id="a3c47-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="a3c47-136">**Required**</span></span>|<span data-ttu-id="a3c47-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3c47-137">**Description**</span></span>|<span data-ttu-id="a3c47-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a3c47-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a3c47-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="a3c47-139">FillStyle</span></span>  <br/> |<span data-ttu-id="a3c47-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3c47-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3c47-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-141">optional</span></span>  <br/> |<span data-ttu-id="a3c47-142">このスタイルが塗りつぶし書式を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="a3c47-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="a3c47-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-144">ID</span><span class="sxs-lookup"><span data-stu-id="a3c47-144">ID</span></span>  <br/> |<span data-ttu-id="a3c47-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3c47-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3c47-146">必須</span><span class="sxs-lookup"><span data-stu-id="a3c47-146">required</span></span>  <br/> |<span data-ttu-id="a3c47-147">親要素内の要素の一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="a3c47-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="a3c47-148">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-149">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a3c47-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="a3c47-150">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a3c47-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a3c47-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-151">optional</span></span>  <br/> |<span data-ttu-id="a3c47-152">ユーザーが名前をカスタマイズしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a3c47-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a3c47-153">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a3c47-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a3c47-155">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a3c47-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a3c47-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-156">optional</span></span>  <br/> |<span data-ttu-id="a3c47-157">ユーザーが汎用名をカスタマイズしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a3c47-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="a3c47-158">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="a3c47-159">LineStyle</span></span>  <br/> |<span data-ttu-id="a3c47-160">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3c47-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3c47-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-161">optional</span></span>  <br/> |<span data-ttu-id="a3c47-162">このスタイルが行書式を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="a3c47-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="a3c47-163">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-164">名前</span><span class="sxs-lookup"><span data-stu-id="a3c47-164">Name</span></span>  <br/> |<span data-ttu-id="a3c47-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3c47-165">xsd:string</span></span>  <br/> |<span data-ttu-id="a3c47-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-166">optional</span></span>  <br/> |<span data-ttu-id="a3c47-167">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="a3c47-167">The name of the root element.</span></span>  <br/> |<span data-ttu-id="a3c47-168">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-169">NameU</span><span class="sxs-lookup"><span data-stu-id="a3c47-169">NameU</span></span>  <br/> |<span data-ttu-id="a3c47-170">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a3c47-170">xsd:string</span></span>  <br/> |<span data-ttu-id="a3c47-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-171">optional</span></span>  <br/> |<span data-ttu-id="a3c47-172">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="a3c47-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="a3c47-173">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a3c47-174">TextStyle</span><span class="sxs-lookup"><span data-stu-id="a3c47-174">TextStyle</span></span>  <br/> |<span data-ttu-id="a3c47-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a3c47-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a3c47-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="a3c47-176">optional</span></span>  <br/> |<span data-ttu-id="a3c47-177">このスタイルがテキスト形式を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="a3c47-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="a3c47-178">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a3c47-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

