---
title: スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: 図面で定義されているスタイルを表します。
ms.openlocfilehash: 2513c7421dc8f890b7ba63f19cf3d31d23ce65ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806594"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a><span data-ttu-id="d4071-103">スタイル シートの要素 (StyleSheets_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d4071-103">StyleSheet element (StyleSheets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d4071-104">図面で定義されているスタイルを表します。</span><span class="sxs-lookup"><span data-stu-id="d4071-104">Represents a style defined in a document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4071-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d4071-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4071-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="d4071-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d4071-107">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="d4071-107">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d4071-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d4071-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d4071-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d4071-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d4071-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d4071-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d4071-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d4071-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d4071-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="d4071-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d4071-113">定義</span><span class="sxs-lookup"><span data-stu-id="d4071-113">Definition</span></span>

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d4071-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d4071-114">Elements and attributes</span></span>

<span data-ttu-id="d4071-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4071-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d4071-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d4071-116">Parent elements</span></span>

|<span data-ttu-id="d4071-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d4071-117">**Element**</span></span>|<span data-ttu-id="d4071-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d4071-118">**Type**</span></span>|<span data-ttu-id="d4071-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4071-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4071-120">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="d4071-120">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4071-121">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="d4071-121">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d4071-122">ドキュメントの**スタイル シート**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4071-122">Contains a collection of **StyleSheet** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d4071-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d4071-123">Child elements</span></span>

|<span data-ttu-id="d4071-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="d4071-124">**Element**</span></span>|<span data-ttu-id="d4071-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d4071-125">**Type**</span></span>|<span data-ttu-id="d4071-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4071-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d4071-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d4071-127">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="d4071-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d4071-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d4071-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4071-129">Specifies a single property.</span></span>  <br/> |
|[<span data-ttu-id="d4071-130">Section</span><span class="sxs-lookup"><span data-stu-id="d4071-130">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d4071-131">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d4071-131">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d4071-132">関連するプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4071-132">Specifies a collection of related properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d4071-133">属性</span><span class="sxs-lookup"><span data-stu-id="d4071-133">Attributes</span></span>

|<span data-ttu-id="d4071-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="d4071-134">**Attribute**</span></span>|<span data-ttu-id="d4071-135">**型**</span><span class="sxs-lookup"><span data-stu-id="d4071-135">**Type**</span></span>|<span data-ttu-id="d4071-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="d4071-136">**Required**</span></span>|<span data-ttu-id="d4071-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4071-137">**Description**</span></span>|<span data-ttu-id="d4071-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d4071-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d4071-139">FillStyle</span><span class="sxs-lookup"><span data-stu-id="d4071-139">FillStyle</span></span>  <br/> |<span data-ttu-id="d4071-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4071-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4071-141">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-141">optional</span></span>  <br/> |<span data-ttu-id="d4071-142">このスタイルを継承する塗りつぶしの書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d4071-142">The ID of the StyleSheet element from which this style inherits fill formatting.</span></span>  <br/> |<span data-ttu-id="d4071-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d4071-144">ID</span><span class="sxs-lookup"><span data-stu-id="d4071-144">ID</span></span>  <br/> |<span data-ttu-id="d4071-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4071-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4071-146">必須</span><span class="sxs-lookup"><span data-stu-id="d4071-146">required</span></span>  <br/> |<span data-ttu-id="d4071-147">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d4071-147">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="d4071-148">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d4071-149">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d4071-149">IsCustomName</span></span>  <br/> |<span data-ttu-id="d4071-150">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d4071-150">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d4071-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-151">optional</span></span>  <br/> |<span data-ttu-id="d4071-152">名前がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d4071-152">Indicates whether the name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="d4071-153">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-153">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d4071-154">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d4071-154">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d4071-155">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d4071-155">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d4071-156">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-156">optional</span></span>  <br/> |<span data-ttu-id="d4071-157">汎用名がユーザーによってカスタマイズされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d4071-157">Indicates whether the universal name has been customized by the user.</span></span>  <br/> |<span data-ttu-id="d4071-158">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-158">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d4071-159">LineStyle</span><span class="sxs-lookup"><span data-stu-id="d4071-159">LineStyle</span></span>  <br/> |<span data-ttu-id="d4071-160">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4071-160">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4071-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-161">optional</span></span>  <br/> |<span data-ttu-id="d4071-162">このスタイルが継承している行の書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d4071-162">The ID of the StyleSheet element from which this style inherits line formatting.</span></span>  <br/> |<span data-ttu-id="d4071-163">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d4071-164">名前</span><span class="sxs-lookup"><span data-stu-id="d4071-164">Name</span></span>  <br/> |<span data-ttu-id="d4071-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d4071-165">xsd:string</span></span>  <br/> |<span data-ttu-id="d4071-166">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-166">optional</span></span>  <br/> |<span data-ttu-id="d4071-167">要素の名前です。</span><span class="sxs-lookup"><span data-stu-id="d4071-167">The name of the element.</span></span>  <br/> |<span data-ttu-id="d4071-168">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-168">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d4071-169">NameU</span><span class="sxs-lookup"><span data-stu-id="d4071-169">NameU</span></span>  <br/> |<span data-ttu-id="d4071-170">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d4071-170">xsd:string</span></span>  <br/> |<span data-ttu-id="d4071-171">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-171">optional</span></span>  <br/> |<span data-ttu-id="d4071-172">要素の汎用名です。</span><span class="sxs-lookup"><span data-stu-id="d4071-172">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="d4071-173">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-173">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d4071-174">テキスト スタイル</span><span class="sxs-lookup"><span data-stu-id="d4071-174">TextStyle</span></span>  <br/> |<span data-ttu-id="d4071-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d4071-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d4071-176">省略可能</span><span class="sxs-lookup"><span data-stu-id="d4071-176">optional</span></span>  <br/> |<span data-ttu-id="d4071-177">このスタイルを継承するテキストの書式設定スタイル シートの要素の ID です。</span><span class="sxs-lookup"><span data-stu-id="d4071-177">The ID of the StyleSheet element from which this style inherits text formatting.</span></span>  <br/> |<span data-ttu-id="d4071-178">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4071-178">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

