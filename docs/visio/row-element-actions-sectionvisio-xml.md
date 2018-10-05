---
title: 行要素 ([操作] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: 図形またはページのショートカット メニューまたは操作タグ メニューのメニュー項目を説明する行が含まれています。
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388911"
---
# <a name="row-element-actions-section-visio-xml"></a><span data-ttu-id="59543-103">行要素 ([操作] セクション) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="59543-103">Row element (Actions Section) ('Visio XML')</span></span>

<span data-ttu-id="59543-104">図形またはページのショートカット メニューまたは操作タグ メニューのメニュー項目を説明する行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59543-104">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59543-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="59543-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59543-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="59543-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59543-107">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="59543-107">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59543-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="59543-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59543-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="59543-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59543-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="59543-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59543-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="59543-111">**Document parts**</span></span> <br/> |<span data-ttu-id="59543-112">ページ # .xml、masters.xml、マスターの # .xml、pages.xml</span><span class="sxs-lookup"><span data-stu-id="59543-112">masters.xml, master#.xml, pages.xml, page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59543-113">定義</span><span class="sxs-lookup"><span data-stu-id="59543-113">Definition</span></span>

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59543-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="59543-114">Elements and attributes</span></span>

<span data-ttu-id="59543-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59543-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59543-116">親要素</span><span class="sxs-lookup"><span data-stu-id="59543-116">Parent elements</span></span>

|<span data-ttu-id="59543-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="59543-117">**Element**</span></span>|<span data-ttu-id="59543-118">**型**</span><span class="sxs-lookup"><span data-stu-id="59543-118">**Type**</span></span>|<span data-ttu-id="59543-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="59543-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59543-120">セクション</span><span class="sxs-lookup"><span data-stu-id="59543-120">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59543-121">Section_Type</span><span class="sxs-lookup"><span data-stu-id="59543-121">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59543-122">図形またはページのショートカット メニューまたは操作タグ メニューのメニュー項目を説明する行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59543-122">Contains rows that describe menu items on a shortcut or action tag menu of a shape or page.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59543-123">子要素</span><span class="sxs-lookup"><span data-stu-id="59543-123">Child elements</span></span>

|<span data-ttu-id="59543-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="59543-124">**Element**</span></span>|<span data-ttu-id="59543-125">**型**</span><span class="sxs-lookup"><span data-stu-id="59543-125">**Type**</span></span>|<span data-ttu-id="59543-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="59543-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59543-127">Cell</span><span class="sxs-lookup"><span data-stu-id="59543-127">Cell</span></span>](cell-element-actions-rowvisio-xml.md) <br/> |[<span data-ttu-id="59543-128">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="59543-128">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59543-129">カスタム メニューのコマンドをショートカット メニューまたは操作タグに関連付けられているアクションの 1 つのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="59543-129">Specifies one property of an action associated with a custom command on a shortcut or action tag menu.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="59543-130">属性</span><span class="sxs-lookup"><span data-stu-id="59543-130">Attributes</span></span>

|<span data-ttu-id="59543-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="59543-131">**Attribute**</span></span>|<span data-ttu-id="59543-132">**型**</span><span class="sxs-lookup"><span data-stu-id="59543-132">**Type**</span></span>|<span data-ttu-id="59543-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="59543-133">**Required**</span></span>|<span data-ttu-id="59543-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="59543-134">**Description**</span></span>|<span data-ttu-id="59543-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="59543-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59543-136">Del</span><span class="sxs-lookup"><span data-stu-id="59543-136">Del</span></span>  <br/> |<span data-ttu-id="59543-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="59543-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="59543-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="59543-138">optional</span></span>  <br/> |<span data-ttu-id="59543-139">マスター シェイプから継承される行が削除されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="59543-139">Specifies whether a row that would otherwise be inherited from a master shape has been deleted.</span></span>  <br/> |<span data-ttu-id="59543-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59543-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="59543-141">IX</span><span class="sxs-lookup"><span data-stu-id="59543-141">IX</span></span>  <br/> |<span data-ttu-id="59543-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="59543-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59543-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="59543-143">optional</span></span>  <br/> |<span data-ttu-id="59543-144">1 から始まる行の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="59543-144">Specifies the one-based identifier for the row.</span></span> <span data-ttu-id="59543-145">特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="59543-145">It should be unqiue and greater than other identifiers in the same section.The IX attribute is only used for the Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch, and Tabs sections.</span></span> <span data-ttu-id="59543-146">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="59543-146">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="59543-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59543-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59543-148">LocalName</span><span class="sxs-lookup"><span data-stu-id="59543-148">LocalName</span></span>  <br/> |<span data-ttu-id="59543-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="59543-149">xsd:string</span></span>  <br/> |<span data-ttu-id="59543-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="59543-150">optional</span></span>  <br/> |<span data-ttu-id="59543-151">行の一意の言語に依存する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="59543-151">Specifies the unique language-dependent name of the row.</span></span>  <br/> |<span data-ttu-id="59543-152">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59543-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59543-153">N</span><span class="sxs-lookup"><span data-stu-id="59543-153">N</span></span>  <br/> |<span data-ttu-id="59543-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="59543-154">xsd:string</span></span>  <br/> |<span data-ttu-id="59543-155">省略可能</span><span class="sxs-lookup"><span data-stu-id="59543-155">optional</span></span>  <br/> |<span data-ttu-id="59543-156">行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="59543-156">Specifies the unique language-independent name of the row.The N attribute is only used for the User, Property, Actions, Control, Connection, Hyperlink, and ActionTag sections.</span></span> <span data-ttu-id="59543-157">行は、IX または N の属性の 1 つだけ配置できます。</span><span class="sxs-lookup"><span data-stu-id="59543-157">A row can only have one of the IX or N attributes.</span></span>  <br/> |<span data-ttu-id="59543-158">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59543-158">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59543-159">SV 要素</span><span class="sxs-lookup"><span data-stu-id="59543-159">T</span></span>  <br/> |<span data-ttu-id="59543-160">xsd:string</span><span class="sxs-lookup"><span data-stu-id="59543-160">xsd:string</span></span>  <br/> |<span data-ttu-id="59543-161">省略可能</span><span class="sxs-lookup"><span data-stu-id="59543-161">optional</span></span>  <br/> |<span data-ttu-id="59543-162">行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="59543-162">Specifies the type of the geometric path represented by the row and used in geometry visualization.</span></span> <span data-ttu-id="59543-163">T 属性は、[Geometry] セクションでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="59543-163">The T attribute is only used for the Geometry section.</span></span>  <br/> |<span data-ttu-id="59543-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59543-164">Values of the xsd:string type.</span></span>  <br/> |
   

