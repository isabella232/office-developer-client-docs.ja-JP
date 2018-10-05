---
title: 行要素 (ハイパーリンクを参照) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: 図形間の複数のジャンプを作成するか、図面のページと別の図面ページ、別のファイル、または web サイトの要素が含まれています。
ms.openlocfilehash: 16935e463e76e0f0ee72b3fa40964551cf125cdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400034"
---
# <a name="row-element-hyperlink-section-visio-xml"></a><span data-ttu-id="4855a-103">行要素 (ハイパーリンクを参照) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4855a-103">Row element (Hyperlink Section) ('Visio XML')</span></span>

<span data-ttu-id="4855a-104">図形間の複数のジャンプを作成するか、図面のページと別の図面ページ、別のファイル、または web サイトの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4855a-104">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4855a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4855a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4855a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4855a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4855a-107">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="4855a-107">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4855a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4855a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4855a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4855a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4855a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4855a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4855a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4855a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4855a-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="4855a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4855a-113">定義</span><span class="sxs-lookup"><span data-stu-id="4855a-113">Definition</span></span>

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4855a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4855a-114">Elements and attributes</span></span>

<span data-ttu-id="4855a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4855a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4855a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4855a-116">Parent elements</span></span>

|<span data-ttu-id="4855a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4855a-117">**Element**</span></span>|<span data-ttu-id="4855a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4855a-118">**Type**</span></span>|<span data-ttu-id="4855a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4855a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4855a-120">セクション</span><span class="sxs-lookup"><span data-stu-id="4855a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4855a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="4855a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4855a-122">図形間の複数のジャンプを作成するか、図面のページと別の図面ページ、別のファイル、または web サイトの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4855a-122">Contains elements for creating multiple jumps between a shape or drawing page and another drawing page, another file, or a website.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4855a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4855a-123">Child elements</span></span>

|<span data-ttu-id="4855a-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="4855a-124">**Element**</span></span>|<span data-ttu-id="4855a-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4855a-125">**Type**</span></span>|<span data-ttu-id="4855a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4855a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4855a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="4855a-127">Cell</span></span>](cell-element-hyperlink-rowvisio-xml.md) <br/> |[<span data-ttu-id="4855a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4855a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4855a-129">図形に関連付けられている 1 つのハイパーリンクの情報が含まれています</span><span class="sxs-lookup"><span data-stu-id="4855a-129">Contains the information for a single hyperlink associated with a shape</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4855a-130">属性</span><span class="sxs-lookup"><span data-stu-id="4855a-130">Attributes</span></span>

|<span data-ttu-id="4855a-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="4855a-131">**Attribute**</span></span>|<span data-ttu-id="4855a-132">**型**</span><span class="sxs-lookup"><span data-stu-id="4855a-132">**Type**</span></span>|<span data-ttu-id="4855a-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="4855a-133">**Required**</span></span>|<span data-ttu-id="4855a-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="4855a-134">**Description**</span></span>|<span data-ttu-id="4855a-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4855a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4855a-136">Del</span><span class="sxs-lookup"><span data-stu-id="4855a-136">Del</span></span>  <br/> |<span data-ttu-id="4855a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="4855a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4855a-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="4855a-138">optional</span></span>  <br/> |<span data-ttu-id="4855a-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4855a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="4855a-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4855a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4855a-141">IX</span><span class="sxs-lookup"><span data-stu-id="4855a-141">IX</span></span>  <br/> |<span data-ttu-id="4855a-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4855a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4855a-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="4855a-143">optional</span></span>  <br/> |<span data-ttu-id="4855a-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="4855a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="4855a-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="4855a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="4855a-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="4855a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4855a-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4855a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4855a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="4855a-148">LocalName</span></span>  <br/> |<span data-ttu-id="4855a-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4855a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="4855a-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="4855a-150">optional</span></span>  <br/> |<span data-ttu-id="4855a-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4855a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="4855a-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4855a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4855a-153">N</span><span class="sxs-lookup"><span data-stu-id="4855a-153">N</span></span>  <br/> |<span data-ttu-id="4855a-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4855a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="4855a-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="4855a-155">optional</span></span>  <br/> |<span data-ttu-id="4855a-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="4855a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="4855a-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="4855a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="4855a-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4855a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4855a-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="4855a-159">T</span></span>  <br/> |<span data-ttu-id="4855a-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4855a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="4855a-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="4855a-161">optional</span></span>  <br/> |<span data-ttu-id="4855a-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="4855a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="4855a-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="4855a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="4855a-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4855a-164">Values of the xsd:string type.</span></span>  <br/> |
   

