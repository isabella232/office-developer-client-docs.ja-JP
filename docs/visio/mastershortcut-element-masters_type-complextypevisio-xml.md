---
title: MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: ドキュメントで定義されているマスター シェイプのショートカットを指定します。
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805835"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a><span data-ttu-id="9831e-103">MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9831e-103">MasterShortcut element (Masters_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9831e-104">ドキュメントで定義されているマスター シェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="9831e-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9831e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9831e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9831e-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="9831e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9831e-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="9831e-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9831e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9831e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9831e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9831e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9831e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9831e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9831e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9831e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9831e-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="9831e-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9831e-113">定義</span><span class="sxs-lookup"><span data-stu-id="9831e-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9831e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9831e-114">Elements and attributes</span></span>

<span data-ttu-id="9831e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9831e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9831e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9831e-116">Parent elements</span></span>

|<span data-ttu-id="9831e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9831e-117">**Element**</span></span>|<span data-ttu-id="9831e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9831e-118">**Type**</span></span>|<span data-ttu-id="9831e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9831e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9831e-120">マスター</span><span class="sxs-lookup"><span data-stu-id="9831e-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="9831e-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="9831e-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9831e-122">ドキュメントの**マスター**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9831e-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9831e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9831e-123">Child elements</span></span>

|<span data-ttu-id="9831e-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="9831e-124">**Element**</span></span>|<span data-ttu-id="9831e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9831e-125">**Type**</span></span>|<span data-ttu-id="9831e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9831e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9831e-127">Icon</span><span class="sxs-lookup"><span data-stu-id="9831e-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9831e-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="9831e-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9831e-129">エンコードされたバイナリ] アイコン (.ico 形式) をドキュメント内の**マスター シェイプ**または**MasterShortcut**要素の MIME (多目的インターネット メール拡張機能) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9831e-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9831e-130">属性</span><span class="sxs-lookup"><span data-stu-id="9831e-130">Attributes</span></span>

|<span data-ttu-id="9831e-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="9831e-131">**Attribute**</span></span>|<span data-ttu-id="9831e-132">**型**</span><span class="sxs-lookup"><span data-stu-id="9831e-132">**Type**</span></span>|<span data-ttu-id="9831e-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="9831e-133">**Required**</span></span>|<span data-ttu-id="9831e-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="9831e-134">**Description**</span></span>|<span data-ttu-id="9831e-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9831e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9831e-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="9831e-136">AlignName</span></span>  <br/> |<span data-ttu-id="9831e-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9831e-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9831e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-138">optional</span></span>  <br/> |<span data-ttu-id="9831e-139">ステンシル ウィンドウ内の要素のテキストが左、右揃えまたは中央揃えかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9831e-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="9831e-140">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9831e-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="9831e-141">IconSize</span></span>  <br/> |<span data-ttu-id="9831e-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9831e-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9831e-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-143">optional</span></span>  <br/> |<span data-ttu-id="9831e-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="9831e-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="9831e-145">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9831e-146">ID</span><span class="sxs-lookup"><span data-stu-id="9831e-146">ID</span></span>  <br/> |<span data-ttu-id="9831e-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9831e-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9831e-148">必須</span><span class="sxs-lookup"><span data-stu-id="9831e-148">required</span></span>  <br/> |<span data-ttu-id="9831e-149">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="9831e-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="9831e-150">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9831e-151">名前</span><span class="sxs-lookup"><span data-stu-id="9831e-151">Name</span></span>  <br/> |<span data-ttu-id="9831e-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9831e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="9831e-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-153">optional</span></span>  <br/> |<span data-ttu-id="9831e-154">要素の名前です。</span><span class="sxs-lookup"><span data-stu-id="9831e-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="9831e-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9831e-156">NameU</span><span class="sxs-lookup"><span data-stu-id="9831e-156">NameU</span></span>  <br/> |<span data-ttu-id="9831e-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9831e-157">xsd:string</span></span>  <br/> |<span data-ttu-id="9831e-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-158">optional</span></span>  <br/> |<span data-ttu-id="9831e-159">要素の汎用名です。</span><span class="sxs-lookup"><span data-stu-id="9831e-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="9831e-160">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9831e-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="9831e-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="9831e-162">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9831e-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9831e-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-163">optional</span></span>  <br/> |<span data-ttu-id="9831e-164">マスターのユーザー設定のパターンとして動作するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="9831e-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="9831e-165">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9831e-166">Prompt</span><span class="sxs-lookup"><span data-stu-id="9831e-166">Prompt</span></span>  <br/> |<span data-ttu-id="9831e-167">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9831e-167">xsd:string</span></span>  <br/> |<span data-ttu-id="9831e-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-168">optional</span></span>  <br/> |<span data-ttu-id="9831e-169">ステータス バー、ツールは、要素の prompt ヒントです。</span><span class="sxs-lookup"><span data-stu-id="9831e-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="9831e-170">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9831e-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="9831e-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="9831e-172">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9831e-172">xsd:string</span></span>  <br/> |<span data-ttu-id="9831e-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-173">optional</span></span>  <br/> |<span data-ttu-id="9831e-174">要素のヘルプ文字列です。</span><span class="sxs-lookup"><span data-stu-id="9831e-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="9831e-175">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9831e-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="9831e-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="9831e-177">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9831e-177">xsd:string</span></span>  <br/> |<span data-ttu-id="9831e-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="9831e-178">optional</span></span>  <br/> |<span data-ttu-id="9831e-179">**MasterShortcut**要素の URL です。</span><span class="sxs-lookup"><span data-stu-id="9831e-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="9831e-180">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9831e-180">Values of the xsd:string type.</span></span>  <br/> |
   

