---
title: VisioDocument 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Microsoft Visio 図面のルート要素です。
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538488"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="5b287-103">VisioDocument 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5b287-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="5b287-104">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="5b287-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b287-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5b287-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b287-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5b287-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5b287-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b287-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5b287-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b287-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5b287-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5b287-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5b287-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b287-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5b287-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5b287-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="5b287-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b287-113">定義</span><span class="sxs-lookup"><span data-stu-id="5b287-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b287-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5b287-114">Elements and attributes</span></span>

<span data-ttu-id="5b287-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b287-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b287-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5b287-116">Parent elements</span></span>

<span data-ttu-id="5b287-117">なし。</span><span class="sxs-lookup"><span data-stu-id="5b287-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b287-118">子要素</span><span class="sxs-lookup"><span data-stu-id="5b287-118">Child elements</span></span>

|<span data-ttu-id="5b287-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b287-119">**Element**</span></span>|<span data-ttu-id="5b287-120">**型**</span><span class="sxs-lookup"><span data-stu-id="5b287-120">**Type**</span></span>|<span data-ttu-id="5b287-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b287-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b287-122">Colors</span><span class="sxs-lookup"><span data-stu-id="5b287-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-124">図面のカラーテーブルを含みます。</span><span class="sxs-lookup"><span data-stu-id="5b287-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="5b287-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="5b287-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-127">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="5b287-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="5b287-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="5b287-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-130">図面の**シェイプシート**の構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b287-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="5b287-131">EventList</span><span class="sxs-lookup"><span data-stu-id="5b287-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-133">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b287-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="5b287-134">FaceNames 方法</span><span class="sxs-lookup"><span data-stu-id="5b287-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-136">**Facename**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="5b287-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="5b287-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="5b287-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-139">文書のヘッダーとフッターの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="5b287-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="5b287-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="5b287-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-142">図面で更新可能な一連の図面ページを表示し、それらを表示することを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b287-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="5b287-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="5b287-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b287-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="5b287-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b287-145">文書の StyleSheet 要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b287-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5b287-146">属性</span><span class="sxs-lookup"><span data-stu-id="5b287-146">Attributes</span></span>

<span data-ttu-id="5b287-147">なし。</span><span class="sxs-lookup"><span data-stu-id="5b287-147">None.</span></span>
  

