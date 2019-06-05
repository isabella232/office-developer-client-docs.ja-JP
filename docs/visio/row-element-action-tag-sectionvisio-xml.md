---
title: Row 要素 (操作タグセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: 図形またはページ上のアクションタグを定義します。
ms.openlocfilehash: 44008d43871bfec9b5b943f19ce6ce0a069323d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540428"
---
# <a name="row-element-action-tag-section-visio-xml"></a><span data-ttu-id="54525-103">Row 要素 (操作タグセクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="54525-103">Row element (Action Tag Section) (Visio XML)</span></span>

<span data-ttu-id="54525-104">図形またはページ上のアクションタグを定義します。</span><span class="sxs-lookup"><span data-stu-id="54525-104">Defines an action tag on a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54525-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="54525-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54525-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="54525-106">**Element type**</span></span> <br/> |[<span data-ttu-id="54525-107">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="54525-107">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54525-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="54525-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54525-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="54525-109">**Schema file**</span></span> <br/> |<span data-ttu-id="54525-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="54525-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54525-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="54525-111">**Document parts**</span></span> <br/> |<span data-ttu-id="54525-112">masters、master # .xml、pages .xml、page # .xml</span><span class="sxs-lookup"><span data-stu-id="54525-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54525-113">定義</span><span class="sxs-lookup"><span data-stu-id="54525-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54525-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="54525-114">Elements and attributes</span></span>

<span data-ttu-id="54525-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="54525-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54525-116">親要素</span><span class="sxs-lookup"><span data-stu-id="54525-116">Parent elements</span></span>

|<span data-ttu-id="54525-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="54525-117">**Element**</span></span>|<span data-ttu-id="54525-118">**型**</span><span class="sxs-lookup"><span data-stu-id="54525-118">**Type**</span></span>|<span data-ttu-id="54525-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="54525-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54525-120">Section</span><span class="sxs-lookup"><span data-stu-id="54525-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54525-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="54525-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54525-122">図形またはページ上のアクションタグを定義します。</span><span class="sxs-lookup"><span data-stu-id="54525-122">Defines an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54525-123">子要素</span><span class="sxs-lookup"><span data-stu-id="54525-123">Child elements</span></span>

|<span data-ttu-id="54525-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="54525-124">**Element**</span></span>|<span data-ttu-id="54525-125">**型**</span><span class="sxs-lookup"><span data-stu-id="54525-125">**Type**</span></span>|<span data-ttu-id="54525-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="54525-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54525-127">Cell</span><span class="sxs-lookup"><span data-stu-id="54525-127">Cell</span></span>](cell-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="54525-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="54525-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54525-129">図形またはページ上のアクションタグに1つのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="54525-129">Defines one property for an action tag on a shape or page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="54525-130">属性</span><span class="sxs-lookup"><span data-stu-id="54525-130">Attributes</span></span>

|<span data-ttu-id="54525-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="54525-131">**Attribute**</span></span>|<span data-ttu-id="54525-132">**型**</span><span class="sxs-lookup"><span data-stu-id="54525-132">**Type**</span></span>|<span data-ttu-id="54525-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="54525-133">**Required**</span></span>|<span data-ttu-id="54525-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="54525-134">**Description**</span></span>|<span data-ttu-id="54525-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="54525-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54525-136">Del</span><span class="sxs-lookup"><span data-stu-id="54525-136">Del</span></span>  <br/> |<span data-ttu-id="54525-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="54525-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="54525-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="54525-138">optional</span></span>  <br/> |<span data-ttu-id="54525-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="54525-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="54525-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="54525-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="54525-141">IX</span><span class="sxs-lookup"><span data-stu-id="54525-141">IX</span></span>  <br/> |<span data-ttu-id="54525-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="54525-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54525-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="54525-143">optional</span></span>  <br/> |<span data-ttu-id="54525-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="54525-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="54525-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="54525-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="54525-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54525-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="54525-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="54525-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="54525-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="54525-148">LocalName</span></span>  <br/> |<span data-ttu-id="54525-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="54525-149">xsd:string</span></span>  <br/> |<span data-ttu-id="54525-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="54525-150">optional</span></span>  <br/> |<span data-ttu-id="54525-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="54525-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="54525-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="54525-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="54525-153">N</span><span class="sxs-lookup"><span data-stu-id="54525-153">N</span></span>  <br/> |<span data-ttu-id="54525-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="54525-154">xsd:string</span></span>  <br/> |<span data-ttu-id="54525-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="54525-155">optional</span></span>  <br/> |<span data-ttu-id="54525-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="54525-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="54525-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54525-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="54525-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="54525-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="54525-159">T</span><span class="sxs-lookup"><span data-stu-id="54525-159">T</span></span>  <br/> |<span data-ttu-id="54525-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="54525-160">xsd:string</span></span>  <br/> |<span data-ttu-id="54525-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="54525-161">optional</span></span>  <br/> |<span data-ttu-id="54525-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="54525-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="54525-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="54525-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="54525-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="54525-164">Values of the xsd:string type.</span></span>  <br/> |
   

