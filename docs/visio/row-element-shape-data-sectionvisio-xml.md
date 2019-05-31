---
title: Row 要素 (Shape Data セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: 図形にデータを関連付けるための1つの図形データエントリを指定します。
ms.openlocfilehash: 4c5644aa2088dcaf3be81ea9aeaa549c911a31f6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538271"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="d0d71-103">Row 要素 (Shape Data セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d0d71-103">Row element (Shape Data Section) (Visio XML)</span></span>

<span data-ttu-id="d0d71-104">図形にデータを関連付けるための1つの図形データエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0d71-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d0d71-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0d71-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d0d71-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d0d71-107">Shape Data_Type</span><span class="sxs-lookup"><span data-stu-id="d0d71-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d0d71-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0d71-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d0d71-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d0d71-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d0d71-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d0d71-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d0d71-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d0d71-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d0d71-112">マスター # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="d0d71-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0d71-113">定義</span><span class="sxs-lookup"><span data-stu-id="d0d71-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0d71-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d0d71-114">Elements and attributes</span></span>

<span data-ttu-id="d0d71-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d71-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d0d71-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d0d71-116">Parent elements</span></span>

|<span data-ttu-id="d0d71-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d0d71-117">**Element**</span></span>|<span data-ttu-id="d0d71-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d0d71-118">**Type**</span></span>|<span data-ttu-id="d0d71-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0d71-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0d71-120">Section</span><span class="sxs-lookup"><span data-stu-id="d0d71-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0d71-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d0d71-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0d71-122">図形にデータを関連付けるための1つの図形データエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d0d71-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d0d71-123">Child elements</span></span>

|<span data-ttu-id="d0d71-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0d71-124">**Element**</span></span>|<span data-ttu-id="d0d71-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d0d71-125">**Type**</span></span>|<span data-ttu-id="d0d71-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0d71-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0d71-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d0d71-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d0d71-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d0d71-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0d71-129">図形データの1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d0d71-130">属性</span><span class="sxs-lookup"><span data-stu-id="d0d71-130">Attributes</span></span>

|<span data-ttu-id="d0d71-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="d0d71-131">**Attribute**</span></span>|<span data-ttu-id="d0d71-132">**型**</span><span class="sxs-lookup"><span data-stu-id="d0d71-132">**Type**</span></span>|<span data-ttu-id="d0d71-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="d0d71-133">**Required**</span></span>|<span data-ttu-id="d0d71-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0d71-134">**Description**</span></span>|<span data-ttu-id="d0d71-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d0d71-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0d71-136">Del</span><span class="sxs-lookup"><span data-stu-id="d0d71-136">Del</span></span>  <br/> |<span data-ttu-id="d0d71-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d0d71-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d0d71-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0d71-138">optional</span></span>  <br/> |<span data-ttu-id="d0d71-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="d0d71-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0d71-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d0d71-141">IX</span><span class="sxs-lookup"><span data-stu-id="d0d71-141">IX</span></span>  <br/> |<span data-ttu-id="d0d71-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="d0d71-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0d71-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0d71-143">optional</span></span>  <br/> |<span data-ttu-id="d0d71-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="d0d71-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0d71-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="d0d71-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d0d71-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d0d71-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0d71-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0d71-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="d0d71-148">LocalName</span></span>  <br/> |<span data-ttu-id="d0d71-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d0d71-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d0d71-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0d71-150">optional</span></span>  <br/> |<span data-ttu-id="d0d71-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="d0d71-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0d71-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0d71-153">N</span><span class="sxs-lookup"><span data-stu-id="d0d71-153">N</span></span>  <br/> |<span data-ttu-id="d0d71-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d0d71-154">xsd:string</span></span>  <br/> |<span data-ttu-id="d0d71-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0d71-155">optional</span></span>  <br/> |<span data-ttu-id="d0d71-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0d71-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="d0d71-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d0d71-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d0d71-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0d71-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0d71-159">T</span><span class="sxs-lookup"><span data-stu-id="d0d71-159">T</span></span>  <br/> |<span data-ttu-id="d0d71-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d0d71-160">xsd:string</span></span>  <br/> |<span data-ttu-id="d0d71-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0d71-161">optional</span></span>  <br/> |<span data-ttu-id="d0d71-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0d71-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="d0d71-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="d0d71-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="d0d71-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0d71-164">Values of the xsd:string type.</span></span>  <br/> |
   

