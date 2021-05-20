---
title: VisioDocument 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Microsoft ドキュメントのルートVisioです。
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538488"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="f81d8-103">VisioDocument 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f81d8-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="f81d8-104">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="f81d8-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f81d8-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="f81d8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f81d8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f81d8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f81d8-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f81d8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f81d8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f81d8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f81d8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f81d8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f81d8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f81d8-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="f81d8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f81d8-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="f81d8-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f81d8-113">定義</span><span class="sxs-lookup"><span data-stu-id="f81d8-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f81d8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f81d8-114">Elements and attributes</span></span>

<span data-ttu-id="f81d8-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f81d8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f81d8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f81d8-116">Parent elements</span></span>

<span data-ttu-id="f81d8-117">なし。</span><span class="sxs-lookup"><span data-stu-id="f81d8-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f81d8-118">子要素</span><span class="sxs-lookup"><span data-stu-id="f81d8-118">Child elements</span></span>

|<span data-ttu-id="f81d8-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f81d8-119">**Element**</span></span>|<span data-ttu-id="f81d8-120">**型**</span><span class="sxs-lookup"><span data-stu-id="f81d8-120">**Type**</span></span>|<span data-ttu-id="f81d8-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="f81d8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f81d8-122">色</span><span class="sxs-lookup"><span data-stu-id="f81d8-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-124">ドキュメントのカラーテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f81d8-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="f81d8-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-127">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f81d8-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="f81d8-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-130">ドキュメントの **ShapeSheet 構造を指定** します。</span><span class="sxs-lookup"><span data-stu-id="f81d8-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-131">EventList</span><span class="sxs-lookup"><span data-stu-id="f81d8-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-133">オブジェクトが応答 **するイベントごとに EventItem** 要素を含む。</span><span class="sxs-lookup"><span data-stu-id="f81d8-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="f81d8-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-136">FaceName 要素のコレクション **を含** む。</span><span class="sxs-lookup"><span data-stu-id="f81d8-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="f81d8-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-139">ドキュメントのヘッダーとフッターの要素を含む。</span><span class="sxs-lookup"><span data-stu-id="f81d8-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="f81d8-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-142">表示可能な図面ページと、図面で更新可能なレコードセットのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="f81d8-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="f81d8-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="f81d8-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f81d8-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="f81d8-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f81d8-145">ドキュメントの StyleSheet 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="f81d8-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f81d8-146">属性</span><span class="sxs-lookup"><span data-stu-id="f81d8-146">Attributes</span></span>

<span data-ttu-id="f81d8-147">なし。</span><span class="sxs-lookup"><span data-stu-id="f81d8-147">None.</span></span>
  

