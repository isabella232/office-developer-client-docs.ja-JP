---
title: Row 要素 (Controls セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: 図形に定義された特定のコントロール ハンドルのセルを格納します。
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541744"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="a4ddb-103">Row 要素 (Controls セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a4ddb-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="a4ddb-104">図形に定義された特定のコントロール ハンドルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4ddb-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a4ddb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4ddb-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a4ddb-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="a4ddb-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a4ddb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a4ddb-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a4ddb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a4ddb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a4ddb-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a4ddb-112">master#.xml, page#.xml</span><span class="sxs-lookup"><span data-stu-id="a4ddb-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4ddb-113">定義</span><span class="sxs-lookup"><span data-stu-id="a4ddb-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4ddb-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a4ddb-114">Elements and attributes</span></span>

<span data-ttu-id="a4ddb-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4ddb-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a4ddb-116">Parent elements</span></span>

|<span data-ttu-id="a4ddb-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-117">**Element**</span></span>|<span data-ttu-id="a4ddb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-118">**Type**</span></span>|<span data-ttu-id="a4ddb-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4ddb-120">Section</span><span class="sxs-lookup"><span data-stu-id="a4ddb-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a4ddb-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a4ddb-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4ddb-122">図形に定義された特定のコントロール ハンドルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4ddb-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a4ddb-123">Child elements</span></span>

|<span data-ttu-id="a4ddb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-124">**Element**</span></span>|<span data-ttu-id="a4ddb-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-125">**Type**</span></span>|<span data-ttu-id="a4ddb-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4ddb-127">Cell</span><span class="sxs-lookup"><span data-stu-id="a4ddb-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="a4ddb-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="a4ddb-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a4ddb-129">図形に定義された特定のコントロール ハンドルのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a4ddb-130">属性</span><span class="sxs-lookup"><span data-stu-id="a4ddb-130">Attributes</span></span>

|<span data-ttu-id="a4ddb-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-131">**Attribute**</span></span>|<span data-ttu-id="a4ddb-132">**型**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-132">**Type**</span></span>|<span data-ttu-id="a4ddb-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-133">**Required**</span></span>|<span data-ttu-id="a4ddb-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-134">**Description**</span></span>|<span data-ttu-id="a4ddb-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a4ddb-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4ddb-136">Del</span><span class="sxs-lookup"><span data-stu-id="a4ddb-136">Del</span></span>  <br/> |<span data-ttu-id="a4ddb-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a4ddb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a4ddb-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4ddb-138">optional</span></span>  <br/> |<span data-ttu-id="a4ddb-139">それ以外の場合はマスター図形から継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="a4ddb-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a4ddb-141">IX</span><span class="sxs-lookup"><span data-stu-id="a4ddb-141">IX</span></span>  <br/> |<span data-ttu-id="a4ddb-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a4ddb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a4ddb-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4ddb-143">optional</span></span>  <br/> |<span data-ttu-id="a4ddb-144">行の 1 ベースの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="a4ddb-145">これは、同じセクション内の他の識別子よりも長く、unqiue である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、Scratch、および Tabs セクションでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="a4ddb-146">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="a4ddb-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a4ddb-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="a4ddb-148">LocalName</span></span>  <br/> |<span data-ttu-id="a4ddb-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4ddb-149">xsd:string</span></span>  <br/> |<span data-ttu-id="a4ddb-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4ddb-150">optional</span></span>  <br/> |<span data-ttu-id="a4ddb-151">行の一意の言語依存の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="a4ddb-152">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4ddb-153">N</span><span class="sxs-lookup"><span data-stu-id="a4ddb-153">N</span></span>  <br/> |<span data-ttu-id="a4ddb-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4ddb-154">xsd:string</span></span>  <br/> |<span data-ttu-id="a4ddb-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4ddb-155">optional</span></span>  <br/> |<span data-ttu-id="a4ddb-156">行の一意の言語に依存しない名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="a4ddb-157">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="a4ddb-158">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a4ddb-159">T</span><span class="sxs-lookup"><span data-stu-id="a4ddb-159">T</span></span>  <br/> |<span data-ttu-id="a4ddb-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a4ddb-160">xsd:string</span></span>  <br/> |<span data-ttu-id="a4ddb-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="a4ddb-161">optional</span></span>  <br/> |<span data-ttu-id="a4ddb-162">行で表され、ジオメトリの視覚化で使用されるジオメトリ パスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="a4ddb-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="a4ddb-164">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a4ddb-164">Values of the xsd:string type.</span></span>  <br/> |
   

