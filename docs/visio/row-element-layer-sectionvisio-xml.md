---
title: Row 要素 (Layer セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: ページの1つのレイヤーとそのプロパティを定義する要素が含まれています。
ms.openlocfilehash: edd076651838d7522af07013cda5fedd9a28de7f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540864"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="59e22-103">Row 要素 (Layer セクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="59e22-103">Row element (Layer Section) (Visio XML)</span></span>

<span data-ttu-id="59e22-104">ページの1つのレイヤーとそのプロパティを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59e22-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59e22-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="59e22-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59e22-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="59e22-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59e22-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="59e22-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59e22-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="59e22-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59e22-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="59e22-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59e22-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="59e22-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59e22-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="59e22-111">**Document parts**</span></span> <br/> |<span data-ttu-id="59e22-112">masters、system.xml ページ</span><span class="sxs-lookup"><span data-stu-id="59e22-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59e22-113">定義</span><span class="sxs-lookup"><span data-stu-id="59e22-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59e22-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="59e22-114">Elements and attributes</span></span>

<span data-ttu-id="59e22-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59e22-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59e22-116">親要素</span><span class="sxs-lookup"><span data-stu-id="59e22-116">Parent elements</span></span>

|<span data-ttu-id="59e22-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="59e22-117">**Element**</span></span>|<span data-ttu-id="59e22-118">**型**</span><span class="sxs-lookup"><span data-stu-id="59e22-118">**Type**</span></span>|<span data-ttu-id="59e22-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e22-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59e22-120">Section</span><span class="sxs-lookup"><span data-stu-id="59e22-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59e22-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="59e22-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59e22-122">ページの1つのレイヤーとそのプロパティを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59e22-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59e22-123">子要素</span><span class="sxs-lookup"><span data-stu-id="59e22-123">Child elements</span></span>

|<span data-ttu-id="59e22-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="59e22-124">**Element**</span></span>|<span data-ttu-id="59e22-125">**型**</span><span class="sxs-lookup"><span data-stu-id="59e22-125">**Type**</span></span>|<span data-ttu-id="59e22-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e22-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59e22-127">Cell</span><span class="sxs-lookup"><span data-stu-id="59e22-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="59e22-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="59e22-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59e22-129">ページのレイヤーまたはそのプロパティに1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="59e22-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="59e22-130">属性</span><span class="sxs-lookup"><span data-stu-id="59e22-130">Attributes</span></span>

|<span data-ttu-id="59e22-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="59e22-131">**Attribute**</span></span>|<span data-ttu-id="59e22-132">**型**</span><span class="sxs-lookup"><span data-stu-id="59e22-132">**Type**</span></span>|<span data-ttu-id="59e22-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="59e22-133">**Required**</span></span>|<span data-ttu-id="59e22-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="59e22-134">**Description**</span></span>|<span data-ttu-id="59e22-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="59e22-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59e22-136">Del</span><span class="sxs-lookup"><span data-stu-id="59e22-136">Del</span></span>  <br/> |<span data-ttu-id="59e22-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="59e22-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="59e22-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e22-138">optional</span></span>  <br/> |<span data-ttu-id="59e22-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59e22-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="59e22-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e22-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="59e22-141">IX</span><span class="sxs-lookup"><span data-stu-id="59e22-141">IX</span></span>  <br/> |<span data-ttu-id="59e22-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="59e22-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59e22-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e22-143">optional</span></span>  <br/> |<span data-ttu-id="59e22-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e22-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="59e22-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="59e22-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="59e22-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="59e22-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="59e22-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e22-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59e22-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="59e22-148">LocalName</span></span>  <br/> |<span data-ttu-id="59e22-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59e22-149">xsd:string</span></span>  <br/> |<span data-ttu-id="59e22-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e22-150">optional</span></span>  <br/> |<span data-ttu-id="59e22-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e22-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="59e22-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e22-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59e22-153">N</span><span class="sxs-lookup"><span data-stu-id="59e22-153">N</span></span>  <br/> |<span data-ttu-id="59e22-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59e22-154">xsd:string</span></span>  <br/> |<span data-ttu-id="59e22-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e22-155">optional</span></span>  <br/> |<span data-ttu-id="59e22-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="59e22-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="59e22-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="59e22-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="59e22-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e22-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59e22-159">T</span><span class="sxs-lookup"><span data-stu-id="59e22-159">T</span></span>  <br/> |<span data-ttu-id="59e22-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59e22-160">xsd:string</span></span>  <br/> |<span data-ttu-id="59e22-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="59e22-161">optional</span></span>  <br/> |<span data-ttu-id="59e22-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="59e22-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="59e22-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="59e22-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="59e22-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59e22-164">Values of the xsd:string type.</span></span>  <br/> |
   

