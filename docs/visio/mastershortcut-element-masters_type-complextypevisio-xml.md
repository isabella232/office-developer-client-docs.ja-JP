---
title: mastershortcut 要素 (Masters_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: 図面で定義されているマスターシェイプのショートカットを指定します。
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341735"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a><span data-ttu-id="0da07-103">mastershortcut 要素 (Masters_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0da07-103">MasterShortcut element (Masters_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0da07-104">図面で定義されているマスターシェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="0da07-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0da07-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0da07-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0da07-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0da07-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0da07-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="0da07-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0da07-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0da07-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0da07-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0da07-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0da07-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="0da07-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0da07-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0da07-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0da07-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="0da07-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0da07-113">定義</span><span class="sxs-lookup"><span data-stu-id="0da07-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0da07-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0da07-114">Elements and attributes</span></span>

<span data-ttu-id="0da07-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0da07-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0da07-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0da07-116">Parent elements</span></span>

|<span data-ttu-id="0da07-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0da07-117">**Element**</span></span>|<span data-ttu-id="0da07-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0da07-118">**Type**</span></span>|<span data-ttu-id="0da07-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0da07-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0da07-120">Masters</span><span class="sxs-lookup"><span data-stu-id="0da07-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="0da07-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="0da07-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0da07-122">文書の**マスター**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="0da07-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0da07-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0da07-123">Child elements</span></span>

|<span data-ttu-id="0da07-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0da07-124">**Element**</span></span>|<span data-ttu-id="0da07-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0da07-125">**Type**</span></span>|<span data-ttu-id="0da07-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0da07-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0da07-127">Icon</span><span class="sxs-lookup"><span data-stu-id="0da07-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0da07-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="0da07-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0da07-129">ドキュメント内の**Master**または**mastershortcut**要素に対してエンコードされた、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="0da07-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0da07-130">属性</span><span class="sxs-lookup"><span data-stu-id="0da07-130">Attributes</span></span>

|<span data-ttu-id="0da07-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="0da07-131">**Attribute**</span></span>|<span data-ttu-id="0da07-132">**型**</span><span class="sxs-lookup"><span data-stu-id="0da07-132">**Type**</span></span>|<span data-ttu-id="0da07-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="0da07-133">**Required**</span></span>|<span data-ttu-id="0da07-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="0da07-134">**Description**</span></span>|<span data-ttu-id="0da07-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0da07-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0da07-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="0da07-136">AlignName</span></span>  <br/> |<span data-ttu-id="0da07-137">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="0da07-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0da07-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-138">optional</span></span>  <br/> |<span data-ttu-id="0da07-139">ステンシルウィンドウ内の要素のテキストを左、右、または中央に配置するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0da07-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="0da07-140">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0da07-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="0da07-141">IconSize</span></span>  <br/> |<span data-ttu-id="0da07-142">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="0da07-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0da07-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-143">optional</span></span>  <br/> |<span data-ttu-id="0da07-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="0da07-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="0da07-145">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0da07-146">ID</span><span class="sxs-lookup"><span data-stu-id="0da07-146">ID</span></span>  <br/> |<span data-ttu-id="0da07-147">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="0da07-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0da07-148">必須</span><span class="sxs-lookup"><span data-stu-id="0da07-148">required</span></span>  <br/> |<span data-ttu-id="0da07-149">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="0da07-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="0da07-150">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0da07-151">名前</span><span class="sxs-lookup"><span data-stu-id="0da07-151">Name</span></span>  <br/> |<span data-ttu-id="0da07-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0da07-152">xsd:string</span></span>  <br/> |<span data-ttu-id="0da07-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-153">optional</span></span>  <br/> |<span data-ttu-id="0da07-154">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="0da07-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="0da07-155">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0da07-156">NameU</span><span class="sxs-lookup"><span data-stu-id="0da07-156">NameU</span></span>  <br/> |<span data-ttu-id="0da07-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0da07-157">xsd:string</span></span>  <br/> |<span data-ttu-id="0da07-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-158">optional</span></span>  <br/> |<span data-ttu-id="0da07-159">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="0da07-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="0da07-160">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0da07-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="0da07-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="0da07-162">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="0da07-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0da07-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-163">optional</span></span>  <br/> |<span data-ttu-id="0da07-164">マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="0da07-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="0da07-165">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0da07-166">プロンプト</span><span class="sxs-lookup"><span data-stu-id="0da07-166">Prompt</span></span>  <br/> |<span data-ttu-id="0da07-167">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0da07-167">xsd:string</span></span>  <br/> |<span data-ttu-id="0da07-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-168">optional</span></span>  <br/> |<span data-ttu-id="0da07-169">要素のステータスバーとツールヒントのプロンプト。</span><span class="sxs-lookup"><span data-stu-id="0da07-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="0da07-170">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0da07-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="0da07-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="0da07-172">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0da07-172">xsd:string</span></span>  <br/> |<span data-ttu-id="0da07-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-173">optional</span></span>  <br/> |<span data-ttu-id="0da07-174">要素のヘルプ文字列。</span><span class="sxs-lookup"><span data-stu-id="0da07-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="0da07-175">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0da07-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="0da07-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="0da07-177">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0da07-177">xsd:string</span></span>  <br/> |<span data-ttu-id="0da07-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="0da07-178">optional</span></span>  <br/> |<span data-ttu-id="0da07-179">**mastershortcut**要素の URL。</span><span class="sxs-lookup"><span data-stu-id="0da07-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="0da07-180">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0da07-180">Values of the xsd:string type.</span></span>  <br/> |
   

