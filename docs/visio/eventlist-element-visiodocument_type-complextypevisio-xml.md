---
title: EventList 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: オブジェクトが応答するイベントごとに EventItem 要素を含む。
ms.openlocfilehash: 7b1406f56dddd8507e330aa93d5cfe9f390caf21
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541800"
---
# <a name="eventlist-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="55a94-103">EventList 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="55a94-103">EventList element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="55a94-104">オブジェクトが応答 **するイベントごとに EventItem** 要素を含む。</span><span class="sxs-lookup"><span data-stu-id="55a94-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="55a94-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="55a94-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55a94-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="55a94-106">**Element type**</span></span> <br/> |[<span data-ttu-id="55a94-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="55a94-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="55a94-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="55a94-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="55a94-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="55a94-109">**Schema file**</span></span> <br/> |<span data-ttu-id="55a94-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="55a94-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="55a94-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="55a94-111">**Document parts**</span></span> <br/> |<span data-ttu-id="55a94-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="55a94-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55a94-113">定義</span><span class="sxs-lookup"><span data-stu-id="55a94-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="55a94-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="55a94-114">Elements and attributes</span></span>

<span data-ttu-id="55a94-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="55a94-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="55a94-116">親要素</span><span class="sxs-lookup"><span data-stu-id="55a94-116">Parent elements</span></span>

|<span data-ttu-id="55a94-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="55a94-117">**Element**</span></span>|<span data-ttu-id="55a94-118">**型**</span><span class="sxs-lookup"><span data-stu-id="55a94-118">**Type**</span></span>|<span data-ttu-id="55a94-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="55a94-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55a94-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="55a94-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="55a94-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="55a94-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55a94-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="55a94-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55a94-123">子要素</span><span class="sxs-lookup"><span data-stu-id="55a94-123">Child elements</span></span>

|<span data-ttu-id="55a94-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="55a94-124">**Element**</span></span>|<span data-ttu-id="55a94-125">**型**</span><span class="sxs-lookup"><span data-stu-id="55a94-125">**Type**</span></span>|<span data-ttu-id="55a94-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="55a94-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55a94-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="55a94-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55a94-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="55a94-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="55a94-129">イベント コードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="55a94-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="55a94-130">属性</span><span class="sxs-lookup"><span data-stu-id="55a94-130">Attributes</span></span>

<span data-ttu-id="55a94-131">なし。</span><span class="sxs-lookup"><span data-stu-id="55a94-131">None.</span></span>
  

