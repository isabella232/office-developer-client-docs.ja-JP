---
title: PageSheet 要素 (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: 図面ページに関連付けられた図面ページのプロパティを指定します。
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540624"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="c522e-103">PageSheet 要素 (Page_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c522e-103">PageSheet element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c522e-104">図面ページに関連付けられた図面ページのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="c522e-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c522e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c522e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c522e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c522e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c522e-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c522e-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c522e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c522e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c522e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c522e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c522e-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="c522e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c522e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c522e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c522e-112">ページの xml</span><span class="sxs-lookup"><span data-stu-id="c522e-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c522e-113">定義</span><span class="sxs-lookup"><span data-stu-id="c522e-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c522e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c522e-114">Elements and attributes</span></span>

<span data-ttu-id="c522e-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c522e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c522e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c522e-116">Parent elements</span></span>

|<span data-ttu-id="c522e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c522e-117">**Element**</span></span>|<span data-ttu-id="c522e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c522e-118">**Type**</span></span>|<span data-ttu-id="c522e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c522e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c522e-120">Page</span><span class="sxs-lookup"><span data-stu-id="c522e-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c522e-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="c522e-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c522e-122">文書内のページを定義する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="c522e-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c522e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c522e-123">Child elements</span></span>

<span data-ttu-id="c522e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="c522e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c522e-125">属性</span><span class="sxs-lookup"><span data-stu-id="c522e-125">Attributes</span></span>

|<span data-ttu-id="c522e-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="c522e-126">**Attribute**</span></span>|<span data-ttu-id="c522e-127">**型**</span><span class="sxs-lookup"><span data-stu-id="c522e-127">**Type**</span></span>|<span data-ttu-id="c522e-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="c522e-128">**Required**</span></span>|<span data-ttu-id="c522e-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="c522e-129">**Description**</span></span>|<span data-ttu-id="c522e-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c522e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c522e-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="c522e-131">FillStyle</span></span>  <br/> |<span data-ttu-id="c522e-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="c522e-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c522e-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="c522e-133">optional</span></span>  <br/> |<span data-ttu-id="c522e-134">塗りつぶしの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c522e-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="c522e-135">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c522e-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c522e-136">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c522e-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c522e-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="c522e-137">LineStyle</span></span>  <br/> |<span data-ttu-id="c522e-138">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="c522e-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c522e-139">省略可能</span><span class="sxs-lookup"><span data-stu-id="c522e-139">optional</span></span>  <br/> |<span data-ttu-id="c522e-140">線の書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c522e-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="c522e-141">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c522e-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c522e-142">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c522e-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c522e-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="c522e-143">TextStyle</span></span>  <br/> |<span data-ttu-id="c522e-144">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="c522e-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c522e-145">省略可能</span><span class="sxs-lookup"><span data-stu-id="c522e-145">optional</span></span>  <br/> |<span data-ttu-id="c522e-146">テキストの書式設定を継承するスタイルシートの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="c522e-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="c522e-147">図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c522e-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="c522e-148">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="c522e-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c522e-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c522e-149">UniqueID</span></span>  <br/> |<span data-ttu-id="c522e-150">xsd: string</span><span class="sxs-lookup"><span data-stu-id="c522e-150">xsd:string</span></span>  <br/> |<span data-ttu-id="c522e-151">省略可能</span><span class="sxs-lookup"><span data-stu-id="c522e-151">optional</span></span>  <br/> |<span data-ttu-id="c522e-152">親要素内の要素の一意の ID。</span><span class="sxs-lookup"><span data-stu-id="c522e-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="c522e-153">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c522e-153">Values of the xsd:string type.</span></span>  <br/> |
   

