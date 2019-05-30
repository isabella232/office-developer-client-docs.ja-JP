---
title: MasterShortcut 要素 (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: 図面で定義されているマスターシェイプのショートカットを指定します。
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538208"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a><span data-ttu-id="2effa-103">MasterShortcut 要素 (Masters_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2effa-103">MasterShortcut element (Masters_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2effa-104">図面で定義されているマスターシェイプのショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="2effa-104">Specifies a master shortcut defined in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2effa-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="2effa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2effa-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2effa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2effa-107">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="2effa-107">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2effa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2effa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2effa-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2effa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2effa-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="2effa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2effa-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="2effa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2effa-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="2effa-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2effa-113">定義</span><span class="sxs-lookup"><span data-stu-id="2effa-113">Definition</span></span>

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2effa-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2effa-114">Elements and attributes</span></span>

<span data-ttu-id="2effa-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2effa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2effa-116">親要素</span><span class="sxs-lookup"><span data-stu-id="2effa-116">Parent elements</span></span>

|<span data-ttu-id="2effa-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="2effa-117">**Element**</span></span>|<span data-ttu-id="2effa-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2effa-118">**Type**</span></span>|<span data-ttu-id="2effa-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="2effa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2effa-120">Masters</span><span class="sxs-lookup"><span data-stu-id="2effa-120">Masters</span></span>](masters-elementvisio-xml.md) <br/> |[<span data-ttu-id="2effa-121">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="2effa-121">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2effa-122">文書の**マスター**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="2effa-122">Contains the **Master** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2effa-123">子要素</span><span class="sxs-lookup"><span data-stu-id="2effa-123">Child elements</span></span>

|<span data-ttu-id="2effa-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="2effa-124">**Element**</span></span>|<span data-ttu-id="2effa-125">**型**</span><span class="sxs-lookup"><span data-stu-id="2effa-125">**Type**</span></span>|<span data-ttu-id="2effa-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="2effa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2effa-127">Icon</span><span class="sxs-lookup"><span data-stu-id="2effa-127">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2effa-128">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="2effa-128">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2effa-129">ドキュメント内の**Master**または**mastershortcut**要素に対してエンコードされた、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。</span><span class="sxs-lookup"><span data-stu-id="2effa-129">Specifies a MIME (Multipurpose Internet Mail Extensions) encoded binary icon (in .ico format) for a **Master** or **MasterShortcut** element in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2effa-130">属性</span><span class="sxs-lookup"><span data-stu-id="2effa-130">Attributes</span></span>

|<span data-ttu-id="2effa-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="2effa-131">**Attribute**</span></span>|<span data-ttu-id="2effa-132">**型**</span><span class="sxs-lookup"><span data-stu-id="2effa-132">**Type**</span></span>|<span data-ttu-id="2effa-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="2effa-133">**Required**</span></span>|<span data-ttu-id="2effa-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="2effa-134">**Description**</span></span>|<span data-ttu-id="2effa-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="2effa-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2effa-136">AlignName</span><span class="sxs-lookup"><span data-stu-id="2effa-136">AlignName</span></span>  <br/> |<span data-ttu-id="2effa-137">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="2effa-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2effa-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-138">optional</span></span>  <br/> |<span data-ttu-id="2effa-139">ステンシルウィンドウ内の要素のテキストを左、右、または中央に配置するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2effa-139">Specifies whether the element's text in the stencil window is aligned left, right, or center.</span></span>  <br/> |<span data-ttu-id="2effa-140">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2effa-141">IconSize</span><span class="sxs-lookup"><span data-stu-id="2effa-141">IconSize</span></span>  <br/> |<span data-ttu-id="2effa-142">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="2effa-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2effa-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-143">optional</span></span>  <br/> |<span data-ttu-id="2effa-144">要素のアイコンのサイズ。</span><span class="sxs-lookup"><span data-stu-id="2effa-144">The size of the element's icon.</span></span>  <br/> |<span data-ttu-id="2effa-145">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2effa-146">ID</span><span class="sxs-lookup"><span data-stu-id="2effa-146">ID</span></span>  <br/> |<span data-ttu-id="2effa-147">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="2effa-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2effa-148">必須</span><span class="sxs-lookup"><span data-stu-id="2effa-148">required</span></span>  <br/> |<span data-ttu-id="2effa-149">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="2effa-149">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="2effa-150">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2effa-151">名前</span><span class="sxs-lookup"><span data-stu-id="2effa-151">Name</span></span>  <br/> |<span data-ttu-id="2effa-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2effa-152">xsd:string</span></span>  <br/> |<span data-ttu-id="2effa-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-153">optional</span></span>  <br/> |<span data-ttu-id="2effa-154">要素の名前。</span><span class="sxs-lookup"><span data-stu-id="2effa-154">The name of the element.</span></span>  <br/> |<span data-ttu-id="2effa-155">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2effa-156">NameU</span><span class="sxs-lookup"><span data-stu-id="2effa-156">NameU</span></span>  <br/> |<span data-ttu-id="2effa-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2effa-157">xsd:string</span></span>  <br/> |<span data-ttu-id="2effa-158">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-158">optional</span></span>  <br/> |<span data-ttu-id="2effa-159">要素の汎用名。</span><span class="sxs-lookup"><span data-stu-id="2effa-159">The universal name of the element.</span></span>  <br/> |<span data-ttu-id="2effa-160">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-160">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2effa-161">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="2effa-161">PatternFlags</span></span>  <br/> |<span data-ttu-id="2effa-162">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="2effa-162">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="2effa-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-163">optional</span></span>  <br/> |<span data-ttu-id="2effa-164">マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2effa-164">Determines whether a master behaves as a custom pattern.</span></span>  <br/> |<span data-ttu-id="2effa-165">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-165">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="2effa-166">プロンプト</span><span class="sxs-lookup"><span data-stu-id="2effa-166">Prompt</span></span>  <br/> |<span data-ttu-id="2effa-167">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2effa-167">xsd:string</span></span>  <br/> |<span data-ttu-id="2effa-168">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-168">optional</span></span>  <br/> |<span data-ttu-id="2effa-169">要素のステータスバーとツールヒントのプロンプト。</span><span class="sxs-lookup"><span data-stu-id="2effa-169">The status bar and tool tip prompt for the element.</span></span>  <br/> |<span data-ttu-id="2effa-170">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-170">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2effa-171">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="2effa-171">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="2effa-172">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2effa-172">xsd:string</span></span>  <br/> |<span data-ttu-id="2effa-173">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-173">optional</span></span>  <br/> |<span data-ttu-id="2effa-174">要素のヘルプ文字列。</span><span class="sxs-lookup"><span data-stu-id="2effa-174">A help string for the element.</span></span>  <br/> |<span data-ttu-id="2effa-175">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2effa-176">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="2effa-176">ShortcutURL</span></span>  <br/> |<span data-ttu-id="2effa-177">xsd: string</span><span class="sxs-lookup"><span data-stu-id="2effa-177">xsd:string</span></span>  <br/> |<span data-ttu-id="2effa-178">省略可能</span><span class="sxs-lookup"><span data-stu-id="2effa-178">optional</span></span>  <br/> |<span data-ttu-id="2effa-179">**Mastershortcut**要素の URL。</span><span class="sxs-lookup"><span data-stu-id="2effa-179">A URL to a **MasterShortcut** element.</span></span>  <br/> |<span data-ttu-id="2effa-180">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2effa-180">Values of the xsd:string type.</span></span>  <br/> |
   

