---
title: StyleSheet 要素 (StyleSheets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 図面で定義されているスタイルを表します。
ms.openlocfilehash: 939180d24972ae68d01b2a707e7806380b706d14
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541940"
---
# <a name="stylesheet-element-stylesheets_type-complextype-visio-xml"></a><span data-ttu-id="29312-103">StyleSheet 要素 (StyleSheets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="29312-103">StyleSheet element (StyleSheets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="29312-104">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="29312-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29312-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="29312-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29312-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="29312-106">**Element type**</span></span> <br/> |[<span data-ttu-id="29312-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="29312-107">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="29312-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="29312-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="29312-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="29312-109">**Schema file**</span></span> <br/> |<span data-ttu-id="29312-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="29312-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="29312-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="29312-111">**Document parts**</span></span> <br/> |<span data-ttu-id="29312-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="29312-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="29312-113">定義</span><span class="sxs-lookup"><span data-stu-id="29312-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="29312-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="29312-114">Elements and attributes</span></span>

<span data-ttu-id="29312-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="29312-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="29312-116">親要素</span><span class="sxs-lookup"><span data-stu-id="29312-116">Parent elements</span></span>

|<span data-ttu-id="29312-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="29312-117">**Element**</span></span>|<span data-ttu-id="29312-118">**型**</span><span class="sxs-lookup"><span data-stu-id="29312-118">**Type**</span></span>|<span data-ttu-id="29312-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="29312-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29312-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="29312-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29312-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="29312-121">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29312-122">ドキュメントの **StyleSheet 要素の** コレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="29312-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="29312-123">子要素</span><span class="sxs-lookup"><span data-stu-id="29312-123">Child elements</span></span>

|<span data-ttu-id="29312-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="29312-124">**Element**</span></span>|<span data-ttu-id="29312-125">**型**</span><span class="sxs-lookup"><span data-stu-id="29312-125">**Type**</span></span>|<span data-ttu-id="29312-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="29312-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="29312-127">Cell</span><span class="sxs-lookup"><span data-stu-id="29312-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="29312-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="29312-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29312-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="29312-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="29312-130">Section</span><span class="sxs-lookup"><span data-stu-id="29312-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="29312-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="29312-131">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="29312-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="29312-132">Specifies a collection of related properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="29312-133">属性</span><span class="sxs-lookup"><span data-stu-id="29312-133">Attributes</span></span>

|<span data-ttu-id="29312-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="29312-134">**Attribute**</span></span>|<span data-ttu-id="29312-135">**型**</span><span class="sxs-lookup"><span data-stu-id="29312-135">**Type**</span></span>|<span data-ttu-id="29312-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="29312-136">**Required**</span></span>|<span data-ttu-id="29312-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="29312-137">**Description**</span></span>|<span data-ttu-id="29312-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="29312-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="29312-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="29312-139">FillStyle</span></span>  <br/> |<span data-ttu-id="29312-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29312-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29312-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-141">optional</span></span>  <br/> |<span data-ttu-id="29312-142">このスタイルが塗りつぶしの書式を継承する StyleSheet 要素の ID。</span><span class="sxs-lookup"><span data-stu-id="29312-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="29312-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29312-144">ID</span><span class="sxs-lookup"><span data-stu-id="29312-144">ID</span></span>  <br/> |<span data-ttu-id="29312-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29312-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29312-146">必須</span><span class="sxs-lookup"><span data-stu-id="29312-146">required</span></span>  <br/> |<span data-ttu-id="29312-147">親要素内の要素の一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="29312-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="29312-148">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29312-149">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="29312-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="29312-150">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="29312-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29312-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-151">optional</span></span>  <br/> |<span data-ttu-id="29312-152">名前がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29312-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="29312-153">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29312-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="29312-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="29312-155">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="29312-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="29312-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-156">optional</span></span>  <br/> |<span data-ttu-id="29312-157">ユニバーサル名がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29312-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="29312-158">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="29312-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="29312-159">LineStyle</span></span>  <br/> |<span data-ttu-id="29312-160">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29312-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29312-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-161">optional</span></span>  <br/> |<span data-ttu-id="29312-162">このスタイルが線の書式設定を継承する StyleSheet 要素の ID。</span><span class="sxs-lookup"><span data-stu-id="29312-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="29312-163">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="29312-164">名前</span><span class="sxs-lookup"><span data-stu-id="29312-164">Name</span></span>  <br/> |<span data-ttu-id="29312-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="29312-165">xsd:string</span></span>  <br/> |<span data-ttu-id="29312-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-166">optional</span></span>  <br/> |<span data-ttu-id="29312-167">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="29312-167">The name of the element.</span></span>  <br/> |<span data-ttu-id="29312-168">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29312-169">NameU</span><span class="sxs-lookup"><span data-stu-id="29312-169">NameU</span></span>  <br/> |<span data-ttu-id="29312-170">xsd:string</span><span class="sxs-lookup"><span data-stu-id="29312-170">xsd:string</span></span>  <br/> |<span data-ttu-id="29312-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-171">optional</span></span>  <br/> |<span data-ttu-id="29312-172">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="29312-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="29312-173">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="29312-174">TextStyle</span><span class="sxs-lookup"><span data-stu-id="29312-174">TextStyle</span></span>  <br/> |<span data-ttu-id="29312-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="29312-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="29312-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="29312-176">optional</span></span>  <br/> |<span data-ttu-id="29312-177">このスタイルがテキストの書式設定を継承する StyleSheet 要素の ID。</span><span class="sxs-lookup"><span data-stu-id="29312-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="29312-178">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="29312-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

