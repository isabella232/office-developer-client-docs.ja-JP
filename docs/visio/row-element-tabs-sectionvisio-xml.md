---
title: Row 要素 ([タブ] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a30d5701-4b56-c44c-fb62-d9daaee3b86e
description: タブの停止位置や配置を制御する、図形およびスタイルのセルを格納します。
ms.openlocfilehash: 530d2e564615f33292b52f9aa860c0cf2794bc67
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538180"
---
# <a name="row-element-tabs-section-visio-xml"></a><span data-ttu-id="62642-103">Row 要素 ([タブ] セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="62642-103">Row element (Tabs Section) (Visio XML)</span></span>

<span data-ttu-id="62642-104">タブの停止位置や配置を制御する、図形およびスタイルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="62642-104">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62642-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="62642-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62642-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="62642-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62642-107">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="62642-107">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62642-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62642-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62642-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="62642-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62642-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62642-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62642-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="62642-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62642-112">document.xml、master#.xml、page#.xml</span><span class="sxs-lookup"><span data-stu-id="62642-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62642-113">定義</span><span class="sxs-lookup"><span data-stu-id="62642-113">Definition</span></span>

```XML
< xs:element name="Row" type="TabsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62642-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="62642-114">Elements and attributes</span></span>

<span data-ttu-id="62642-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62642-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62642-116">親要素</span><span class="sxs-lookup"><span data-stu-id="62642-116">Parent elements</span></span>

|<span data-ttu-id="62642-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="62642-117">**Element**</span></span>|<span data-ttu-id="62642-118">**型**</span><span class="sxs-lookup"><span data-stu-id="62642-118">**Type**</span></span>|<span data-ttu-id="62642-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="62642-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62642-120">Section</span><span class="sxs-lookup"><span data-stu-id="62642-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62642-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="62642-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62642-122">タブの停止位置や配置を制御する、図形およびスタイルのセルを格納します。</span><span class="sxs-lookup"><span data-stu-id="62642-122">Contains cells for shapes or styles that control tab stop position and alignment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62642-123">子要素</span><span class="sxs-lookup"><span data-stu-id="62642-123">Child elements</span></span>

|<span data-ttu-id="62642-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="62642-124">**Element**</span></span>|<span data-ttu-id="62642-125">**型**</span><span class="sxs-lookup"><span data-stu-id="62642-125">**Type**</span></span>|<span data-ttu-id="62642-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="62642-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62642-127">Cell</span><span class="sxs-lookup"><span data-stu-id="62642-127">Cell</span></span>](cell-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="62642-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="62642-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62642-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="62642-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="62642-130">属性</span><span class="sxs-lookup"><span data-stu-id="62642-130">Attributes</span></span>

|<span data-ttu-id="62642-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="62642-131">**Attribute**</span></span>|<span data-ttu-id="62642-132">**型**</span><span class="sxs-lookup"><span data-stu-id="62642-132">**Type**</span></span>|<span data-ttu-id="62642-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="62642-133">**Required**</span></span>|<span data-ttu-id="62642-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="62642-134">**Description**</span></span>|<span data-ttu-id="62642-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="62642-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62642-136">Del</span><span class="sxs-lookup"><span data-stu-id="62642-136">Del</span></span>  <br/> |<span data-ttu-id="62642-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="62642-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="62642-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="62642-138">optional</span></span>  <br/> |<span data-ttu-id="62642-139">それ以外の場合はマスター図形から継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="62642-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="62642-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="62642-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="62642-141">IX</span><span class="sxs-lookup"><span data-stu-id="62642-141">IX</span></span>  <br/> |<span data-ttu-id="62642-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="62642-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62642-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="62642-143">optional</span></span>  <br/> |<span data-ttu-id="62642-144">行の 1 ベースの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="62642-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="62642-145">これは、同じセクション内の他の識別子よりも長く、unqiue である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、Scratch、および Tabs セクションでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="62642-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="62642-146">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="62642-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="62642-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="62642-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="62642-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="62642-148">LocalName</span></span>  <br/> |<span data-ttu-id="62642-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62642-149">xsd:string</span></span>  <br/> |<span data-ttu-id="62642-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="62642-150">optional</span></span>  <br/> |<span data-ttu-id="62642-151">行の一意の言語依存の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="62642-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="62642-152">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="62642-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62642-153">N</span><span class="sxs-lookup"><span data-stu-id="62642-153">N</span></span>  <br/> |<span data-ttu-id="62642-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62642-154">xsd:string</span></span>  <br/> |<span data-ttu-id="62642-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="62642-155">optional</span></span>  <br/> |<span data-ttu-id="62642-156">行の一意の言語に依存しない名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="62642-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="62642-157">行には IX 属性または N 属性のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="62642-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="62642-158">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="62642-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62642-159">T</span><span class="sxs-lookup"><span data-stu-id="62642-159">T</span></span>  <br/> |<span data-ttu-id="62642-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="62642-160">xsd:string</span></span>  <br/> |<span data-ttu-id="62642-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="62642-161">optional</span></span>  <br/> |<span data-ttu-id="62642-162">行で表され、ジオメトリの視覚化で使用されるジオメトリ パスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="62642-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="62642-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="62642-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="62642-164">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="62642-164">Values of the xsd:string type.</span></span>  <br/> |
   

