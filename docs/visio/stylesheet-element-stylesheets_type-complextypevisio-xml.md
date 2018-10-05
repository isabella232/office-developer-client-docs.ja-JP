---
title: スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 図面で定義されているスタイルを表します。
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384571"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="67af4-103">スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="67af4-103">StyleSheet element (StyleSheets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67af4-104">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="67af4-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67af4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="67af4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67af4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="67af4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67af4-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="67af4-107">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67af4-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="67af4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67af4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="67af4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67af4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67af4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67af4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="67af4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67af4-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="67af4-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67af4-113">定義</span><span class="sxs-lookup"><span data-stu-id="67af4-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67af4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="67af4-114">Elements and attributes</span></span>

<span data-ttu-id="67af4-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="67af4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67af4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="67af4-116">Parent elements</span></span>

|<span data-ttu-id="67af4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="67af4-117">**Element**</span></span>|<span data-ttu-id="67af4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="67af4-118">**Type**</span></span>|<span data-ttu-id="67af4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="67af4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67af4-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="67af4-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67af4-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="67af4-121">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67af4-122">ドキュメントの**スタイル シート**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67af4-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67af4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="67af4-123">Child elements</span></span>

|<span data-ttu-id="67af4-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="67af4-124">**Element**</span></span>|<span data-ttu-id="67af4-125">**型**</span><span class="sxs-lookup"><span data-stu-id="67af4-125">**Type**</span></span>|<span data-ttu-id="67af4-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="67af4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67af4-127">Cell</span><span class="sxs-lookup"><span data-stu-id="67af4-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="67af4-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="67af4-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67af4-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="67af4-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="67af4-130">セクション</span><span class="sxs-lookup"><span data-stu-id="67af4-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67af4-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="67af4-131">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67af4-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="67af4-132">Specifies a collection of related properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="67af4-133">属性</span><span class="sxs-lookup"><span data-stu-id="67af4-133">Attributes</span></span>

|<span data-ttu-id="67af4-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="67af4-134">**Attribute**</span></span>|<span data-ttu-id="67af4-135">**型**</span><span class="sxs-lookup"><span data-stu-id="67af4-135">**Type**</span></span>|<span data-ttu-id="67af4-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="67af4-136">**Required**</span></span>|<span data-ttu-id="67af4-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="67af4-137">**Description**</span></span>|<span data-ttu-id="67af4-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="67af4-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67af4-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="67af4-139">FillStyle</span></span>  <br/> |<span data-ttu-id="67af4-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67af4-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67af4-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-141">optional</span></span>  <br/> |<span data-ttu-id="67af4-142">このスタイルを継承する塗りつぶしの書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="67af4-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="67af4-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67af4-144">ID</span><span class="sxs-lookup"><span data-stu-id="67af4-144">ID</span></span>  <br/> |<span data-ttu-id="67af4-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67af4-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67af4-146">必須</span><span class="sxs-lookup"><span data-stu-id="67af4-146">required</span></span>  <br/> |<span data-ttu-id="67af4-147">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="67af4-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="67af4-148">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67af4-149">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="67af4-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="67af4-150">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="67af4-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67af4-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-151">optional</span></span>  <br/> |<span data-ttu-id="67af4-152">名前がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="67af4-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="67af4-153">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67af4-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="67af4-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="67af4-155">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="67af4-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67af4-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-156">optional</span></span>  <br/> |<span data-ttu-id="67af4-157">汎用名がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="67af4-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="67af4-158">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67af4-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="67af4-159">LineStyle</span></span>  <br/> |<span data-ttu-id="67af4-160">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67af4-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67af4-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-161">optional</span></span>  <br/> |<span data-ttu-id="67af4-162">このスタイルが継承している行の書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="67af4-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="67af4-163">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67af4-164">名前</span><span class="sxs-lookup"><span data-stu-id="67af4-164">Name</span></span>  <br/> |<span data-ttu-id="67af4-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="67af4-165">xsd:string</span></span>  <br/> |<span data-ttu-id="67af4-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-166">optional</span></span>  <br/> |<span data-ttu-id="67af4-167">要素の名前です。</span><span class="sxs-lookup"><span data-stu-id="67af4-167">The name of the element.</span></span>  <br/> |<span data-ttu-id="67af4-168">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67af4-169">NameU</span><span class="sxs-lookup"><span data-stu-id="67af4-169">NameU</span></span>  <br/> |<span data-ttu-id="67af4-170">xsd:string</span><span class="sxs-lookup"><span data-stu-id="67af4-170">xsd:string</span></span>  <br/> |<span data-ttu-id="67af4-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-171">optional</span></span>  <br/> |<span data-ttu-id="67af4-172">要素の汎用名です。</span><span class="sxs-lookup"><span data-stu-id="67af4-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="67af4-173">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67af4-174">TextStyle</span><span class="sxs-lookup"><span data-stu-id="67af4-174">TextStyle</span></span>  <br/> |<span data-ttu-id="67af4-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67af4-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67af4-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="67af4-176">optional</span></span>  <br/> |<span data-ttu-id="67af4-177">このスタイルを継承するテキストの書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="67af4-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="67af4-178">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67af4-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

