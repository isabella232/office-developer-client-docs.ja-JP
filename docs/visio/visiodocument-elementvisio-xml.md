---
title: VisioDocument 要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Microsoft Visio ドキュメントのルート要素です。
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391305"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="9fdb6-103">VisioDocument 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9fdb6-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="9fdb6-104">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fdb6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9fdb6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fdb6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fdb6-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fdb6-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fdb6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fdb6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9fdb6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fdb6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fdb6-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="9fdb6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fdb6-113">定義</span><span class="sxs-lookup"><span data-stu-id="9fdb6-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fdb6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9fdb6-114">Elements and attributes</span></span>

<span data-ttu-id="9fdb6-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fdb6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9fdb6-116">Parent elements</span></span>

<span data-ttu-id="9fdb6-117">なし。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fdb6-118">子要素</span><span class="sxs-lookup"><span data-stu-id="9fdb6-118">Child elements</span></span>

|<span data-ttu-id="9fdb6-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-119">**Element**</span></span>|<span data-ttu-id="9fdb6-120">**型**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-120">**Type**</span></span>|<span data-ttu-id="9fdb6-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fdb6-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fdb6-122">色</span><span class="sxs-lookup"><span data-stu-id="9fdb6-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-124">図面のカラー テーブルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="9fdb6-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-127">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="9fdb6-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-130">図面の**シェイプ シート**の構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-131">EventList</span><span class="sxs-lookup"><span data-stu-id="9fdb6-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-133">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="9fdb6-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-136">**フォント名**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="9fdb6-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-139">ドキュメントのヘッダーとフッターの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="9fdb6-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-142">図面ページを表示し、図面のデータを更新するレコード セットの設定のセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="9fdb6-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="9fdb6-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fdb6-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="9fdb6-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fdb6-145">ドキュメントのスタイル シートの要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9fdb6-146">属性</span><span class="sxs-lookup"><span data-stu-id="9fdb6-146">Attributes</span></span>

<span data-ttu-id="9fdb6-147">なし。</span><span class="sxs-lookup"><span data-stu-id="9fdb6-147">None.</span></span>
  

