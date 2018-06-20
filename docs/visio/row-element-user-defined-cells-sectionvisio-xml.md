---
title: 行要素 (ユーザー定義セル-部分) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。
ms.openlocfilehash: 10a0e0e5f7255274de528a34d5faa2de6137446e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806299"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a><span data-ttu-id="e5d91-103">行要素 (ユーザー定義セル-部分) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e5d91-103">Row element (User-defined Cells Section) ('Visio XML')</span></span>

<span data-ttu-id="e5d91-104">ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。</span><span class="sxs-lookup"><span data-stu-id="e5d91-104">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5d91-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e5d91-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5d91-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="e5d91-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e5d91-107">UserRow_Type</span><span class="sxs-lookup"><span data-stu-id="e5d91-107">UserRow_Type</span></span>](userrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e5d91-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e5d91-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e5d91-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e5d91-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e5d91-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e5d91-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e5d91-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e5d91-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e5d91-112">document.xml、masters.xml、マスターの # .xml、pages.xml ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="e5d91-112">document.xml, masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5d91-113">定義</span><span class="sxs-lookup"><span data-stu-id="e5d91-113">Definition</span></span>

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5d91-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e5d91-114">Elements and attributes</span></span>

<span data-ttu-id="e5d91-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5d91-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e5d91-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e5d91-116">Parent elements</span></span>

|<span data-ttu-id="e5d91-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e5d91-117">**Element**</span></span>|<span data-ttu-id="e5d91-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e5d91-118">**Type**</span></span>|<span data-ttu-id="e5d91-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5d91-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5d91-120">Section</span><span class="sxs-lookup"><span data-stu-id="e5d91-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5d91-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="e5d91-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e5d91-122">ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。</span><span class="sxs-lookup"><span data-stu-id="e5d91-122">A user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e5d91-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e5d91-123">Child elements</span></span>

|<span data-ttu-id="e5d91-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="e5d91-124">**Element**</span></span>|<span data-ttu-id="e5d91-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e5d91-125">**Type**</span></span>|<span data-ttu-id="e5d91-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5d91-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5d91-127">Cell</span><span class="sxs-lookup"><span data-stu-id="e5d91-127">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e5d91-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e5d91-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e5d91-129">1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。</span><span class="sxs-lookup"><span data-stu-id="e5d91-129">One property of a user-specified piece of information that can be referred to by other cells and add-on tools.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e5d91-130">属性</span><span class="sxs-lookup"><span data-stu-id="e5d91-130">Attributes</span></span>

|<span data-ttu-id="e5d91-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="e5d91-131">**Attribute**</span></span>|<span data-ttu-id="e5d91-132">**型**</span><span class="sxs-lookup"><span data-stu-id="e5d91-132">**Type**</span></span>|<span data-ttu-id="e5d91-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="e5d91-133">**Required**</span></span>|<span data-ttu-id="e5d91-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="e5d91-134">**Description**</span></span>|<span data-ttu-id="e5d91-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="e5d91-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e5d91-136">Del</span><span class="sxs-lookup"><span data-stu-id="e5d91-136">Del</span></span>  <br/> |<span data-ttu-id="e5d91-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e5d91-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e5d91-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="e5d91-138">optional</span></span>  <br/> |<span data-ttu-id="e5d91-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="e5d91-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e5d91-141">IX</span><span class="sxs-lookup"><span data-stu-id="e5d91-141">IX</span></span>  <br/> |<span data-ttu-id="e5d91-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e5d91-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e5d91-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="e5d91-143">optional</span></span>  <br/> |<span data-ttu-id="e5d91-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="e5d91-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="e5d91-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="e5d91-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e5d91-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e5d91-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="e5d91-148">LocalName</span></span>  <br/> |<span data-ttu-id="e5d91-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e5d91-149">xsd:string</span></span>  <br/> |<span data-ttu-id="e5d91-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="e5d91-150">optional</span></span>  <br/> |<span data-ttu-id="e5d91-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="e5d91-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5d91-153">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="e5d91-153">N</span></span>  <br/> |<span data-ttu-id="e5d91-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e5d91-154">xsd:string</span></span>  <br/> |<span data-ttu-id="e5d91-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="e5d91-155">optional</span></span>  <br/> |<span data-ttu-id="e5d91-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="e5d91-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="e5d91-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="e5d91-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e5d91-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="e5d91-159">T</span></span>  <br/> |<span data-ttu-id="e5d91-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e5d91-160">xsd:string</span></span>  <br/> |<span data-ttu-id="e5d91-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="e5d91-161">optional</span></span>  <br/> |<span data-ttu-id="e5d91-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="e5d91-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="e5d91-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d91-164">Values of the xsd:string type.</span></span>  <br/> |
   

