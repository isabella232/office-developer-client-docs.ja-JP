---
title: 行要素 ([Character] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: 、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。
ms.openlocfilehash: 3d8aa3e508b2f045a2cf38faaa795922dcc14803
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387490"
---
# <a name="row-element-character-section-visio-xml"></a><span data-ttu-id="88dd9-103">行要素 ([Character] セクション) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="88dd9-103">Row element (Character Section) ('Visio XML')</span></span>

<span data-ttu-id="88dd9-104">、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-104">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88dd9-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="88dd9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88dd9-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="88dd9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="88dd9-107">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="88dd9-107">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="88dd9-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88dd9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="88dd9-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88dd9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="88dd9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="88dd9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="88dd9-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="88dd9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="88dd9-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="88dd9-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88dd9-113">定義</span><span class="sxs-lookup"><span data-stu-id="88dd9-113">Definition</span></span>

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88dd9-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88dd9-114">Elements and attributes</span></span>

<span data-ttu-id="88dd9-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88dd9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="88dd9-116">親要素</span><span class="sxs-lookup"><span data-stu-id="88dd9-116">Parent elements</span></span>

|<span data-ttu-id="88dd9-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="88dd9-117">**Element**</span></span>|<span data-ttu-id="88dd9-118">**型**</span><span class="sxs-lookup"><span data-stu-id="88dd9-118">**Type**</span></span>|<span data-ttu-id="88dd9-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="88dd9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88dd9-120">セクション</span><span class="sxs-lookup"><span data-stu-id="88dd9-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88dd9-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="88dd9-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88dd9-122">、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-122">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88dd9-123">子要素</span><span class="sxs-lookup"><span data-stu-id="88dd9-123">Child elements</span></span>

|<span data-ttu-id="88dd9-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="88dd9-124">**Element**</span></span>|<span data-ttu-id="88dd9-125">**型**</span><span class="sxs-lookup"><span data-stu-id="88dd9-125">**Type**</span></span>|<span data-ttu-id="88dd9-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="88dd9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88dd9-127">Cell</span><span class="sxs-lookup"><span data-stu-id="88dd9-127">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="88dd9-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="88dd9-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88dd9-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="88dd9-130">属性</span><span class="sxs-lookup"><span data-stu-id="88dd9-130">Attributes</span></span>

|<span data-ttu-id="88dd9-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="88dd9-131">**Attribute**</span></span>|<span data-ttu-id="88dd9-132">**型**</span><span class="sxs-lookup"><span data-stu-id="88dd9-132">**Type**</span></span>|<span data-ttu-id="88dd9-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="88dd9-133">**Required**</span></span>|<span data-ttu-id="88dd9-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="88dd9-134">**Description**</span></span>|<span data-ttu-id="88dd9-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="88dd9-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88dd9-136">Del</span><span class="sxs-lookup"><span data-stu-id="88dd9-136">Del</span></span>  <br/> |<span data-ttu-id="88dd9-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="88dd9-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="88dd9-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="88dd9-138">optional</span></span>  <br/> |<span data-ttu-id="88dd9-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="88dd9-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="88dd9-141">IX</span><span class="sxs-lookup"><span data-stu-id="88dd9-141">IX</span></span>  <br/> |<span data-ttu-id="88dd9-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88dd9-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88dd9-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="88dd9-143">optional</span></span>  <br/> |<span data-ttu-id="88dd9-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="88dd9-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="88dd9-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="88dd9-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="88dd9-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88dd9-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="88dd9-148">LocalName</span></span>  <br/> |<span data-ttu-id="88dd9-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="88dd9-149">xsd:string</span></span>  <br/> |<span data-ttu-id="88dd9-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="88dd9-150">optional</span></span>  <br/> |<span data-ttu-id="88dd9-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="88dd9-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88dd9-153">N</span><span class="sxs-lookup"><span data-stu-id="88dd9-153">N</span></span>  <br/> |<span data-ttu-id="88dd9-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="88dd9-154">xsd:string</span></span>  <br/> |<span data-ttu-id="88dd9-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="88dd9-155">optional</span></span>  <br/> |<span data-ttu-id="88dd9-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="88dd9-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="88dd9-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="88dd9-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88dd9-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="88dd9-159">T</span></span>  <br/> |<span data-ttu-id="88dd9-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="88dd9-160">xsd:string</span></span>  <br/> |<span data-ttu-id="88dd9-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="88dd9-161">optional</span></span>  <br/> |<span data-ttu-id="88dd9-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="88dd9-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="88dd9-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88dd9-164">Values of the xsd:string type.</span></span>  <br/> |
   

