---
title: 行要素 (接続部分) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f44fc18-4757-7aba-8778-a474ab93a78d
description: X 座標または y 座標、水平方向と垂直方向、および図形上の 1 つの接続ポイントの型が含まれています。
ms.openlocfilehash: d06a51e52f2b5273171d068f6fc2a6bf5227eed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806274"
---
# <a name="row-element-connection-section-visio-xml"></a><span data-ttu-id="69b0b-103">行要素 (接続部分) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="69b0b-103">Row element (Connection Section) ('Visio XML')</span></span>

<span data-ttu-id="69b0b-104">X 座標または y 座標、水平方向と垂直方向、および図形上の 1 つの接続ポイントの型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69b0b-104">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69b0b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="69b0b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69b0b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="69b0b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="69b0b-107">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="69b0b-107">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="69b0b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="69b0b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="69b0b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="69b0b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="69b0b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="69b0b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="69b0b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="69b0b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="69b0b-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="69b0b-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69b0b-113">定義</span><span class="sxs-lookup"><span data-stu-id="69b0b-113">Definition</span></span>

```XML
< xs:element name="Row" type="ConnectionRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="69b0b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="69b0b-114">Elements and attributes</span></span>

<span data-ttu-id="69b0b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="69b0b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="69b0b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="69b0b-116">Parent elements</span></span>

|<span data-ttu-id="69b0b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="69b0b-117">**Element**</span></span>|<span data-ttu-id="69b0b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="69b0b-118">**Type**</span></span>|<span data-ttu-id="69b0b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="69b0b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69b0b-120">セクション</span><span class="sxs-lookup"><span data-stu-id="69b0b-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69b0b-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="69b0b-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="69b0b-122">X 座標または y 座標、水平方向と垂直方向、および図形上の 1 つの接続ポイントの型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69b0b-122">Contains the x- or y-coordinates, horizontal and vertical direction, and type for a single connection point on a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="69b0b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="69b0b-123">Child elements</span></span>

|<span data-ttu-id="69b0b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="69b0b-124">**Element**</span></span>|<span data-ttu-id="69b0b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="69b0b-125">**Type**</span></span>|<span data-ttu-id="69b0b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="69b0b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69b0b-127">Cell</span><span class="sxs-lookup"><span data-stu-id="69b0b-127">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="69b0b-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="69b0b-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="69b0b-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="69b0b-130">属性</span><span class="sxs-lookup"><span data-stu-id="69b0b-130">Attributes</span></span>

|<span data-ttu-id="69b0b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="69b0b-131">**Attribute**</span></span>|<span data-ttu-id="69b0b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="69b0b-132">**Type**</span></span>|<span data-ttu-id="69b0b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="69b0b-133">**Required**</span></span>|<span data-ttu-id="69b0b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="69b0b-134">**Description**</span></span>|<span data-ttu-id="69b0b-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="69b0b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69b0b-136">Del</span><span class="sxs-lookup"><span data-stu-id="69b0b-136">Del</span></span>  <br/> |<span data-ttu-id="69b0b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="69b0b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69b0b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="69b0b-138">optional</span></span>  <br/> |<span data-ttu-id="69b0b-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="69b0b-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="69b0b-141">IX</span><span class="sxs-lookup"><span data-stu-id="69b0b-141">IX</span></span>  <br/> |<span data-ttu-id="69b0b-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69b0b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69b0b-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="69b0b-143">optional</span></span>  <br/> |<span data-ttu-id="69b0b-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="69b0b-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="69b0b-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="69b0b-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="69b0b-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69b0b-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="69b0b-148">LocalName</span></span>  <br/> |<span data-ttu-id="69b0b-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="69b0b-149">xsd:string</span></span>  <br/> |<span data-ttu-id="69b0b-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="69b0b-150">optional</span></span>  <br/> |<span data-ttu-id="69b0b-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="69b0b-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69b0b-153">N</span><span class="sxs-lookup"><span data-stu-id="69b0b-153">N</span></span>  <br/> |<span data-ttu-id="69b0b-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="69b0b-154">xsd:string</span></span>  <br/> |<span data-ttu-id="69b0b-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="69b0b-155">optional</span></span>  <br/> |<span data-ttu-id="69b0b-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="69b0b-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="69b0b-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="69b0b-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="69b0b-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="69b0b-159">T</span></span>  <br/> |<span data-ttu-id="69b0b-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="69b0b-160">xsd:string</span></span>  <br/> |<span data-ttu-id="69b0b-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="69b0b-161">optional</span></span>  <br/> |<span data-ttu-id="69b0b-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="69b0b-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="69b0b-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="69b0b-164">Values of the xsd:string type.</span></span>  <br/> |
   

