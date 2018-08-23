---
title: 行要素 (段落、セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 00ecaa82-3b40-24cc-91c0-b2562e92161d
description: 図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。
ms.openlocfilehash: ac4b2083889d3cf01b8c5bfe2fa64fe0ec1ad01a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806290"
---
# <a name="row-element-paragraph-section-visio-xml"></a><span data-ttu-id="8af6e-103">行要素 (段落、セクション)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="8af6e-103">Row element (Paragraph Section) ('Visio XML')</span></span>

<span data-ttu-id="8af6e-104">図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。</span><span class="sxs-lookup"><span data-stu-id="8af6e-104">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8af6e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8af6e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8af6e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8af6e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8af6e-107">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="8af6e-107">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8af6e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="8af6e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8af6e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8af6e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8af6e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8af6e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8af6e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8af6e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8af6e-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="8af6e-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8af6e-113">定義</span><span class="sxs-lookup"><span data-stu-id="8af6e-113">Definition</span></span>

```XML
< xs:element name="Row" type="ParagraphRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8af6e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8af6e-114">Elements and attributes</span></span>

<span data-ttu-id="8af6e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8af6e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8af6e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8af6e-116">Parent elements</span></span>

|<span data-ttu-id="8af6e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8af6e-117">**Element**</span></span>|<span data-ttu-id="8af6e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8af6e-118">**Type**</span></span>|<span data-ttu-id="8af6e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8af6e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8af6e-120">セクション</span><span class="sxs-lookup"><span data-stu-id="8af6e-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8af6e-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="8af6e-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8af6e-122">図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。</span><span class="sxs-lookup"><span data-stu-id="8af6e-122">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8af6e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8af6e-123">Child elements</span></span>

|<span data-ttu-id="8af6e-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="8af6e-124">**Element**</span></span>|<span data-ttu-id="8af6e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8af6e-125">**Type**</span></span>|<span data-ttu-id="8af6e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8af6e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8af6e-127">Cell</span><span class="sxs-lookup"><span data-stu-id="8af6e-127">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="8af6e-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8af6e-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8af6e-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8af6e-130">属性</span><span class="sxs-lookup"><span data-stu-id="8af6e-130">Attributes</span></span>

|<span data-ttu-id="8af6e-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="8af6e-131">**Attribute**</span></span>|<span data-ttu-id="8af6e-132">**型**</span><span class="sxs-lookup"><span data-stu-id="8af6e-132">**Type**</span></span>|<span data-ttu-id="8af6e-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="8af6e-133">**Required**</span></span>|<span data-ttu-id="8af6e-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="8af6e-134">**Description**</span></span>|<span data-ttu-id="8af6e-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="8af6e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8af6e-136">Del</span><span class="sxs-lookup"><span data-stu-id="8af6e-136">Del</span></span>  <br/> |<span data-ttu-id="8af6e-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="8af6e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8af6e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="8af6e-138">optional</span></span>  <br/> |<span data-ttu-id="8af6e-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="8af6e-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8af6e-141">IX</span><span class="sxs-lookup"><span data-stu-id="8af6e-141">IX</span></span>  <br/> |<span data-ttu-id="8af6e-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8af6e-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8af6e-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="8af6e-143">optional</span></span>  <br/> |<span data-ttu-id="8af6e-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="8af6e-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="8af6e-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="8af6e-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8af6e-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8af6e-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="8af6e-148">LocalName</span></span>  <br/> |<span data-ttu-id="8af6e-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8af6e-149">xsd:string</span></span>  <br/> |<span data-ttu-id="8af6e-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="8af6e-150">optional</span></span>  <br/> |<span data-ttu-id="8af6e-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="8af6e-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8af6e-153">N</span><span class="sxs-lookup"><span data-stu-id="8af6e-153">N</span></span>  <br/> |<span data-ttu-id="8af6e-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8af6e-154">xsd:string</span></span>  <br/> |<span data-ttu-id="8af6e-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="8af6e-155">optional</span></span>  <br/> |<span data-ttu-id="8af6e-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="8af6e-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="8af6e-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="8af6e-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8af6e-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="8af6e-159">T</span></span>  <br/> |<span data-ttu-id="8af6e-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8af6e-160">xsd:string</span></span>  <br/> |<span data-ttu-id="8af6e-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="8af6e-161">optional</span></span>  <br/> |<span data-ttu-id="8af6e-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="8af6e-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="8af6e-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8af6e-164">Values of the xsd:string type.</span></span>  <br/> |
   

