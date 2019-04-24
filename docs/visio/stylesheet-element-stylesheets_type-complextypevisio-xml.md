---
title: StyleSheet 要素 (StyleSheets_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 図面で定義されているスタイルを表します。
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329800"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="d27ca-103">StyleSheet 要素 (StyleSheets_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d27ca-103">StyleSheet element (StyleSheets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d27ca-104">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="d27ca-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d27ca-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d27ca-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d27ca-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d27ca-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d27ca-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="d27ca-107">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d27ca-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d27ca-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d27ca-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d27ca-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d27ca-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d27ca-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d27ca-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d27ca-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d27ca-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="d27ca-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d27ca-113">定義</span><span class="sxs-lookup"><span data-stu-id="d27ca-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d27ca-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d27ca-114">Elements and attributes</span></span>

<span data-ttu-id="d27ca-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d27ca-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d27ca-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d27ca-116">Parent elements</span></span>

|<span data-ttu-id="d27ca-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d27ca-117">**Element**</span></span>|<span data-ttu-id="d27ca-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d27ca-118">**Type**</span></span>|<span data-ttu-id="d27ca-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d27ca-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d27ca-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="d27ca-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d27ca-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="d27ca-121">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d27ca-122">文書の**StyleSheet**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d27ca-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d27ca-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d27ca-123">Child elements</span></span>

|<span data-ttu-id="d27ca-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d27ca-124">**Element**</span></span>|<span data-ttu-id="d27ca-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d27ca-125">**Type**</span></span>|<span data-ttu-id="d27ca-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d27ca-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d27ca-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d27ca-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="d27ca-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d27ca-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d27ca-129">1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d27ca-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="d27ca-130">Section</span><span class="sxs-lookup"><span data-stu-id="d27ca-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d27ca-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d27ca-131">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d27ca-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d27ca-132">Specifies a collection of related properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d27ca-133">属性</span><span class="sxs-lookup"><span data-stu-id="d27ca-133">Attributes</span></span>

|<span data-ttu-id="d27ca-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="d27ca-134">**Attribute**</span></span>|<span data-ttu-id="d27ca-135">**型**</span><span class="sxs-lookup"><span data-stu-id="d27ca-135">**Type**</span></span>|<span data-ttu-id="d27ca-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="d27ca-136">**Required**</span></span>|<span data-ttu-id="d27ca-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="d27ca-137">**Description**</span></span>|<span data-ttu-id="d27ca-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d27ca-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d27ca-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="d27ca-139">FillStyle</span></span>  <br/> |<span data-ttu-id="d27ca-140">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d27ca-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d27ca-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-141">optional</span></span>  <br/> |<span data-ttu-id="d27ca-142">このスタイルが塗りつぶしの書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d27ca-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="d27ca-143">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-144">ID</span><span class="sxs-lookup"><span data-stu-id="d27ca-144">ID</span></span>  <br/> |<span data-ttu-id="d27ca-145">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d27ca-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d27ca-146">必須</span><span class="sxs-lookup"><span data-stu-id="d27ca-146">required</span></span>  <br/> |<span data-ttu-id="d27ca-147">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d27ca-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="d27ca-148">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-149">iscustomname</span><span class="sxs-lookup"><span data-stu-id="d27ca-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="d27ca-150">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d27ca-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d27ca-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-151">optional</span></span>  <br/> |<span data-ttu-id="d27ca-152">ユーザーによって名前がカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d27ca-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="d27ca-153">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d27ca-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d27ca-155">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d27ca-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d27ca-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-156">optional</span></span>  <br/> |<span data-ttu-id="d27ca-157">ユーザーが汎用名をカスタマイズしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d27ca-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="d27ca-158">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="d27ca-159">LineStyle</span></span>  <br/> |<span data-ttu-id="d27ca-160">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d27ca-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d27ca-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-161">optional</span></span>  <br/> |<span data-ttu-id="d27ca-162">このスタイルが行の書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d27ca-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="d27ca-163">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-164">名前</span><span class="sxs-lookup"><span data-stu-id="d27ca-164">Name</span></span>  <br/> |<span data-ttu-id="d27ca-165">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d27ca-165">xsd:string</span></span>  <br/> |<span data-ttu-id="d27ca-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-166">optional</span></span>  <br/> |<span data-ttu-id="d27ca-167">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="d27ca-167">The name of the element.</span></span>  <br/> |<span data-ttu-id="d27ca-168">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-169">NameU</span><span class="sxs-lookup"><span data-stu-id="d27ca-169">NameU</span></span>  <br/> |<span data-ttu-id="d27ca-170">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d27ca-170">xsd:string</span></span>  <br/> |<span data-ttu-id="d27ca-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-171">optional</span></span>  <br/> |<span data-ttu-id="d27ca-172">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="d27ca-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="d27ca-173">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d27ca-174">TextStyle</span><span class="sxs-lookup"><span data-stu-id="d27ca-174">TextStyle</span></span>  <br/> |<span data-ttu-id="d27ca-175">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d27ca-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d27ca-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="d27ca-176">optional</span></span>  <br/> |<span data-ttu-id="d27ca-177">このスタイルがテキストの書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d27ca-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="d27ca-178">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d27ca-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

