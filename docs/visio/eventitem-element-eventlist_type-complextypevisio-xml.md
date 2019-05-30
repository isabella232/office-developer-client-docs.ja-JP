---
title: EventItem 要素 (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベントコードをカプセル化します。
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541842"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="3d8f0-103">EventItem 要素 (EventList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="3d8f0-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="3d8f0-104">イベントコードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d8f0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3d8f0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d8f0-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3d8f0-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="3d8f0-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3d8f0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3d8f0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3d8f0-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3d8f0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3d8f0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3d8f0-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="3d8f0-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3d8f0-113">定義</span><span class="sxs-lookup"><span data-stu-id="3d8f0-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3d8f0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3d8f0-114">Elements and attributes</span></span>

<span data-ttu-id="3d8f0-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3d8f0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3d8f0-116">Parent elements</span></span>

|<span data-ttu-id="3d8f0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-117">**Element**</span></span>|<span data-ttu-id="3d8f0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-118">**Type**</span></span>|<span data-ttu-id="3d8f0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3d8f0-120">EventList</span><span class="sxs-lookup"><span data-stu-id="3d8f0-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3d8f0-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="3d8f0-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3d8f0-122">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3d8f0-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3d8f0-123">Child elements</span></span>

<span data-ttu-id="3d8f0-124">なし。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d8f0-125">属性</span><span class="sxs-lookup"><span data-stu-id="3d8f0-125">Attributes</span></span>

|<span data-ttu-id="3d8f0-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-126">**Attribute**</span></span>|<span data-ttu-id="3d8f0-127">**型**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-127">**Type**</span></span>|<span data-ttu-id="3d8f0-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-128">**Required**</span></span>|<span data-ttu-id="3d8f0-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-129">**Description**</span></span>|<span data-ttu-id="3d8f0-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="3d8f0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3d8f0-131">Action</span><span class="sxs-lookup"><span data-stu-id="3d8f0-131">Action</span></span>  <br/> |<span data-ttu-id="3d8f0-132">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="3d8f0-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3d8f0-133">必須</span><span class="sxs-lookup"><span data-stu-id="3d8f0-133">required</span></span>  <br/> |<span data-ttu-id="3d8f0-134">親**EventItem**要素のアクションコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="3d8f0-135">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3d8f0-136">有効</span><span class="sxs-lookup"><span data-stu-id="3d8f0-136">Enabled</span></span>  <br/> |<span data-ttu-id="3d8f0-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="3d8f0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3d8f0-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="3d8f0-138">optional</span></span>  <br/> |<span data-ttu-id="3d8f0-139">イベントが有効であるか無効であるかを示すフラグを表します。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="3d8f0-140">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3d8f0-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="3d8f0-141">EventCode</span></span>  <br/> |<span data-ttu-id="3d8f0-142">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="3d8f0-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3d8f0-143">必須</span><span class="sxs-lookup"><span data-stu-id="3d8f0-143">required</span></span>  <br/> |<span data-ttu-id="3d8f0-144">アドオンをトリガーするイベントを示すコード。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="3d8f0-145">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3d8f0-146">ID</span><span class="sxs-lookup"><span data-stu-id="3d8f0-146">ID</span></span>  <br/> |<span data-ttu-id="3d8f0-147">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="3d8f0-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3d8f0-148">必須</span><span class="sxs-lookup"><span data-stu-id="3d8f0-148">required</span></span>  <br/> |<span data-ttu-id="3d8f0-149">イベントの ID。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="3d8f0-150">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3d8f0-151">Target</span><span class="sxs-lookup"><span data-stu-id="3d8f0-151">Target</span></span>  <br/> |<span data-ttu-id="3d8f0-152">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3d8f0-152">xsd:string</span></span>  <br/> |<span data-ttu-id="3d8f0-153">必須</span><span class="sxs-lookup"><span data-stu-id="3d8f0-153">required</span></span>  <br/> |<span data-ttu-id="3d8f0-154">イベントのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="3d8f0-155">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3d8f0-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="3d8f0-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="3d8f0-157">xsd: string</span><span class="sxs-lookup"><span data-stu-id="3d8f0-157">xsd:string</span></span>  <br/> |<span data-ttu-id="3d8f0-158">必須</span><span class="sxs-lookup"><span data-stu-id="3d8f0-158">required</span></span>  <br/> |<span data-ttu-id="3d8f0-159">イベントのターゲットに送信する引数を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="3d8f0-160">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="3d8f0-160">Values of the xsd:string type.</span></span>  <br/> |
   

