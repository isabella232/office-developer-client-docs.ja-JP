---
title: EventList 要素 (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: オブジェクトが応答する各イベントの EventItem 要素が含まれています。
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351052"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="ad8af-103">EventList 要素 (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ad8af-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad8af-104">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad8af-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ad8af-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ad8af-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad8af-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ad8af-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad8af-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="ad8af-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad8af-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad8af-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad8af-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad8af-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad8af-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="ad8af-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad8af-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ad8af-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad8af-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="ad8af-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad8af-113">定義</span><span class="sxs-lookup"><span data-stu-id="ad8af-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad8af-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ad8af-114">Elements and attributes</span></span>

<span data-ttu-id="ad8af-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad8af-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad8af-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ad8af-116">Parent elements</span></span>

|<span data-ttu-id="ad8af-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ad8af-117">**Element**</span></span>|<span data-ttu-id="ad8af-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ad8af-118">**Type**</span></span>|<span data-ttu-id="ad8af-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad8af-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad8af-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="ad8af-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="ad8af-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="ad8af-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad8af-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="ad8af-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad8af-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ad8af-123">Child elements</span></span>

|<span data-ttu-id="ad8af-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad8af-124">**Element**</span></span>|<span data-ttu-id="ad8af-125">**型**</span><span class="sxs-lookup"><span data-stu-id="ad8af-125">**Type**</span></span>|<span data-ttu-id="ad8af-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad8af-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad8af-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="ad8af-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad8af-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="ad8af-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad8af-129">イベントコードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="ad8af-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad8af-130">属性</span><span class="sxs-lookup"><span data-stu-id="ad8af-130">Attributes</span></span>

<span data-ttu-id="ad8af-131">なし。</span><span class="sxs-lookup"><span data-stu-id="ad8af-131">None.</span></span>
  

