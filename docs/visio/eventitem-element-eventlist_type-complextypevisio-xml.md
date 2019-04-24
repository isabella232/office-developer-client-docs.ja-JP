---
title: EventItem 要素 (EventList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベントコードをカプセル化します。
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337199"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="d6976-103">EventItem 要素 (EventList_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d6976-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d6976-104">イベントコードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="d6976-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6976-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d6976-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6976-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d6976-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d6976-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="d6976-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d6976-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6976-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d6976-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d6976-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d6976-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d6976-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d6976-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d6976-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d6976-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="d6976-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6976-113">定義</span><span class="sxs-lookup"><span data-stu-id="d6976-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6976-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d6976-114">Elements and attributes</span></span>

<span data-ttu-id="d6976-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6976-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d6976-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d6976-116">Parent elements</span></span>

|<span data-ttu-id="d6976-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d6976-117">**Element**</span></span>|<span data-ttu-id="d6976-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d6976-118">**Type**</span></span>|<span data-ttu-id="d6976-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6976-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6976-120">EventList</span><span class="sxs-lookup"><span data-stu-id="d6976-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6976-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="d6976-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6976-122">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d6976-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d6976-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d6976-123">Child elements</span></span>

<span data-ttu-id="d6976-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d6976-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6976-125">属性</span><span class="sxs-lookup"><span data-stu-id="d6976-125">Attributes</span></span>

|<span data-ttu-id="d6976-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="d6976-126">**Attribute**</span></span>|<span data-ttu-id="d6976-127">**型**</span><span class="sxs-lookup"><span data-stu-id="d6976-127">**Type**</span></span>|<span data-ttu-id="d6976-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="d6976-128">**Required**</span></span>|<span data-ttu-id="d6976-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6976-129">**Description**</span></span>|<span data-ttu-id="d6976-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d6976-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6976-131">アクション</span><span class="sxs-lookup"><span data-stu-id="d6976-131">Action</span></span>  <br/> |<span data-ttu-id="d6976-132">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="d6976-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d6976-133">必須</span><span class="sxs-lookup"><span data-stu-id="d6976-133">required</span></span>  <br/> |<span data-ttu-id="d6976-134">親**EventItem**要素のアクションコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="d6976-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="d6976-135">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d6976-136">有効</span><span class="sxs-lookup"><span data-stu-id="d6976-136">Enabled</span></span>  <br/> |<span data-ttu-id="d6976-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="d6976-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d6976-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d6976-138">optional</span></span>  <br/> |<span data-ttu-id="d6976-139">イベントが有効であるか無効であるかを示すフラグを表します。</span><span class="sxs-lookup"><span data-stu-id="d6976-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="d6976-140">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d6976-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="d6976-141">EventCode</span></span>  <br/> |<span data-ttu-id="d6976-142">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="d6976-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d6976-143">必須</span><span class="sxs-lookup"><span data-stu-id="d6976-143">required</span></span>  <br/> |<span data-ttu-id="d6976-144">アドオンをトリガーするイベントを示すコード。</span><span class="sxs-lookup"><span data-stu-id="d6976-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="d6976-145">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d6976-146">ID</span><span class="sxs-lookup"><span data-stu-id="d6976-146">ID</span></span>  <br/> |<span data-ttu-id="d6976-147">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d6976-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d6976-148">必須</span><span class="sxs-lookup"><span data-stu-id="d6976-148">required</span></span>  <br/> |<span data-ttu-id="d6976-149">イベントの ID。</span><span class="sxs-lookup"><span data-stu-id="d6976-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="d6976-150">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d6976-151">Target</span><span class="sxs-lookup"><span data-stu-id="d6976-151">Target</span></span>  <br/> |<span data-ttu-id="d6976-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d6976-152">xsd:string</span></span>  <br/> |<span data-ttu-id="d6976-153">必須</span><span class="sxs-lookup"><span data-stu-id="d6976-153">required</span></span>  <br/> |<span data-ttu-id="d6976-154">イベントのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="d6976-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="d6976-155">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d6976-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="d6976-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="d6976-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d6976-157">xsd:string</span></span>  <br/> |<span data-ttu-id="d6976-158">必須</span><span class="sxs-lookup"><span data-stu-id="d6976-158">required</span></span>  <br/> |<span data-ttu-id="d6976-159">イベントのターゲットに送信する引数を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6976-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="d6976-160">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d6976-160">Values of the xsd:string type.</span></span>  <br/> |
   

