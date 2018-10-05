---
title: 行要素 (図形データ セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: データを図形に関連付けるための 1 つの図形データの入力を指定します。
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385509"
---
# <a name="row-element-shape-data-section-visio-xml"></a><span data-ttu-id="d9035-103">行要素 (図形データ セクション)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d9035-103">Row element (Shape Data Section) ('Visio XML')</span></span>

<span data-ttu-id="d9035-104">データを図形に関連付けるための 1 つの図形データの入力を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-104">Specifies one shape data entry for associating data with a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9035-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d9035-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9035-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d9035-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d9035-107">Data_Type を図形します。</span><span class="sxs-lookup"><span data-stu-id="d9035-107">Shape Data_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d9035-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d9035-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d9035-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d9035-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d9035-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d9035-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d9035-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d9035-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d9035-112"># .xml をマスター、# .xml のページ</span><span class="sxs-lookup"><span data-stu-id="d9035-112">master#.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9035-113">定義</span><span class="sxs-lookup"><span data-stu-id="d9035-113">Definition</span></span>

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d9035-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d9035-114">Elements and attributes</span></span>

<span data-ttu-id="d9035-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9035-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d9035-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d9035-116">Parent elements</span></span>

|<span data-ttu-id="d9035-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d9035-117">**Element**</span></span>|<span data-ttu-id="d9035-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d9035-118">**Type**</span></span>|<span data-ttu-id="d9035-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9035-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9035-120">セクション</span><span class="sxs-lookup"><span data-stu-id="d9035-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9035-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="d9035-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9035-122">データを図形に関連付けるための 1 つの図形データの入力を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-122">Specifies one shape data entry for associating data with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d9035-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d9035-123">Child elements</span></span>

|<span data-ttu-id="d9035-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="d9035-124">**Element**</span></span>|<span data-ttu-id="d9035-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d9035-125">**Type**</span></span>|<span data-ttu-id="d9035-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9035-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9035-127">Cell</span><span class="sxs-lookup"><span data-stu-id="d9035-127">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="d9035-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d9035-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9035-129">図形データの 1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-129">Specifies one property of the shape data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d9035-130">属性</span><span class="sxs-lookup"><span data-stu-id="d9035-130">Attributes</span></span>

|<span data-ttu-id="d9035-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="d9035-131">**Attribute**</span></span>|<span data-ttu-id="d9035-132">**型**</span><span class="sxs-lookup"><span data-stu-id="d9035-132">**Type**</span></span>|<span data-ttu-id="d9035-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="d9035-133">**Required**</span></span>|<span data-ttu-id="d9035-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9035-134">**Description**</span></span>|<span data-ttu-id="d9035-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d9035-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d9035-136">Del</span><span class="sxs-lookup"><span data-stu-id="d9035-136">Del</span></span>  <br/> |<span data-ttu-id="d9035-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d9035-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d9035-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d9035-138">optional</span></span>  <br/> |<span data-ttu-id="d9035-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="d9035-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9035-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d9035-141">IX</span><span class="sxs-lookup"><span data-stu-id="d9035-141">IX</span></span>  <br/> |<span data-ttu-id="d9035-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9035-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9035-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="d9035-143">optional</span></span>  <br/> |<span data-ttu-id="d9035-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="d9035-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="d9035-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="d9035-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="d9035-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d9035-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9035-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9035-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="d9035-148">LocalName</span></span>  <br/> |<span data-ttu-id="d9035-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d9035-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d9035-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="d9035-150">optional</span></span>  <br/> |<span data-ttu-id="d9035-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="d9035-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9035-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d9035-153">N</span><span class="sxs-lookup"><span data-stu-id="d9035-153">N</span></span>  <br/> |<span data-ttu-id="d9035-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d9035-154">xsd:string</span></span>  <br/> |<span data-ttu-id="d9035-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="d9035-155">optional</span></span>  <br/> |<span data-ttu-id="d9035-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="d9035-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="d9035-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="d9035-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="d9035-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9035-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d9035-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="d9035-159">T</span></span>  <br/> |<span data-ttu-id="d9035-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d9035-160">xsd:string</span></span>  <br/> |<span data-ttu-id="d9035-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="d9035-161">optional</span></span>  <br/> |<span data-ttu-id="d9035-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9035-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="d9035-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="d9035-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="d9035-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9035-164">Values of the xsd:string type.</span></span>  <br/> |
   

