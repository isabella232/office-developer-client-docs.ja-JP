---
title: MasterShortcut 要素 (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: ドキュメントで定義されているマスター ショートカットを指定します。
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538208"
---
# <a name="mastershortcut-element-masters_type-complextype-visio-xml"></a><span data-ttu-id="c29f8-103">MasterShortcut 要素 (Masters_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c29f8-103">MasterShortcut element (Masters_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c29f8-104">ドキュメントで定義されているマスター ショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="c29f8-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c29f8-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="c29f8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c29f8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c29f8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c29f8-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="c29f8-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c29f8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c29f8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c29f8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c29f8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c29f8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c29f8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c29f8-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="c29f8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c29f8-112">master#.xml</span><span class="sxs-lookup"><span data-stu-id="c29f8-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c29f8-113">定義</span><span class="sxs-lookup"><span data-stu-id="c29f8-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c29f8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c29f8-114">Elements and attributes</span></span>

<span data-ttu-id="c29f8-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c29f8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c29f8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c29f8-116">Parent elements</span></span>

|<span data-ttu-id="c29f8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c29f8-117">**Element**</span></span>|<span data-ttu-id="c29f8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c29f8-118">**Type**</span></span>|<span data-ttu-id="c29f8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c29f8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c29f8-120">Masters</span><span class="sxs-lookup"><span data-stu-id="c29f8-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="c29f8-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="c29f8-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c29f8-122">ドキュメントの **Master** 要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="c29f8-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c29f8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c29f8-123">Child elements</span></span>

|<span data-ttu-id="c29f8-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="c29f8-124">**Element**</span></span>|<span data-ttu-id="c29f8-125">**型**</span><span class="sxs-lookup"><span data-stu-id="c29f8-125">**Type**</span></span>|<span data-ttu-id="c29f8-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="c29f8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c29f8-127">Icon</span><span class="sxs-lookup"><span data-stu-id="c29f8-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c29f8-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="c29f8-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c29f8-129">ドキュメント内の Master 要素または **MasterShortcut** 要素の MIME (多目的インターネット メール拡張機能)エンコードされたバイナリ アイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="c29f8-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c29f8-130">属性</span><span class="sxs-lookup"><span data-stu-id="c29f8-130">Attributes</span></span>

|<span data-ttu-id="c29f8-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="c29f8-131">**Attribute**</span></span>|<span data-ttu-id="c29f8-132">**型**</span><span class="sxs-lookup"><span data-stu-id="c29f8-132">**Type**</span></span>|<span data-ttu-id="c29f8-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="c29f8-133">**Required**</span></span>|<span data-ttu-id="c29f8-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="c29f8-134">**Description**</span></span>|<span data-ttu-id="c29f8-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c29f8-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c29f8-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="c29f8-136">AlignName</span></span>  <br/> |<span data-ttu-id="c29f8-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c29f8-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c29f8-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-138">optional</span></span>  <br/> |<span data-ttu-id="c29f8-139">ステンシル ウィンドウ内の要素のテキストを左揃え、右揃え、中央揃えにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c29f8-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="c29f8-140">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="c29f8-141">IconSize</span></span>  <br/> |<span data-ttu-id="c29f8-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c29f8-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c29f8-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-143">optional</span></span>  <br/> |<span data-ttu-id="c29f8-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="c29f8-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="c29f8-145">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-146">ID</span><span class="sxs-lookup"><span data-stu-id="c29f8-146">ID</span></span>  <br/> |<span data-ttu-id="c29f8-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c29f8-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c29f8-148">必須</span><span class="sxs-lookup"><span data-stu-id="c29f8-148">required</span></span>  <br/> |<span data-ttu-id="c29f8-149">親要素内の要素の一意の ID です。</span><span class="sxs-lookup"><span data-stu-id="c29f8-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="c29f8-150">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-151">名前</span><span class="sxs-lookup"><span data-stu-id="c29f8-151">Name</span></span>  <br/> |<span data-ttu-id="c29f8-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c29f8-152">xsd:string</span></span>  <br/> |<span data-ttu-id="c29f8-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-153">optional</span></span>  <br/> |<span data-ttu-id="c29f8-154">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="c29f8-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="c29f8-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-156">NameU</span><span class="sxs-lookup"><span data-stu-id="c29f8-156">NameU</span></span>  <br/> |<span data-ttu-id="c29f8-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c29f8-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c29f8-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-158">optional</span></span>  <br/> |<span data-ttu-id="c29f8-159">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="c29f8-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="c29f8-160">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="c29f8-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="c29f8-162">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c29f8-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c29f8-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-163">optional</span></span>  <br/> |<span data-ttu-id="c29f8-164">マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c29f8-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="c29f8-165">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-166">プロンプト</span><span class="sxs-lookup"><span data-stu-id="c29f8-166">Prompt</span></span>  <br/> |<span data-ttu-id="c29f8-167">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c29f8-167">xsd:string</span></span>  <br/> |<span data-ttu-id="c29f8-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-168">optional</span></span>  <br/> |<span data-ttu-id="c29f8-169">要素のステータス バーとツール ヒントのプロンプト。</span><span class="sxs-lookup"><span data-stu-id="c29f8-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="c29f8-170">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="c29f8-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="c29f8-172">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c29f8-172">xsd:string</span></span>  <br/> |<span data-ttu-id="c29f8-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-173">optional</span></span>  <br/> |<span data-ttu-id="c29f8-174">要素のヘルプ文字列。</span><span class="sxs-lookup"><span data-stu-id="c29f8-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="c29f8-175">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c29f8-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="c29f8-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="c29f8-177">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c29f8-177">xsd:string</span></span>  <br/> |<span data-ttu-id="c29f8-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="c29f8-178">optional</span></span>  <br/> |<span data-ttu-id="c29f8-179">**MasterShortcut 要素への** URL。</span><span class="sxs-lookup"><span data-stu-id="c29f8-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="c29f8-180">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c29f8-180">Values of the xsd:string type.</span></span>  <br/> |
   

