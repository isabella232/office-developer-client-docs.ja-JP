---
title: 行要素 (塗りつぶしグラデーション]) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: 塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。
ms.openlocfilehash: 55ec3b58f57d1fb008825c1a5a4156e5aec59552
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393776"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a><span data-ttu-id="473ea-103">行要素 (塗りつぶしグラデーション]) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="473ea-103">Row element (Fill Gradient Section) ('Visio XML')</span></span>

<span data-ttu-id="473ea-104">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="473ea-104">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="473ea-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="473ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="473ea-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="473ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="473ea-107">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="473ea-107">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="473ea-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="473ea-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="473ea-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="473ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="473ea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="473ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="473ea-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="473ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="473ea-112">document.xml、# .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="473ea-112">document.xml, master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="473ea-113">定義</span><span class="sxs-lookup"><span data-stu-id="473ea-113">Definition</span></span>

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="473ea-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="473ea-114">Elements and attributes</span></span>

<span data-ttu-id="473ea-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="473ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="473ea-116">親要素</span><span class="sxs-lookup"><span data-stu-id="473ea-116">Parent elements</span></span>

|<span data-ttu-id="473ea-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="473ea-117">**Element**</span></span>|<span data-ttu-id="473ea-118">**型**</span><span class="sxs-lookup"><span data-stu-id="473ea-118">**Type**</span></span>|<span data-ttu-id="473ea-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="473ea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="473ea-120">セクション</span><span class="sxs-lookup"><span data-stu-id="473ea-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="473ea-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="473ea-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="473ea-122">塗りつぶしのグラデーションに対する、グラデーションの分岐点の色、透過性、および位置を格納します。</span><span class="sxs-lookup"><span data-stu-id="473ea-122">Contains the color, transparency, and position of a gradient stop for a fill gradient.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="473ea-123">子要素</span><span class="sxs-lookup"><span data-stu-id="473ea-123">Child elements</span></span>

|<span data-ttu-id="473ea-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="473ea-124">**Element**</span></span>|<span data-ttu-id="473ea-125">**型**</span><span class="sxs-lookup"><span data-stu-id="473ea-125">**Type**</span></span>|<span data-ttu-id="473ea-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="473ea-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="473ea-127">Cell</span><span class="sxs-lookup"><span data-stu-id="473ea-127">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="473ea-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="473ea-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="473ea-129">1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="473ea-129">Specifies a single property.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="473ea-130">属性</span><span class="sxs-lookup"><span data-stu-id="473ea-130">Attributes</span></span>

|<span data-ttu-id="473ea-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="473ea-131">**Attribute**</span></span>|<span data-ttu-id="473ea-132">**型**</span><span class="sxs-lookup"><span data-stu-id="473ea-132">**Type**</span></span>|<span data-ttu-id="473ea-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="473ea-133">**Required**</span></span>|<span data-ttu-id="473ea-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="473ea-134">**Description**</span></span>|<span data-ttu-id="473ea-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="473ea-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="473ea-136">Del</span><span class="sxs-lookup"><span data-stu-id="473ea-136">Del</span></span>  <br/> |<span data-ttu-id="473ea-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="473ea-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="473ea-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="473ea-138">optional</span></span>  <br/> |<span data-ttu-id="473ea-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="473ea-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="473ea-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="473ea-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="473ea-141">IX</span><span class="sxs-lookup"><span data-stu-id="473ea-141">IX</span></span>  <br/> |<span data-ttu-id="473ea-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="473ea-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="473ea-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="473ea-143">optional</span></span>  <br/> |<span data-ttu-id="473ea-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="473ea-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="473ea-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="473ea-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="473ea-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="473ea-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="473ea-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="473ea-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="473ea-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="473ea-148">LocalName</span></span>  <br/> |<span data-ttu-id="473ea-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="473ea-149">xsd:string</span></span>  <br/> |<span data-ttu-id="473ea-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="473ea-150">optional</span></span>  <br/> |<span data-ttu-id="473ea-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="473ea-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="473ea-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="473ea-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="473ea-153">N</span><span class="sxs-lookup"><span data-stu-id="473ea-153">N</span></span>  <br/> |<span data-ttu-id="473ea-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="473ea-154">xsd:string</span></span>  <br/> |<span data-ttu-id="473ea-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="473ea-155">optional</span></span>  <br/> |<span data-ttu-id="473ea-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="473ea-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="473ea-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="473ea-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="473ea-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="473ea-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="473ea-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="473ea-159">T</span></span>  <br/> |<span data-ttu-id="473ea-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="473ea-160">xsd:string</span></span>  <br/> |<span data-ttu-id="473ea-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="473ea-161">optional</span></span>  <br/> |<span data-ttu-id="473ea-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="473ea-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="473ea-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="473ea-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="473ea-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="473ea-164">Values of the xsd:string type.</span></span>  <br/> |
   

