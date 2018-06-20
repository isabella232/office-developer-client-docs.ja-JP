---
title: 行要素 (レイヤー ・ セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b884be2-3eed-0864-6a6c-877b43d9065f
description: 1 つのレイヤーとページのプロパティを定義する要素が含まれています。
ms.openlocfilehash: ed8368c0c7215068cbbfcdd89c1f5b56969b5a06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806308"
---
# <a name="row-element-layer-section-visio-xml"></a><span data-ttu-id="7196b-103">行要素 (レイヤー ・ セクション)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="7196b-103">Row element (Layer Section) ('Visio XML')</span></span>

<span data-ttu-id="7196b-104">1 つのレイヤーとページのプロパティを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7196b-104">Contains elements that define a single layer and its properties for a page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7196b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="7196b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7196b-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="7196b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7196b-107">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="7196b-107">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7196b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="7196b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7196b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7196b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7196b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7196b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7196b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="7196b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7196b-112">masters.xml、pages.xml</span><span class="sxs-lookup"><span data-stu-id="7196b-112">masters.xml, pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7196b-113">定義</span><span class="sxs-lookup"><span data-stu-id="7196b-113">Definition</span></span>

```XML
< xs:element name="Row" type="LayerRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7196b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7196b-114">Elements and attributes</span></span>

<span data-ttu-id="7196b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7196b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7196b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7196b-116">Parent elements</span></span>

|<span data-ttu-id="7196b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="7196b-117">**Element**</span></span>|<span data-ttu-id="7196b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="7196b-118">**Type**</span></span>|<span data-ttu-id="7196b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7196b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7196b-120">Section</span><span class="sxs-lookup"><span data-stu-id="7196b-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7196b-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7196b-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7196b-122">1 つのレイヤーとページのプロパティを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7196b-122">Contains elements that define a single layer and its properties for a page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7196b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="7196b-123">Child elements</span></span>

|<span data-ttu-id="7196b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="7196b-124">**Element**</span></span>|<span data-ttu-id="7196b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="7196b-125">**Type**</span></span>|<span data-ttu-id="7196b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="7196b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7196b-127">Cell</span><span class="sxs-lookup"><span data-stu-id="7196b-127">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7196b-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7196b-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7196b-129">レイヤーの 1 つのプロパティ ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="7196b-129">Specifies one property for a layer or its properties for a page.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7196b-130">属性</span><span class="sxs-lookup"><span data-stu-id="7196b-130">Attributes</span></span>

|<span data-ttu-id="7196b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="7196b-131">**Attribute**</span></span>|<span data-ttu-id="7196b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="7196b-132">**Type**</span></span>|<span data-ttu-id="7196b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="7196b-133">**Required**</span></span>|<span data-ttu-id="7196b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="7196b-134">**Description**</span></span>|<span data-ttu-id="7196b-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="7196b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7196b-136">Del</span><span class="sxs-lookup"><span data-stu-id="7196b-136">Del</span></span>  <br/> |<span data-ttu-id="7196b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7196b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7196b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="7196b-138">optional</span></span>  <br/> |<span data-ttu-id="7196b-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7196b-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="7196b-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7196b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7196b-141">IX</span><span class="sxs-lookup"><span data-stu-id="7196b-141">IX</span></span>  <br/> |<span data-ttu-id="7196b-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7196b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7196b-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="7196b-143">optional</span></span>  <br/> |<span data-ttu-id="7196b-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="7196b-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="7196b-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="7196b-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="7196b-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="7196b-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7196b-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7196b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7196b-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="7196b-148">LocalName</span></span>  <br/> |<span data-ttu-id="7196b-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7196b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7196b-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="7196b-150">optional</span></span>  <br/> |<span data-ttu-id="7196b-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="7196b-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="7196b-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7196b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7196b-153">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="7196b-153">N</span></span>  <br/> |<span data-ttu-id="7196b-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7196b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="7196b-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="7196b-155">optional</span></span>  <br/> |<span data-ttu-id="7196b-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="7196b-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="7196b-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="7196b-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="7196b-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7196b-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7196b-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="7196b-159">T</span></span>  <br/> |<span data-ttu-id="7196b-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7196b-160">xsd:string</span></span>  <br/> |<span data-ttu-id="7196b-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="7196b-161">optional</span></span>  <br/> |<span data-ttu-id="7196b-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="7196b-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="7196b-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="7196b-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="7196b-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7196b-164">Values of the xsd:string type.</span></span>  <br/> |
   

