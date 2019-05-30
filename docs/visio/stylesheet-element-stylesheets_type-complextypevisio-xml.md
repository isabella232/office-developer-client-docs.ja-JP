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
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="6b507-103">StyleSheet 要素 (StyleSheets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6b507-103">StyleSheet element (StyleSheets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6b507-104">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="6b507-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b507-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6b507-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b507-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6b507-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b507-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6b507-107">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b507-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6b507-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b507-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6b507-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b507-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="6b507-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b507-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6b507-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b507-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="6b507-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b507-113">定義</span><span class="sxs-lookup"><span data-stu-id="6b507-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b507-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6b507-114">Elements and attributes</span></span>

<span data-ttu-id="6b507-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b507-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b507-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6b507-116">Parent elements</span></span>

|<span data-ttu-id="6b507-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6b507-117">**Element**</span></span>|<span data-ttu-id="6b507-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6b507-118">**Type**</span></span>|<span data-ttu-id="6b507-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b507-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b507-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="6b507-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b507-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="6b507-121">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b507-122">文書の**StyleSheet**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6b507-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b507-123">子要素</span><span class="sxs-lookup"><span data-stu-id="6b507-123">Child elements</span></span>

|<span data-ttu-id="6b507-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="6b507-124">**Element**</span></span>|<span data-ttu-id="6b507-125">**型**</span><span class="sxs-lookup"><span data-stu-id="6b507-125">**Type**</span></span>|<span data-ttu-id="6b507-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b507-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b507-127">Cell</span><span class="sxs-lookup"><span data-stu-id="6b507-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="6b507-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="6b507-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b507-129">1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b507-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="6b507-130">Section</span><span class="sxs-lookup"><span data-stu-id="6b507-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b507-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="6b507-131">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b507-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b507-132">Specifies a collection of related properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6b507-133">属性</span><span class="sxs-lookup"><span data-stu-id="6b507-133">Attributes</span></span>

|<span data-ttu-id="6b507-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="6b507-134">**Attribute**</span></span>|<span data-ttu-id="6b507-135">**型**</span><span class="sxs-lookup"><span data-stu-id="6b507-135">**Type**</span></span>|<span data-ttu-id="6b507-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="6b507-136">**Required**</span></span>|<span data-ttu-id="6b507-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b507-137">**Description**</span></span>|<span data-ttu-id="6b507-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="6b507-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b507-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="6b507-139">FillStyle</span></span>  <br/> |<span data-ttu-id="6b507-140">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="6b507-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b507-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-141">optional</span></span>  <br/> |<span data-ttu-id="6b507-142">このスタイルが塗りつぶしの書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="6b507-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="6b507-143">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b507-144">ID</span><span class="sxs-lookup"><span data-stu-id="6b507-144">ID</span></span>  <br/> |<span data-ttu-id="6b507-145">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="6b507-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b507-146">必須</span><span class="sxs-lookup"><span data-stu-id="6b507-146">required</span></span>  <br/> |<span data-ttu-id="6b507-147">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="6b507-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="6b507-148">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b507-149">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="6b507-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="6b507-150">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="6b507-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6b507-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-151">optional</span></span>  <br/> |<span data-ttu-id="6b507-152">ユーザーによって名前がカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6b507-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="6b507-153">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6b507-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="6b507-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="6b507-155">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="6b507-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6b507-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-156">optional</span></span>  <br/> |<span data-ttu-id="6b507-157">ユーザーが汎用名をカスタマイズしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6b507-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="6b507-158">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6b507-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="6b507-159">LineStyle</span></span>  <br/> |<span data-ttu-id="6b507-160">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="6b507-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b507-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-161">optional</span></span>  <br/> |<span data-ttu-id="6b507-162">このスタイルが行の書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="6b507-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="6b507-163">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b507-164">名前</span><span class="sxs-lookup"><span data-stu-id="6b507-164">Name</span></span>  <br/> |<span data-ttu-id="6b507-165">xsd: string</span><span class="sxs-lookup"><span data-stu-id="6b507-165">xsd:string</span></span>  <br/> |<span data-ttu-id="6b507-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-166">optional</span></span>  <br/> |<span data-ttu-id="6b507-167">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="6b507-167">The name of the element.</span></span>  <br/> |<span data-ttu-id="6b507-168">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b507-169">NameU</span><span class="sxs-lookup"><span data-stu-id="6b507-169">NameU</span></span>  <br/> |<span data-ttu-id="6b507-170">xsd: string</span><span class="sxs-lookup"><span data-stu-id="6b507-170">xsd:string</span></span>  <br/> |<span data-ttu-id="6b507-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-171">optional</span></span>  <br/> |<span data-ttu-id="6b507-172">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="6b507-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="6b507-173">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b507-174">TextStyle</span><span class="sxs-lookup"><span data-stu-id="6b507-174">TextStyle</span></span>  <br/> |<span data-ttu-id="6b507-175">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="6b507-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b507-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b507-176">optional</span></span>  <br/> |<span data-ttu-id="6b507-177">このスタイルがテキストの書式設定を継承する StyleSheet 要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="6b507-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="6b507-178">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="6b507-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

