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
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a><span data-ttu-id="b380b-103">MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b380b-103">MasterShortcut element (Masters_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b380b-104">ドキュメントで定義されているマスター シェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="b380b-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b380b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b380b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b380b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b380b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b380b-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="b380b-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b380b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b380b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b380b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b380b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b380b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b380b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b380b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b380b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b380b-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="b380b-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b380b-113">定義</span><span class="sxs-lookup"><span data-stu-id="b380b-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b380b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b380b-114">Elements and attributes</span></span>

<span data-ttu-id="b380b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b380b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b380b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b380b-116">Parent elements</span></span>

|<span data-ttu-id="b380b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b380b-117">**Element**</span></span>|<span data-ttu-id="b380b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b380b-118">**Type**</span></span>|<span data-ttu-id="b380b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b380b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b380b-120">Masters</span><span class="sxs-lookup"><span data-stu-id="b380b-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="b380b-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="b380b-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b380b-122">ドキュメントの**マスター**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b380b-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b380b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b380b-123">Child elements</span></span>

|<span data-ttu-id="b380b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="b380b-124">**Element**</span></span>|<span data-ttu-id="b380b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="b380b-125">**Type**</span></span>|<span data-ttu-id="b380b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="b380b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b380b-127">Icon</span><span class="sxs-lookup"><span data-stu-id="b380b-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b380b-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="b380b-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b380b-129">エンコードされたバイナリ] アイコン (.ico 形式) をドキュメント内の**マスター シェイプ**または**MasterShortcut**要素の MIME (多目的インターネット メール拡張機能) を指定します。</span><span class="sxs-lookup"><span data-stu-id="b380b-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b380b-130">属性</span><span class="sxs-lookup"><span data-stu-id="b380b-130">Attributes</span></span>

|<span data-ttu-id="b380b-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="b380b-131">**Attribute**</span></span>|<span data-ttu-id="b380b-132">**型**</span><span class="sxs-lookup"><span data-stu-id="b380b-132">**Type**</span></span>|<span data-ttu-id="b380b-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="b380b-133">**Required**</span></span>|<span data-ttu-id="b380b-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="b380b-134">**Description**</span></span>|<span data-ttu-id="b380b-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="b380b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b380b-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="b380b-136">AlignName</span></span>  <br/> |<span data-ttu-id="b380b-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b380b-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b380b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-138">optional</span></span>  <br/> |<span data-ttu-id="b380b-139">ステンシル ウィンドウ内の要素のテキストが左、右揃えまたは中央揃えかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b380b-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="b380b-140">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b380b-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="b380b-141">IconSize</span></span>  <br/> |<span data-ttu-id="b380b-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b380b-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b380b-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-143">optional</span></span>  <br/> |<span data-ttu-id="b380b-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="b380b-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="b380b-145">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b380b-146">ID</span><span class="sxs-lookup"><span data-stu-id="b380b-146">ID</span></span>  <br/> |<span data-ttu-id="b380b-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b380b-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b380b-148">必須</span><span class="sxs-lookup"><span data-stu-id="b380b-148">required</span></span>  <br/> |<span data-ttu-id="b380b-149">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="b380b-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="b380b-150">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b380b-151">名前</span><span class="sxs-lookup"><span data-stu-id="b380b-151">Name</span></span>  <br/> |<span data-ttu-id="b380b-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b380b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="b380b-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-153">optional</span></span>  <br/> |<span data-ttu-id="b380b-154">要素の名前です。</span><span class="sxs-lookup"><span data-stu-id="b380b-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="b380b-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b380b-156">NameU</span><span class="sxs-lookup"><span data-stu-id="b380b-156">NameU</span></span>  <br/> |<span data-ttu-id="b380b-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b380b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="b380b-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-158">optional</span></span>  <br/> |<span data-ttu-id="b380b-159">要素の汎用名です。</span><span class="sxs-lookup"><span data-stu-id="b380b-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="b380b-160">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b380b-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="b380b-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="b380b-162">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b380b-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b380b-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-163">optional</span></span>  <br/> |<span data-ttu-id="b380b-164">マスターのユーザー設定のパターンとして動作するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b380b-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="b380b-165">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b380b-166">プロンプト</span><span class="sxs-lookup"><span data-stu-id="b380b-166">Prompt</span></span>  <br/> |<span data-ttu-id="b380b-167">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b380b-167">xsd:string</span></span>  <br/> |<span data-ttu-id="b380b-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-168">optional</span></span>  <br/> |<span data-ttu-id="b380b-169">ステータス バー、ツールは、要素の prompt ヒントです。</span><span class="sxs-lookup"><span data-stu-id="b380b-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="b380b-170">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b380b-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="b380b-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="b380b-172">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b380b-172">xsd:string</span></span>  <br/> |<span data-ttu-id="b380b-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-173">optional</span></span>  <br/> |<span data-ttu-id="b380b-174">要素のヘルプ文字列です。</span><span class="sxs-lookup"><span data-stu-id="b380b-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="b380b-175">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b380b-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="b380b-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="b380b-177">xsd:string</span><span class="sxs-lookup"><span data-stu-id="b380b-177">xsd:string</span></span>  <br/> |<span data-ttu-id="b380b-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="b380b-178">optional</span></span>  <br/> |<span data-ttu-id="b380b-179">**MasterShortcut**要素の URL です。</span><span class="sxs-lookup"><span data-stu-id="b380b-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="b380b-180">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b380b-180">Values of the xsd:string type.</span></span>  <br/> |
   

