---
title: PageSheet 要素 (Page_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: 図面ページに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395134"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="0eed3-103">PageSheet 要素 (Page_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0eed3-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0eed3-104">図面ページに関連付けられている図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0eed3-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0eed3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0eed3-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0eed3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0eed3-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0eed3-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0eed3-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0eed3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0eed3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0eed3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0eed3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0eed3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0eed3-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0eed3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0eed3-112">pages.xml</span><span class="sxs-lookup"><span data-stu-id="0eed3-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0eed3-113">定義</span><span class="sxs-lookup"><span data-stu-id="0eed3-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0eed3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0eed3-114">Elements and attributes</span></span>

<span data-ttu-id="0eed3-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0eed3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0eed3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0eed3-116">Parent elements</span></span>

|<span data-ttu-id="0eed3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0eed3-117">**Element**</span></span>|<span data-ttu-id="0eed3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0eed3-118">**Type**</span></span>|<span data-ttu-id="0eed3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0eed3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0eed3-120">Page</span><span class="sxs-lookup"><span data-stu-id="0eed3-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0eed3-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="0eed3-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0eed3-122">ドキュメント内のページを定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0eed3-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0eed3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0eed3-123">Child elements</span></span>

<span data-ttu-id="0eed3-124">なし。</span><span class="sxs-lookup"><span data-stu-id="0eed3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eed3-125">属性</span><span class="sxs-lookup"><span data-stu-id="0eed3-125">Attributes</span></span>

|<span data-ttu-id="0eed3-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="0eed3-126">**Attribute**</span></span>|<span data-ttu-id="0eed3-127">**型**</span><span class="sxs-lookup"><span data-stu-id="0eed3-127">**Type**</span></span>|<span data-ttu-id="0eed3-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="0eed3-128">**Required**</span></span>|<span data-ttu-id="0eed3-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="0eed3-129">**Description**</span></span>|<span data-ttu-id="0eed3-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0eed3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0eed3-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="0eed3-131">FillStyle</span></span>  <br/> |<span data-ttu-id="0eed3-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0eed3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0eed3-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="0eed3-133">optional</span></span>  <br/> |<span data-ttu-id="0eed3-134">塗りつぶしの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="0eed3-135">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0eed3-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="0eed3-136">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0eed3-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="0eed3-137">LineStyle</span></span>  <br/> |<span data-ttu-id="0eed3-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0eed3-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0eed3-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="0eed3-139">optional</span></span>  <br/> |<span data-ttu-id="0eed3-140">線の書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="0eed3-141">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0eed3-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="0eed3-142">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0eed3-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="0eed3-143">TextStyle</span></span>  <br/> |<span data-ttu-id="0eed3-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0eed3-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0eed3-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="0eed3-145">optional</span></span>  <br/> |<span data-ttu-id="0eed3-146">テキストの書式設定を継承するスタイル シートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="0eed3-147">図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0eed3-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="0eed3-148">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0eed3-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0eed3-149">UniqueID</span></span>  <br/> |<span data-ttu-id="0eed3-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0eed3-150">xsd:string</span></span>  <br/> |<span data-ttu-id="0eed3-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="0eed3-151">optional</span></span>  <br/> |<span data-ttu-id="0eed3-152">その親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="0eed3-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="0eed3-153">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0eed3-153">Values of the xsd:string type.</span></span>  <br/> |
   

