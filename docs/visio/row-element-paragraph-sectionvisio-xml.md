---
title: Row 要素 (段落セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 00ecaa82-3b40-24cc-91c0-b2562e92161d
description: 図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。
ms.openlocfilehash: 48d32f3a0712e2ed3110ced545d5b946f147d755
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540820"
---
# <a name="row-element-paragraph-section-visio-xml"></a><span data-ttu-id="79914-103">Row 要素 (段落セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="79914-103">Row element (Paragraph Section) (Visio XML)</span></span>

<span data-ttu-id="79914-104">図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。</span><span class="sxs-lookup"><span data-stu-id="79914-104">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79914-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="79914-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79914-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="79914-106">**Element type**</span></span> <br/> |[<span data-ttu-id="79914-107">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="79914-107">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="79914-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="79914-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="79914-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="79914-109">**Schema file**</span></span> <br/> |<span data-ttu-id="79914-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="79914-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="79914-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="79914-111">**Document parts**</span></span> <br/> |<span data-ttu-id="79914-112">文書 .xml、master # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="79914-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79914-113">定義</span><span class="sxs-lookup"><span data-stu-id="79914-113">Definition</span></span>

```XML
< xs:element name="Row" type="ParagraphRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="79914-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="79914-114">Elements and attributes</span></span>

<span data-ttu-id="79914-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="79914-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="79914-116">親要素</span><span class="sxs-lookup"><span data-stu-id="79914-116">Parent elements</span></span>

|<span data-ttu-id="79914-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="79914-117">**Element**</span></span>|<span data-ttu-id="79914-118">**型**</span><span class="sxs-lookup"><span data-stu-id="79914-118">**Type**</span></span>|<span data-ttu-id="79914-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="79914-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79914-120">Section</span><span class="sxs-lookup"><span data-stu-id="79914-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="79914-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="79914-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="79914-122">図形のテキストに対する、段落の書式属性を表示します。属性には、インデント、行間隔、箇条書き、および段落の水平方向の配置などがあります。</span><span class="sxs-lookup"><span data-stu-id="79914-122">Shows the paragraph formatting attributes for the shape's text, such as indents, line spacing, bullets, and horizontal alignment of paragraphs.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="79914-123">子要素</span><span class="sxs-lookup"><span data-stu-id="79914-123">Child elements</span></span>

|<span data-ttu-id="79914-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="79914-124">**Element**</span></span>|<span data-ttu-id="79914-125">**型**</span><span class="sxs-lookup"><span data-stu-id="79914-125">**Type**</span></span>|<span data-ttu-id="79914-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="79914-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79914-127">Cell</span><span class="sxs-lookup"><span data-stu-id="79914-127">Cell</span></span>](cell-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="79914-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="79914-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="79914-129">1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="79914-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="79914-130">属性</span><span class="sxs-lookup"><span data-stu-id="79914-130">Attributes</span></span>

|<span data-ttu-id="79914-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="79914-131">**Attribute**</span></span>|<span data-ttu-id="79914-132">**型**</span><span class="sxs-lookup"><span data-stu-id="79914-132">**Type**</span></span>|<span data-ttu-id="79914-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="79914-133">**Required**</span></span>|<span data-ttu-id="79914-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="79914-134">**Description**</span></span>|<span data-ttu-id="79914-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="79914-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="79914-136">Del</span><span class="sxs-lookup"><span data-stu-id="79914-136">Del</span></span>  <br/> |<span data-ttu-id="79914-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="79914-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="79914-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="79914-138">optional</span></span>  <br/> |<span data-ttu-id="79914-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="79914-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="79914-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="79914-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="79914-141">IX</span><span class="sxs-lookup"><span data-stu-id="79914-141">IX</span></span>  <br/> |<span data-ttu-id="79914-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="79914-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="79914-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="79914-143">optional</span></span>  <br/> |<span data-ttu-id="79914-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="79914-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="79914-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="79914-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="79914-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="79914-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="79914-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="79914-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="79914-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="79914-148">LocalName</span></span>  <br/> |<span data-ttu-id="79914-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="79914-149">xsd:string</span></span>  <br/> |<span data-ttu-id="79914-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="79914-150">optional</span></span>  <br/> |<span data-ttu-id="79914-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="79914-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="79914-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="79914-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79914-153">N</span><span class="sxs-lookup"><span data-stu-id="79914-153">N</span></span>  <br/> |<span data-ttu-id="79914-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="79914-154">xsd:string</span></span>  <br/> |<span data-ttu-id="79914-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="79914-155">optional</span></span>  <br/> |<span data-ttu-id="79914-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="79914-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="79914-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="79914-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="79914-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="79914-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79914-159">T</span><span class="sxs-lookup"><span data-stu-id="79914-159">T</span></span>  <br/> |<span data-ttu-id="79914-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="79914-160">xsd:string</span></span>  <br/> |<span data-ttu-id="79914-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="79914-161">optional</span></span>  <br/> |<span data-ttu-id="79914-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="79914-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="79914-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="79914-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="79914-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="79914-164">Values of the xsd:string type.</span></span>  <br/> |
   

