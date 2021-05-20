---
title: Row 要素 ([線のグラデーション] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: 線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: bfaf3ab8cc16e11051310d7e838b9dddbf7e108d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540827"
---
# <a name="row-element-line-gradient-section-visio-xml"></a><span data-ttu-id="97132-103">Row 要素 ([線のグラデーション] セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="97132-103">Row element (Line Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="97132-104">線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="97132-104">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97132-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="97132-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97132-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="97132-106">**Element type**</span></span> <br/> |[<span data-ttu-id="97132-107">LineGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="97132-107">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="97132-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="97132-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="97132-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="97132-109">**Schema file**</span></span> <br/> |<span data-ttu-id="97132-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="97132-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="97132-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="97132-111">**Document parts**</span></span> <br/> |<span data-ttu-id="97132-112">document.xml、master#.xml、page#.xml</span><span class="sxs-lookup"><span data-stu-id="97132-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="97132-113">定義</span><span class="sxs-lookup"><span data-stu-id="97132-113">Definition</span></span>

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="97132-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="97132-114">Elements and attributes</span></span>

<span data-ttu-id="97132-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="97132-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="97132-116">親要素</span><span class="sxs-lookup"><span data-stu-id="97132-116">Parent elements</span></span>

|<span data-ttu-id="97132-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="97132-117">**Element**</span></span>|<span data-ttu-id="97132-118">**型**</span><span class="sxs-lookup"><span data-stu-id="97132-118">**Type**</span></span>|<span data-ttu-id="97132-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="97132-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97132-120">Section</span><span class="sxs-lookup"><span data-stu-id="97132-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="97132-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="97132-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="97132-122">線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="97132-122">Contains the color, transparency, and position of a gradient stop for a line gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97132-123">子要素</span><span class="sxs-lookup"><span data-stu-id="97132-123">Child elements</span></span>

|<span data-ttu-id="97132-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="97132-124">**Element**</span></span>|<span data-ttu-id="97132-125">**型**</span><span class="sxs-lookup"><span data-stu-id="97132-125">**Type**</span></span>|<span data-ttu-id="97132-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="97132-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97132-127">Cell</span><span class="sxs-lookup"><span data-stu-id="97132-127">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="97132-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="97132-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="97132-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="97132-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="97132-130">属性</span><span class="sxs-lookup"><span data-stu-id="97132-130">Attributes</span></span>

|<span data-ttu-id="97132-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="97132-131">**Attribute**</span></span>|<span data-ttu-id="97132-132">**型**</span><span class="sxs-lookup"><span data-stu-id="97132-132">**Type**</span></span>|<span data-ttu-id="97132-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="97132-133">**Required**</span></span>|<span data-ttu-id="97132-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="97132-134">**Description**</span></span>|<span data-ttu-id="97132-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="97132-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="97132-136">Del</span><span class="sxs-lookup"><span data-stu-id="97132-136">Del</span></span>  <br/> |<span data-ttu-id="97132-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="97132-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="97132-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="97132-138">optional</span></span>  <br/> |<span data-ttu-id="97132-139">それ以外の場合はマスター図形から継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="97132-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="97132-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="97132-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="97132-141">IX</span><span class="sxs-lookup"><span data-stu-id="97132-141">IX</span></span>  <br/> |<span data-ttu-id="97132-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="97132-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="97132-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="97132-143">optional</span></span>  <br/> |<span data-ttu-id="97132-144">行の 1 ベースの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="97132-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="97132-145">これは、同じセクション内の他の識別子よりも長く、unqiue である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、Scratch、および Tabs セクションでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="97132-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="97132-146">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="97132-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="97132-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="97132-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="97132-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="97132-148">LocalName</span></span>  <br/> |<span data-ttu-id="97132-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="97132-149">xsd:string</span></span>  <br/> |<span data-ttu-id="97132-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="97132-150">optional</span></span>  <br/> |<span data-ttu-id="97132-151">行の一意の言語依存の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="97132-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="97132-152">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="97132-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="97132-153">N</span><span class="sxs-lookup"><span data-stu-id="97132-153">N</span></span>  <br/> |<span data-ttu-id="97132-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="97132-154">xsd:string</span></span>  <br/> |<span data-ttu-id="97132-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="97132-155">optional</span></span>  <br/> |<span data-ttu-id="97132-156">行の一意の言語に依存しない名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="97132-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="97132-157">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="97132-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="97132-158">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="97132-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="97132-159">T</span><span class="sxs-lookup"><span data-stu-id="97132-159">T</span></span>  <br/> |<span data-ttu-id="97132-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="97132-160">xsd:string</span></span>  <br/> |<span data-ttu-id="97132-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="97132-161">optional</span></span>  <br/> |<span data-ttu-id="97132-162">行で表され、ジオメトリの視覚化で使用されるジオメトリ パスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="97132-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="97132-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="97132-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="97132-164">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="97132-164">Values of the xsd:string type.</span></span>  <br/> |
   

