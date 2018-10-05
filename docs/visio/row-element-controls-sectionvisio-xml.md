---
title: 行要素 (コントロール セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb61870d-3f93-59e3-6671-e545c3a85718
description: 特定のコントロール ハンドルの図形に対して定義されているセルが含まれています。
ms.openlocfilehash: aa690bf70078a711dffca3f01b6e7acc05507bdd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386769"
---
# <a name="row-element-controls-section-visio-xml"></a><span data-ttu-id="f9072-103">行要素 (コントロール セクション)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="f9072-103">Row element (Controls Section) ('Visio XML')</span></span>

<span data-ttu-id="f9072-104">特定のコントロール ハンドルの図形に対して定義されているセルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9072-104">Contains the cells for a particular control handle defined for a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9072-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f9072-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9072-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f9072-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f9072-107">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="f9072-107">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f9072-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="f9072-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f9072-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f9072-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f9072-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f9072-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f9072-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="f9072-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f9072-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="f9072-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9072-113">定義</span><span class="sxs-lookup"><span data-stu-id="f9072-113">Definition</span></span>

```XML
< xs:element name="Row" type="ControlRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9072-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f9072-114">Elements and attributes</span></span>

<span data-ttu-id="f9072-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f9072-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f9072-116">Parent elements</span></span>

|<span data-ttu-id="f9072-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f9072-117">**Element**</span></span>|<span data-ttu-id="f9072-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f9072-118">**Type**</span></span>|<span data-ttu-id="f9072-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f9072-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9072-120">セクション</span><span class="sxs-lookup"><span data-stu-id="f9072-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9072-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="f9072-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9072-122">特定のコントロール ハンドルの図形に対して定義されているセルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9072-122">Contains the cells for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f9072-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f9072-123">Child elements</span></span>

|<span data-ttu-id="f9072-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="f9072-124">**Element**</span></span>|<span data-ttu-id="f9072-125">**型**</span><span class="sxs-lookup"><span data-stu-id="f9072-125">**Type**</span></span>|<span data-ttu-id="f9072-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="f9072-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9072-127">Cell</span><span class="sxs-lookup"><span data-stu-id="f9072-127">Cell</span></span>](cell-element-controls-rowvisio-xml.md) <br/> |[<span data-ttu-id="f9072-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f9072-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f9072-129">図形に対して定義されている特定のコントロール ハンドルのプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9072-129">Contains a property for a particular control handle defined for a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f9072-130">属性</span><span class="sxs-lookup"><span data-stu-id="f9072-130">Attributes</span></span>

|<span data-ttu-id="f9072-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="f9072-131">**Attribute**</span></span>|<span data-ttu-id="f9072-132">**型**</span><span class="sxs-lookup"><span data-stu-id="f9072-132">**Type**</span></span>|<span data-ttu-id="f9072-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="f9072-133">**Required**</span></span>|<span data-ttu-id="f9072-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="f9072-134">**Description**</span></span>|<span data-ttu-id="f9072-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="f9072-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f9072-136">Del</span><span class="sxs-lookup"><span data-stu-id="f9072-136">Del</span></span>  <br/> |<span data-ttu-id="f9072-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f9072-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f9072-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="f9072-138">optional</span></span>  <br/> |<span data-ttu-id="f9072-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f9072-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="f9072-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9072-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f9072-141">IX</span><span class="sxs-lookup"><span data-stu-id="f9072-141">IX</span></span>  <br/> |<span data-ttu-id="f9072-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f9072-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f9072-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="f9072-143">optional</span></span>  <br/> |<span data-ttu-id="f9072-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9072-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="f9072-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="f9072-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="f9072-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="f9072-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f9072-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9072-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f9072-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="f9072-148">LocalName</span></span>  <br/> |<span data-ttu-id="f9072-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f9072-149">xsd:string</span></span>  <br/> |<span data-ttu-id="f9072-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="f9072-150">optional</span></span>  <br/> |<span data-ttu-id="f9072-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9072-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="f9072-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9072-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f9072-153">N</span><span class="sxs-lookup"><span data-stu-id="f9072-153">N</span></span>  <br/> |<span data-ttu-id="f9072-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f9072-154">xsd:string</span></span>  <br/> |<span data-ttu-id="f9072-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="f9072-155">optional</span></span>  <br/> |<span data-ttu-id="f9072-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="f9072-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="f9072-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="f9072-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="f9072-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9072-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f9072-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="f9072-159">T</span></span>  <br/> |<span data-ttu-id="f9072-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="f9072-160">xsd:string</span></span>  <br/> |<span data-ttu-id="f9072-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="f9072-161">optional</span></span>  <br/> |<span data-ttu-id="f9072-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9072-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="f9072-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="f9072-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="f9072-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9072-164">Values of the xsd:string type.</span></span>  <br/> |
   

