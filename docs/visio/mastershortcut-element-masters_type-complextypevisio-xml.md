---
title: MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: ドキュメントで定義されているマスター シェイプのショートカットを指定します。
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392957"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a><span data-ttu-id="d40ab-103">MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d40ab-103">MasterShortcut element (Masters_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d40ab-104">ドキュメントで定義されているマスター シェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d40ab-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d40ab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d40ab-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d40ab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d40ab-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="d40ab-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d40ab-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d40ab-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d40ab-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d40ab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d40ab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d40ab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d40ab-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d40ab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d40ab-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="d40ab-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d40ab-113">定義</span><span class="sxs-lookup"><span data-stu-id="d40ab-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d40ab-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d40ab-114">Elements and attributes</span></span>

<span data-ttu-id="d40ab-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d40ab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d40ab-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d40ab-116">Parent elements</span></span>

|<span data-ttu-id="d40ab-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d40ab-117">**Element**</span></span>|<span data-ttu-id="d40ab-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d40ab-118">**Type**</span></span>|<span data-ttu-id="d40ab-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d40ab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d40ab-120">Masters</span><span class="sxs-lookup"><span data-stu-id="d40ab-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="d40ab-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="d40ab-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d40ab-122">ドキュメントの**マスター**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d40ab-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d40ab-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d40ab-123">Child elements</span></span>

|<span data-ttu-id="d40ab-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="d40ab-124">**Element**</span></span>|<span data-ttu-id="d40ab-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d40ab-125">**Type**</span></span>|<span data-ttu-id="d40ab-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d40ab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d40ab-127">Icon</span><span class="sxs-lookup"><span data-stu-id="d40ab-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d40ab-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="d40ab-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d40ab-129">エンコードされたバイナリ] アイコン (.ico 形式) をドキュメント内の**マスター シェイプ**または**MasterShortcut**要素の MIME (多目的インターネット メール拡張機能) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d40ab-130">属性</span><span class="sxs-lookup"><span data-stu-id="d40ab-130">Attributes</span></span>

|<span data-ttu-id="d40ab-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="d40ab-131">**Attribute**</span></span>|<span data-ttu-id="d40ab-132">**型**</span><span class="sxs-lookup"><span data-stu-id="d40ab-132">**Type**</span></span>|<span data-ttu-id="d40ab-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="d40ab-133">**Required**</span></span>|<span data-ttu-id="d40ab-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="d40ab-134">**Description**</span></span>|<span data-ttu-id="d40ab-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d40ab-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d40ab-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="d40ab-136">AlignName</span></span>  <br/> |<span data-ttu-id="d40ab-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d40ab-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d40ab-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-138">optional</span></span>  <br/> |<span data-ttu-id="d40ab-139">ステンシル ウィンドウ内の要素のテキストが左、右揃えまたは中央揃えかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="d40ab-140">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="d40ab-141">IconSize</span></span>  <br/> |<span data-ttu-id="d40ab-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d40ab-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d40ab-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-143">optional</span></span>  <br/> |<span data-ttu-id="d40ab-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="d40ab-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="d40ab-145">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-146">ID</span><span class="sxs-lookup"><span data-stu-id="d40ab-146">ID</span></span>  <br/> |<span data-ttu-id="d40ab-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d40ab-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d40ab-148">必須</span><span class="sxs-lookup"><span data-stu-id="d40ab-148">required</span></span>  <br/> |<span data-ttu-id="d40ab-149">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="d40ab-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="d40ab-150">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-151">名前</span><span class="sxs-lookup"><span data-stu-id="d40ab-151">Name</span></span>  <br/> |<span data-ttu-id="d40ab-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d40ab-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d40ab-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-153">optional</span></span>  <br/> |<span data-ttu-id="d40ab-154">要素の名前です。</span><span class="sxs-lookup"><span data-stu-id="d40ab-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="d40ab-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-156">NameU</span><span class="sxs-lookup"><span data-stu-id="d40ab-156">NameU</span></span>  <br/> |<span data-ttu-id="d40ab-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d40ab-157">xsd:string</span></span>  <br/> |<span data-ttu-id="d40ab-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-158">optional</span></span>  <br/> |<span data-ttu-id="d40ab-159">要素の汎用名です。</span><span class="sxs-lookup"><span data-stu-id="d40ab-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="d40ab-160">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="d40ab-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="d40ab-162">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d40ab-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d40ab-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-163">optional</span></span>  <br/> |<span data-ttu-id="d40ab-164">マスターのユーザー設定のパターンとして動作するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="d40ab-165">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-166">プロンプト</span><span class="sxs-lookup"><span data-stu-id="d40ab-166">Prompt</span></span>  <br/> |<span data-ttu-id="d40ab-167">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d40ab-167">xsd:string</span></span>  <br/> |<span data-ttu-id="d40ab-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-168">optional</span></span>  <br/> |<span data-ttu-id="d40ab-169">ステータス バー、ツールは、要素の prompt ヒントです。</span><span class="sxs-lookup"><span data-stu-id="d40ab-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="d40ab-170">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="d40ab-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="d40ab-172">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d40ab-172">xsd:string</span></span>  <br/> |<span data-ttu-id="d40ab-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-173">optional</span></span>  <br/> |<span data-ttu-id="d40ab-174">要素のヘルプ文字列です。</span><span class="sxs-lookup"><span data-stu-id="d40ab-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="d40ab-175">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d40ab-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="d40ab-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="d40ab-177">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d40ab-177">xsd:string</span></span>  <br/> |<span data-ttu-id="d40ab-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="d40ab-178">optional</span></span>  <br/> |<span data-ttu-id="d40ab-179">**MasterShortcut**要素の URL です。</span><span class="sxs-lookup"><span data-stu-id="d40ab-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="d40ab-180">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d40ab-180">Values of the xsd:string type.</span></span>  <br/> |
   

