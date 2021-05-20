---
title: HeaderFooter 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: ドキュメントのヘッダーとフッターの要素を含む。
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541107"
---
# <a name="headerfooter-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="0dfac-103">HeaderFooter 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0dfac-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0dfac-104">ドキュメントのヘッダーとフッターの要素を含む。</span><span class="sxs-lookup"><span data-stu-id="0dfac-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dfac-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="0dfac-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dfac-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0dfac-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0dfac-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0dfac-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0dfac-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0dfac-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0dfac-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0dfac-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0dfac-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0dfac-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="0dfac-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0dfac-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="0dfac-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0dfac-113">定義</span><span class="sxs-lookup"><span data-stu-id="0dfac-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0dfac-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0dfac-114">Elements and attributes</span></span>

<span data-ttu-id="0dfac-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dfac-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0dfac-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0dfac-116">Parent elements</span></span>

|<span data-ttu-id="0dfac-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0dfac-117">**Element**</span></span>|<span data-ttu-id="0dfac-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0dfac-118">**Type**</span></span>|<span data-ttu-id="0dfac-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0dfac-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0dfac-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="0dfac-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="0dfac-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="0dfac-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0dfac-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0dfac-123">Child elements</span></span>

|<span data-ttu-id="0dfac-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dfac-124">**Element**</span></span>|<span data-ttu-id="0dfac-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0dfac-125">**Type**</span></span>|<span data-ttu-id="0dfac-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0dfac-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0dfac-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="0dfac-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-129">ドキュメントのフッターの中央部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="0dfac-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-132">ドキュメントのフッターの左側に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="0dfac-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-135">ドキュメントのフッターの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="0dfac-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-138">ドキュメントのフッターの右側に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="0dfac-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-141">図面のヘッダーの中央に表示される文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="0dfac-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="0dfac-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-144">ヘッダーおよびフッターのテキストに使用されるフォントを指定します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="0dfac-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-147">ドキュメントのヘッダーの左側に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="0dfac-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-150">ドキュメントのヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="0dfac-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="0dfac-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dfac-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="0dfac-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dfac-153">ドキュメントのヘッダーの右側に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0dfac-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0dfac-154">属性</span><span class="sxs-lookup"><span data-stu-id="0dfac-154">Attributes</span></span>

|<span data-ttu-id="0dfac-155">**属性**</span><span class="sxs-lookup"><span data-stu-id="0dfac-155">**Attribute**</span></span>|<span data-ttu-id="0dfac-156">**型**</span><span class="sxs-lookup"><span data-stu-id="0dfac-156">**Type**</span></span>|<span data-ttu-id="0dfac-157">**必須**</span><span class="sxs-lookup"><span data-stu-id="0dfac-157">**Required**</span></span>|<span data-ttu-id="0dfac-158">**説明**</span><span class="sxs-lookup"><span data-stu-id="0dfac-158">**Description**</span></span>|<span data-ttu-id="0dfac-159">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0dfac-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0dfac-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="0dfac-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="0dfac-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0dfac-161">xsd:string</span></span>  <br/> |<span data-ttu-id="0dfac-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="0dfac-162">optional</span></span>  <br/> |<span data-ttu-id="0dfac-163">ヘッダーとフッターのテキストの色の RGB 値を 16 進表記で指定します。たとえば、#rrggbb。</span><span class="sxs-lookup"><span data-stu-id="0dfac-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="0dfac-164">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0dfac-164">Values of the xsd:string type.</span></span>  <br/> |
   

