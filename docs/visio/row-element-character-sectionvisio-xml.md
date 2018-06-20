---
title: 行要素 ([Character] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: 、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。
ms.openlocfilehash: 11194506a593a445656852b107f6fd780a39b9b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806265"
---
# <a name="row-element-character-section-visio-xml"></a><span data-ttu-id="970be-103">行要素 ([Character] セクション) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="970be-103">Row element (Character Section) ('Visio XML')</span></span>

<span data-ttu-id="970be-104">、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。</span><span class="sxs-lookup"><span data-stu-id="970be-104">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="970be-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="970be-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="970be-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="970be-106">**Element type**</span></span> <br/> |[<span data-ttu-id="970be-107">CharacterRow_Type</span><span class="sxs-lookup"><span data-stu-id="970be-107">CharacterRow_Type</span></span>](characterrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="970be-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="970be-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="970be-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="970be-109">**Schema file**</span></span> <br/> |<span data-ttu-id="970be-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="970be-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="970be-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="970be-111">**Document parts**</span></span> <br/> |<span data-ttu-id="970be-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="970be-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="970be-113">定義</span><span class="sxs-lookup"><span data-stu-id="970be-113">Definition</span></span>

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="970be-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="970be-114">Elements and attributes</span></span>

<span data-ttu-id="970be-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="970be-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="970be-116">親要素</span><span class="sxs-lookup"><span data-stu-id="970be-116">Parent elements</span></span>

|<span data-ttu-id="970be-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="970be-117">**Element**</span></span>|<span data-ttu-id="970be-118">**型**</span><span class="sxs-lookup"><span data-stu-id="970be-118">**Type**</span></span>|<span data-ttu-id="970be-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="970be-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="970be-120">Section</span><span class="sxs-lookup"><span data-stu-id="970be-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="970be-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="970be-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="970be-122">、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。</span><span class="sxs-lookup"><span data-stu-id="970be-122">Shows the formatting attributes for a text run of the shape, such as font, color, text style, case, position relative to the baseline, and point size.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="970be-123">子要素</span><span class="sxs-lookup"><span data-stu-id="970be-123">Child elements</span></span>

|<span data-ttu-id="970be-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="970be-124">**Element**</span></span>|<span data-ttu-id="970be-125">**型**</span><span class="sxs-lookup"><span data-stu-id="970be-125">**Type**</span></span>|<span data-ttu-id="970be-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="970be-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="970be-127">Cell</span><span class="sxs-lookup"><span data-stu-id="970be-127">Cell</span></span>](cell-element-character-sectionvisio-xml.md) <br/> |[<span data-ttu-id="970be-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="970be-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="970be-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="970be-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="970be-130">属性</span><span class="sxs-lookup"><span data-stu-id="970be-130">Attributes</span></span>

|<span data-ttu-id="970be-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="970be-131">**Attribute**</span></span>|<span data-ttu-id="970be-132">**型**</span><span class="sxs-lookup"><span data-stu-id="970be-132">**Type**</span></span>|<span data-ttu-id="970be-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="970be-133">**Required**</span></span>|<span data-ttu-id="970be-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="970be-134">**Description**</span></span>|<span data-ttu-id="970be-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="970be-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="970be-136">Del</span><span class="sxs-lookup"><span data-stu-id="970be-136">Del</span></span>  <br/> |<span data-ttu-id="970be-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="970be-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="970be-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="970be-138">optional</span></span>  <br/> |<span data-ttu-id="970be-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="970be-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="970be-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970be-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="970be-141">IX</span><span class="sxs-lookup"><span data-stu-id="970be-141">IX</span></span>  <br/> |<span data-ttu-id="970be-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="970be-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="970be-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="970be-143">optional</span></span>  <br/> |<span data-ttu-id="970be-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="970be-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="970be-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="970be-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="970be-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="970be-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="970be-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970be-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="970be-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="970be-148">LocalName</span></span>  <br/> |<span data-ttu-id="970be-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="970be-149">xsd:string</span></span>  <br/> |<span data-ttu-id="970be-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="970be-150">optional</span></span>  <br/> |<span data-ttu-id="970be-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="970be-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="970be-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970be-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="970be-153">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="970be-153">N</span></span>  <br/> |<span data-ttu-id="970be-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="970be-154">xsd:string</span></span>  <br/> |<span data-ttu-id="970be-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="970be-155">optional</span></span>  <br/> |<span data-ttu-id="970be-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="970be-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="970be-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="970be-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="970be-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970be-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="970be-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="970be-159">T</span></span>  <br/> |<span data-ttu-id="970be-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="970be-160">xsd:string</span></span>  <br/> |<span data-ttu-id="970be-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="970be-161">optional</span></span>  <br/> |<span data-ttu-id="970be-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="970be-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="970be-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="970be-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="970be-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970be-164">Values of the xsd:string type.</span></span>  <br/> |
   

