---
title: HeaderFooter 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: ドキュメントのヘッダーとフッターの要素が含まれています。
ms.openlocfilehash: e5933ad318b8100569046668e3cc372ce9a03788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805521"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="d7ef8-103">HeaderFooter 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d7ef8-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d7ef8-104">ドキュメントのヘッダーとフッターの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7ef8-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d7ef8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7ef8-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d7ef8-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d7ef8-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d7ef8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d7ef8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d7ef8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d7ef8-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d7ef8-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="d7ef8-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d7ef8-113">定義</span><span class="sxs-lookup"><span data-stu-id="d7ef8-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d7ef8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d7ef8-114">Elements and attributes</span></span>

<span data-ttu-id="d7ef8-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d7ef8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d7ef8-116">Parent elements</span></span>

|<span data-ttu-id="d7ef8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-117">**Element**</span></span>|<span data-ttu-id="d7ef8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-118">**Type**</span></span>|<span data-ttu-id="d7ef8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7ef8-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="d7ef8-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d7ef8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d7ef8-123">Child elements</span></span>

|<span data-ttu-id="d7ef8-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-124">**Element**</span></span>|<span data-ttu-id="d7ef8-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-125">**Type**</span></span>|<span data-ttu-id="d7ef8-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d7ef8-127">中央</span><span class="sxs-lookup"><span data-stu-id="d7ef8-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-129">図面のフッターの中央の部分に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="d7ef8-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-132">図面のフッターの左部分に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="d7ef8-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-135">図面のフッターの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-136">フッター</span><span class="sxs-lookup"><span data-stu-id="d7ef8-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-138">図面のフッターの右側に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="d7ef8-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-141">図面のヘッダーの中央の部分に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="d7ef8-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-144">ヘッダーおよびフッターのテキストに使用するフォントを指定します。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="d7ef8-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-147">図面のヘッダーの左側の部分に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="d7ef8-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-150">図面のヘッダーの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="d7ef8-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="d7ef8-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d7ef8-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="d7ef8-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d7ef8-153">図面のヘッダーの右側の部分に表示されるテキスト文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d7ef8-154">属性</span><span class="sxs-lookup"><span data-stu-id="d7ef8-154">Attributes</span></span>

|<span data-ttu-id="d7ef8-155">**属性**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-155">**Attribute**</span></span>|<span data-ttu-id="d7ef8-156">**型**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-156">**Type**</span></span>|<span data-ttu-id="d7ef8-157">**必須**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-157">**Required**</span></span>|<span data-ttu-id="d7ef8-158">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-158">**Description**</span></span>|<span data-ttu-id="d7ef8-159">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="d7ef8-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d7ef8-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="d7ef8-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="d7ef8-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d7ef8-161">xsd:string</span></span>  <br/> |<span data-ttu-id="d7ef8-162">省略可能</span><span class="sxs-lookup"><span data-stu-id="d7ef8-162">optional</span></span>  <br/> |<span data-ttu-id="d7ef8-163">ヘッダーとフッターを 16 進表記でのテキストの色の RGB 値たとえば、#rrggbb です。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="d7ef8-164">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7ef8-164">Values of the xsd:string type.</span></span>  <br/> |
   

