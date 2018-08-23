---
title: EventList 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: オブジェクトが応答する各イベントの EventItem 要素が含まれています。
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805322"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="47c02-103">EventList 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="47c02-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="47c02-104">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="47c02-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="47c02-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="47c02-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47c02-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="47c02-106">**Element type**</span></span> <br/> |[<span data-ttu-id="47c02-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="47c02-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="47c02-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="47c02-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="47c02-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="47c02-109">**Schema file**</span></span> <br/> |<span data-ttu-id="47c02-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="47c02-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="47c02-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="47c02-111">**Document parts**</span></span> <br/> |<span data-ttu-id="47c02-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="47c02-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47c02-113">定義</span><span class="sxs-lookup"><span data-stu-id="47c02-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="47c02-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="47c02-114">Elements and attributes</span></span>

<span data-ttu-id="47c02-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c02-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="47c02-116">親要素</span><span class="sxs-lookup"><span data-stu-id="47c02-116">Parent elements</span></span>

|<span data-ttu-id="47c02-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="47c02-117">**Element**</span></span>|<span data-ttu-id="47c02-118">**型**</span><span class="sxs-lookup"><span data-stu-id="47c02-118">**Type**</span></span>|<span data-ttu-id="47c02-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="47c02-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47c02-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="47c02-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="47c02-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="47c02-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47c02-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="47c02-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="47c02-123">子要素</span><span class="sxs-lookup"><span data-stu-id="47c02-123">Child elements</span></span>

|<span data-ttu-id="47c02-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="47c02-124">**Element**</span></span>|<span data-ttu-id="47c02-125">**型**</span><span class="sxs-lookup"><span data-stu-id="47c02-125">**Type**</span></span>|<span data-ttu-id="47c02-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="47c02-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="47c02-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="47c02-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="47c02-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="47c02-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="47c02-129">イベント コードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="47c02-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="47c02-130">属性</span><span class="sxs-lookup"><span data-stu-id="47c02-130">Attributes</span></span>

<span data-ttu-id="47c02-131">なし。</span><span class="sxs-lookup"><span data-stu-id="47c02-131">None.</span></span>
  

