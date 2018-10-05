---
title: EventItem 要素 (EventList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベント コードをカプセル化します。
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394399"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="975bf-103">EventItem 要素 (EventList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="975bf-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="975bf-104">イベント コードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="975bf-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="975bf-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="975bf-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="975bf-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="975bf-106">**Element type**</span></span> <br/> |[<span data-ttu-id="975bf-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="975bf-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="975bf-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="975bf-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="975bf-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="975bf-109">**Schema file**</span></span> <br/> |<span data-ttu-id="975bf-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="975bf-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="975bf-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="975bf-111">**Document parts**</span></span> <br/> |<span data-ttu-id="975bf-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="975bf-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="975bf-113">定義</span><span class="sxs-lookup"><span data-stu-id="975bf-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="975bf-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="975bf-114">Elements and attributes</span></span>

<span data-ttu-id="975bf-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="975bf-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="975bf-116">親要素</span><span class="sxs-lookup"><span data-stu-id="975bf-116">Parent elements</span></span>

|<span data-ttu-id="975bf-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="975bf-117">**Element**</span></span>|<span data-ttu-id="975bf-118">**型**</span><span class="sxs-lookup"><span data-stu-id="975bf-118">**Type**</span></span>|<span data-ttu-id="975bf-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="975bf-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="975bf-120">EventList</span><span class="sxs-lookup"><span data-stu-id="975bf-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="975bf-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="975bf-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="975bf-122">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="975bf-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="975bf-123">子要素</span><span class="sxs-lookup"><span data-stu-id="975bf-123">Child elements</span></span>

<span data-ttu-id="975bf-124">なし。</span><span class="sxs-lookup"><span data-stu-id="975bf-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="975bf-125">属性</span><span class="sxs-lookup"><span data-stu-id="975bf-125">Attributes</span></span>

|<span data-ttu-id="975bf-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="975bf-126">**Attribute**</span></span>|<span data-ttu-id="975bf-127">**型**</span><span class="sxs-lookup"><span data-stu-id="975bf-127">**Type**</span></span>|<span data-ttu-id="975bf-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="975bf-128">**Required**</span></span>|<span data-ttu-id="975bf-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="975bf-129">**Description**</span></span>|<span data-ttu-id="975bf-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="975bf-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="975bf-131">アクション</span><span class="sxs-lookup"><span data-stu-id="975bf-131">Action</span></span>  <br/> |<span data-ttu-id="975bf-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="975bf-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="975bf-133">必須</span><span class="sxs-lookup"><span data-stu-id="975bf-133">required</span></span>  <br/> |<span data-ttu-id="975bf-134">**EventItem**の親要素のアクション コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="975bf-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="975bf-135">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="975bf-136">有効</span><span class="sxs-lookup"><span data-stu-id="975bf-136">Enabled</span></span>  <br/> |<span data-ttu-id="975bf-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="975bf-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="975bf-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="975bf-138">optional</span></span>  <br/> |<span data-ttu-id="975bf-139">イベントが有効か無効になっているかどうかを示すフラグを表します。</span><span class="sxs-lookup"><span data-stu-id="975bf-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="975bf-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="975bf-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="975bf-141">EventCode</span></span>  <br/> |<span data-ttu-id="975bf-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="975bf-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="975bf-143">必須</span><span class="sxs-lookup"><span data-stu-id="975bf-143">required</span></span>  <br/> |<span data-ttu-id="975bf-144">アドオンをトリガーするイベントを示すコードです。</span><span class="sxs-lookup"><span data-stu-id="975bf-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="975bf-145">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="975bf-146">ID</span><span class="sxs-lookup"><span data-stu-id="975bf-146">ID</span></span>  <br/> |<span data-ttu-id="975bf-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="975bf-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="975bf-148">必須</span><span class="sxs-lookup"><span data-stu-id="975bf-148">required</span></span>  <br/> |<span data-ttu-id="975bf-149">イベントの ID。</span><span class="sxs-lookup"><span data-stu-id="975bf-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="975bf-150">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="975bf-151">ターゲット</span><span class="sxs-lookup"><span data-stu-id="975bf-151">Target</span></span>  <br/> |<span data-ttu-id="975bf-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="975bf-152">xsd:string</span></span>  <br/> |<span data-ttu-id="975bf-153">必須</span><span class="sxs-lookup"><span data-stu-id="975bf-153">required</span></span>  <br/> |<span data-ttu-id="975bf-154">イベントのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="975bf-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="975bf-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="975bf-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="975bf-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="975bf-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="975bf-157">xsd:string</span></span>  <br/> |<span data-ttu-id="975bf-158">必須</span><span class="sxs-lookup"><span data-stu-id="975bf-158">required</span></span>  <br/> |<span data-ttu-id="975bf-159">イベントのターゲットに送る引数を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="975bf-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="975bf-160">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="975bf-160">Values of the xsd:string type.</span></span>  <br/> |
   

