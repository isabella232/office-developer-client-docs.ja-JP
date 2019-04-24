---
title: PageSheet 要素 (Page_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: 図面ページに関連付けられた図面ページのプロパティを指定します。
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326118"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="3670a-103">PageSheet 要素 (Page_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3670a-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3670a-104">図面ページに関連付けられた図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3670a-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3670a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3670a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3670a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3670a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3670a-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="3670a-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3670a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3670a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3670a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3670a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3670a-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3670a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3670a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3670a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3670a-112">ページの xml</span><span class="sxs-lookup"><span data-stu-id="3670a-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3670a-113">定義</span><span class="sxs-lookup"><span data-stu-id="3670a-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3670a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3670a-114">Elements and attributes</span></span>

<span data-ttu-id="3670a-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3670a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3670a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3670a-116">Parent elements</span></span>

|<span data-ttu-id="3670a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3670a-117">**Element**</span></span>|<span data-ttu-id="3670a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3670a-118">**Type**</span></span>|<span data-ttu-id="3670a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3670a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3670a-120">Page</span><span class="sxs-lookup"><span data-stu-id="3670a-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3670a-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="3670a-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3670a-122">文書内のページを定義する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="3670a-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3670a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3670a-123">Child elements</span></span>

<span data-ttu-id="3670a-124">なし。</span><span class="sxs-lookup"><span data-stu-id="3670a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3670a-125">属性</span><span class="sxs-lookup"><span data-stu-id="3670a-125">Attributes</span></span>

|<span data-ttu-id="3670a-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="3670a-126">**Attribute**</span></span>|<span data-ttu-id="3670a-127">**型**</span><span class="sxs-lookup"><span data-stu-id="3670a-127">**Type**</span></span>|<span data-ttu-id="3670a-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="3670a-128">**Required**</span></span>|<span data-ttu-id="3670a-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3670a-129">**Description**</span></span>|<span data-ttu-id="3670a-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3670a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3670a-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="3670a-131">FillStyle</span></span>  <br/> |<span data-ttu-id="3670a-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3670a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3670a-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="3670a-133">optional</span></span>  <br/> |<span data-ttu-id="3670a-134">塗りつぶしの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3670a-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="3670a-135">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3670a-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="3670a-136">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3670a-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3670a-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="3670a-137">LineStyle</span></span>  <br/> |<span data-ttu-id="3670a-138">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3670a-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3670a-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="3670a-139">optional</span></span>  <br/> |<span data-ttu-id="3670a-140">線の書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3670a-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="3670a-141">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3670a-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="3670a-142">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3670a-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3670a-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="3670a-143">TextStyle</span></span>  <br/> |<span data-ttu-id="3670a-144">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="3670a-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3670a-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="3670a-145">optional</span></span>  <br/> |<span data-ttu-id="3670a-146">テキストの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="3670a-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="3670a-147">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3670a-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="3670a-148">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3670a-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3670a-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="3670a-149">UniqueID</span></span>  <br/> |<span data-ttu-id="3670a-150">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3670a-150">xsd:string</span></span>  <br/> |<span data-ttu-id="3670a-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="3670a-151">optional</span></span>  <br/> |<span data-ttu-id="3670a-152">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="3670a-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="3670a-153">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3670a-153">Values of the xsd:string type.</span></span>  <br/> |
   

