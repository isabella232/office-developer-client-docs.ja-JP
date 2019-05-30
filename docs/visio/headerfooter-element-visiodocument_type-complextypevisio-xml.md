---
title: HeaderFooter 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: 文書のヘッダーとフッターの要素を格納します。
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541107"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="26841-103">HeaderFooter 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="26841-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="26841-104">文書のヘッダーとフッターの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26841-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="26841-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26841-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="26841-106">**Element type**</span></span> <br/> |[<span data-ttu-id="26841-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="26841-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="26841-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="26841-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="26841-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="26841-109">**Schema file**</span></span> <br/> |<span data-ttu-id="26841-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="26841-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="26841-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="26841-111">**Document parts**</span></span> <br/> |<span data-ttu-id="26841-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="26841-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="26841-113">定義</span><span class="sxs-lookup"><span data-stu-id="26841-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="26841-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="26841-114">Elements and attributes</span></span>

<span data-ttu-id="26841-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26841-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="26841-116">親要素</span><span class="sxs-lookup"><span data-stu-id="26841-116">Parent elements</span></span>

|<span data-ttu-id="26841-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="26841-117">**Element**</span></span>|<span data-ttu-id="26841-118">**型**</span><span class="sxs-lookup"><span data-stu-id="26841-118">**Type**</span></span>|<span data-ttu-id="26841-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="26841-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26841-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="26841-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="26841-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="26841-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="26841-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="26841-123">子要素</span><span class="sxs-lookup"><span data-stu-id="26841-123">Child elements</span></span>

|<span data-ttu-id="26841-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="26841-124">**Element**</span></span>|<span data-ttu-id="26841-125">**型**</span><span class="sxs-lookup"><span data-stu-id="26841-125">**Type**</span></span>|<span data-ttu-id="26841-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="26841-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26841-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="26841-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="26841-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-129">図面のフッターの中央部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="26841-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="26841-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="26841-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-132">ドキュメントのフッターの左側の部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="26841-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="26841-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="26841-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-135">文書のフッターの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="26841-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="26841-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="26841-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="26841-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-138">文書のフッターの右部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="26841-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="26841-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="26841-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-141">図面のヘッダーの中央に表示される文字列を含みます。</span><span class="sxs-lookup"><span data-stu-id="26841-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="26841-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="26841-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="26841-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-144">ヘッダーおよびフッターのテキストに使用されるフォントを指定します。</span><span class="sxs-lookup"><span data-stu-id="26841-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="26841-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="26841-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="26841-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-147">文書のヘッダーの左側の部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="26841-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="26841-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="26841-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-150">文書のヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="26841-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="26841-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="26841-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="26841-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="26841-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="26841-153">文書のヘッダーの右部分に表示されるテキスト文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="26841-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="26841-154">属性</span><span class="sxs-lookup"><span data-stu-id="26841-154">Attributes</span></span>

|<span data-ttu-id="26841-155">**属性**</span><span class="sxs-lookup"><span data-stu-id="26841-155">**Attribute**</span></span>|<span data-ttu-id="26841-156">**型**</span><span class="sxs-lookup"><span data-stu-id="26841-156">**Type**</span></span>|<span data-ttu-id="26841-157">**必須**</span><span class="sxs-lookup"><span data-stu-id="26841-157">**Required**</span></span>|<span data-ttu-id="26841-158">**説明**</span><span class="sxs-lookup"><span data-stu-id="26841-158">**Description**</span></span>|<span data-ttu-id="26841-159">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="26841-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26841-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="26841-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="26841-161">xsd: string</span><span class="sxs-lookup"><span data-stu-id="26841-161">xsd:string</span></span>  <br/> |<span data-ttu-id="26841-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="26841-162">optional</span></span>  <br/> |<span data-ttu-id="26841-163">ヘッダーおよびフッターのテキストの色の RGB 値 (16 進表記)。たとえば、#rrggbb のようにします。</span><span class="sxs-lookup"><span data-stu-id="26841-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="26841-164">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="26841-164">Values of the xsd:string type.</span></span>  <br/> |
   

