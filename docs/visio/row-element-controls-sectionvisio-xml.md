---
title: Row 要素 (Controls セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: 図形に定義されている特定のコントロールハンドルのセルを格納します。
ms.openlocfilehash: 0fb31d8066e0a76bfe00735cb5dcc984d02685f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541744"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="be54a-103">Row 要素 (Controls セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="be54a-103">Row element (Controls Section) (Visio XML)</span></span>

<span data-ttu-id="be54a-104">図形に定義されている特定のコントロールハンドルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="be54a-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be54a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="be54a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be54a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="be54a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="be54a-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="be54a-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="be54a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="be54a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="be54a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="be54a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="be54a-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="be54a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="be54a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="be54a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="be54a-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="be54a-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be54a-113">定義</span><span class="sxs-lookup"><span data-stu-id="be54a-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be54a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="be54a-114">Elements and attributes</span></span>

<span data-ttu-id="be54a-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="be54a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="be54a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="be54a-116">Parent elements</span></span>

|<span data-ttu-id="be54a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="be54a-117">**Element**</span></span>|<span data-ttu-id="be54a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="be54a-118">**Type**</span></span>|<span data-ttu-id="be54a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="be54a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be54a-120">Section</span><span class="sxs-lookup"><span data-stu-id="be54a-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be54a-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="be54a-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be54a-122">図形に定義されている特定のコントロールハンドルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="be54a-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="be54a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="be54a-123">Child elements</span></span>

|<span data-ttu-id="be54a-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="be54a-124">**Element**</span></span>|<span data-ttu-id="be54a-125">**型**</span><span class="sxs-lookup"><span data-stu-id="be54a-125">**Type**</span></span>|<span data-ttu-id="be54a-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="be54a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be54a-127">Cell</span><span class="sxs-lookup"><span data-stu-id="be54a-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="be54a-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="be54a-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be54a-129">図形に定義されている特定のコントロールハンドルのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be54a-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="be54a-130">属性</span><span class="sxs-lookup"><span data-stu-id="be54a-130">Attributes</span></span>

|<span data-ttu-id="be54a-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="be54a-131">**Attribute**</span></span>|<span data-ttu-id="be54a-132">**型**</span><span class="sxs-lookup"><span data-stu-id="be54a-132">**Type**</span></span>|<span data-ttu-id="be54a-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="be54a-133">**Required**</span></span>|<span data-ttu-id="be54a-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="be54a-134">**Description**</span></span>|<span data-ttu-id="be54a-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="be54a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="be54a-136">Del</span><span class="sxs-lookup"><span data-stu-id="be54a-136">Del</span></span>  <br/> |<span data-ttu-id="be54a-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="be54a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="be54a-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="be54a-138">optional</span></span>  <br/> |<span data-ttu-id="be54a-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="be54a-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="be54a-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="be54a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="be54a-141">IX</span><span class="sxs-lookup"><span data-stu-id="be54a-141">IX</span></span>  <br/> |<span data-ttu-id="be54a-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="be54a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="be54a-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="be54a-143">optional</span></span>  <br/> |<span data-ttu-id="be54a-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="be54a-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="be54a-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="be54a-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="be54a-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="be54a-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="be54a-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="be54a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="be54a-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="be54a-148">LocalName</span></span>  <br/> |<span data-ttu-id="be54a-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="be54a-149">xsd:string</span></span>  <br/> |<span data-ttu-id="be54a-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="be54a-150">optional</span></span>  <br/> |<span data-ttu-id="be54a-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="be54a-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="be54a-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="be54a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="be54a-153">N</span><span class="sxs-lookup"><span data-stu-id="be54a-153">N</span></span>  <br/> |<span data-ttu-id="be54a-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="be54a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="be54a-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="be54a-155">optional</span></span>  <br/> |<span data-ttu-id="be54a-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="be54a-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="be54a-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="be54a-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="be54a-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="be54a-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="be54a-159">T</span><span class="sxs-lookup"><span data-stu-id="be54a-159">T</span></span>  <br/> |<span data-ttu-id="be54a-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="be54a-160">xsd:string</span></span>  <br/> |<span data-ttu-id="be54a-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="be54a-161">optional</span></span>  <br/> |<span data-ttu-id="be54a-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="be54a-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="be54a-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="be54a-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="be54a-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="be54a-164">Values of the xsd:string type.</span></span>  <br/> |
   

