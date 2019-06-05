---
title: Row 要素 (塗りつぶしのグラデーションセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: 塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538621"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="88877-103">Row 要素 (塗りつぶしのグラデーションセクション) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="88877-103">Row element (Fill Gradient Section) (Visio XML)</span></span>

<span data-ttu-id="88877-104">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="88877-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88877-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="88877-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88877-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="88877-106">**Element type**</span></span> <br/> |[<span data-ttu-id="88877-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="88877-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="88877-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88877-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="88877-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88877-109">**Schema file**</span></span> <br/> |<span data-ttu-id="88877-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="88877-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="88877-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="88877-111">**Document parts**</span></span> <br/> |<span data-ttu-id="88877-112">文書 .xml、master # .xml、ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="88877-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88877-113">定義</span><span class="sxs-lookup"><span data-stu-id="88877-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88877-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88877-114">Elements and attributes</span></span>

<span data-ttu-id="88877-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88877-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="88877-116">親要素</span><span class="sxs-lookup"><span data-stu-id="88877-116">Parent elements</span></span>

|<span data-ttu-id="88877-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="88877-117">**Element**</span></span>|<span data-ttu-id="88877-118">**型**</span><span class="sxs-lookup"><span data-stu-id="88877-118">**Type**</span></span>|<span data-ttu-id="88877-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="88877-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88877-120">Section</span><span class="sxs-lookup"><span data-stu-id="88877-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88877-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="88877-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88877-122">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="88877-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88877-123">子要素</span><span class="sxs-lookup"><span data-stu-id="88877-123">Child elements</span></span>

|<span data-ttu-id="88877-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="88877-124">**Element**</span></span>|<span data-ttu-id="88877-125">**型**</span><span class="sxs-lookup"><span data-stu-id="88877-125">**Type**</span></span>|<span data-ttu-id="88877-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="88877-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88877-127">Cell</span><span class="sxs-lookup"><span data-stu-id="88877-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="88877-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="88877-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88877-129">1つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="88877-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="88877-130">属性</span><span class="sxs-lookup"><span data-stu-id="88877-130">Attributes</span></span>

|<span data-ttu-id="88877-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="88877-131">**Attribute**</span></span>|<span data-ttu-id="88877-132">**型**</span><span class="sxs-lookup"><span data-stu-id="88877-132">**Type**</span></span>|<span data-ttu-id="88877-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="88877-133">**Required**</span></span>|<span data-ttu-id="88877-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="88877-134">**Description**</span></span>|<span data-ttu-id="88877-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="88877-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88877-136">Del</span><span class="sxs-lookup"><span data-stu-id="88877-136">Del</span></span>  <br/> |<span data-ttu-id="88877-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="88877-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="88877-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="88877-138">optional</span></span>  <br/> |<span data-ttu-id="88877-139">マスターシェイプから継承される行が削除されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="88877-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="88877-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="88877-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="88877-141">IX</span><span class="sxs-lookup"><span data-stu-id="88877-141">IX</span></span>  <br/> |<span data-ttu-id="88877-142">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="88877-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88877-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="88877-143">optional</span></span>  <br/> |<span data-ttu-id="88877-144">行の1から始まる識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="88877-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="88877-145">これは、同じセクションの他の識別子よりも大きい qiue-v である必要があります。IX 属性は、文字、接続、フィールド、FillGradient、Geometry、Layer、LineGradient、Paragraph、Reviewer、スクラッチ、およびタブセクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="88877-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="88877-146">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="88877-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="88877-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="88877-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88877-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="88877-148">LocalName</span></span>  <br/> |<span data-ttu-id="88877-149">xsd: string</span><span class="sxs-lookup"><span data-stu-id="88877-149">xsd:string</span></span>  <br/> |<span data-ttu-id="88877-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="88877-150">optional</span></span>  <br/> |<span data-ttu-id="88877-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="88877-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="88877-152">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="88877-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88877-153">N</span><span class="sxs-lookup"><span data-stu-id="88877-153">N</span></span>  <br/> |<span data-ttu-id="88877-154">xsd: string</span><span class="sxs-lookup"><span data-stu-id="88877-154">xsd:string</span></span>  <br/> |<span data-ttu-id="88877-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="88877-155">optional</span></span>  <br/> |<span data-ttu-id="88877-156">一意の言語に依存しない行の名前を指定します。N 属性は、User、Property、Actions、Control、Connection、Hyperlink、および ActionTag セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="88877-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="88877-157">行には、IX 属性または N 属性のいずれかのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="88877-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="88877-158">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="88877-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="88877-159">T</span><span class="sxs-lookup"><span data-stu-id="88877-159">T</span></span>  <br/> |<span data-ttu-id="88877-160">xsd: string</span><span class="sxs-lookup"><span data-stu-id="88877-160">xsd:string</span></span>  <br/> |<span data-ttu-id="88877-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="88877-161">optional</span></span>  <br/> |<span data-ttu-id="88877-162">Geometry の視覚化で使用される、行で表されるジオメトリックパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="88877-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="88877-163">T 属性は、[Geometry] セクションにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="88877-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="88877-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="88877-164">Values of the xsd:string type.</span></span>  <br/> |
   

