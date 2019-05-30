---
title: EventList 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: オブジェクトが応答する各イベントの EventItem 要素が含まれています。
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541800"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="aa161-103">EventList 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aa161-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="aa161-104">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa161-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="aa161-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="aa161-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa161-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="aa161-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aa161-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="aa161-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aa161-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="aa161-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aa161-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="aa161-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aa161-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="aa161-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aa161-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="aa161-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aa161-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="aa161-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aa161-113">定義</span><span class="sxs-lookup"><span data-stu-id="aa161-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aa161-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="aa161-114">Elements and attributes</span></span>

<span data-ttu-id="aa161-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa161-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aa161-116">親要素</span><span class="sxs-lookup"><span data-stu-id="aa161-116">Parent elements</span></span>

|<span data-ttu-id="aa161-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="aa161-117">**Element**</span></span>|<span data-ttu-id="aa161-118">**型**</span><span class="sxs-lookup"><span data-stu-id="aa161-118">**Type**</span></span>|<span data-ttu-id="aa161-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="aa161-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa161-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="aa161-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="aa161-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="aa161-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aa161-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="aa161-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aa161-123">子要素</span><span class="sxs-lookup"><span data-stu-id="aa161-123">Child elements</span></span>

|<span data-ttu-id="aa161-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="aa161-124">**Element**</span></span>|<span data-ttu-id="aa161-125">**型**</span><span class="sxs-lookup"><span data-stu-id="aa161-125">**Type**</span></span>|<span data-ttu-id="aa161-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="aa161-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa161-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="aa161-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aa161-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="aa161-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aa161-129">イベントコードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="aa161-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aa161-130">属性</span><span class="sxs-lookup"><span data-stu-id="aa161-130">Attributes</span></span>

<span data-ttu-id="aa161-131">なし。</span><span class="sxs-lookup"><span data-stu-id="aa161-131">None.</span></span>
  

