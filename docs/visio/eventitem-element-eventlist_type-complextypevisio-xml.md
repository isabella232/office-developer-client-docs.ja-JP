---
title: EventItem 要素 (EventList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベント コードをカプセル化します。
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805326"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="49f6b-103">EventItem 要素 (EventList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="49f6b-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="49f6b-104">イベント コードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49f6b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="49f6b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49f6b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="49f6b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="49f6b-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="49f6b-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="49f6b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="49f6b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="49f6b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="49f6b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="49f6b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="49f6b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="49f6b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="49f6b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="49f6b-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="49f6b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="49f6b-113">定義</span><span class="sxs-lookup"><span data-stu-id="49f6b-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="49f6b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="49f6b-114">Elements and attributes</span></span>

<span data-ttu-id="49f6b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="49f6b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="49f6b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="49f6b-116">Parent elements</span></span>

|<span data-ttu-id="49f6b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="49f6b-117">**Element**</span></span>|<span data-ttu-id="49f6b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="49f6b-118">**Type**</span></span>|<span data-ttu-id="49f6b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="49f6b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="49f6b-120">EventList</span><span class="sxs-lookup"><span data-stu-id="49f6b-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49f6b-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="49f6b-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="49f6b-122">オブジェクトが応答する各イベントの**EventItem**要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="49f6b-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="49f6b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="49f6b-123">Child elements</span></span>

<span data-ttu-id="49f6b-124">なし。</span><span class="sxs-lookup"><span data-stu-id="49f6b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49f6b-125">属性</span><span class="sxs-lookup"><span data-stu-id="49f6b-125">Attributes</span></span>

|<span data-ttu-id="49f6b-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="49f6b-126">**Attribute**</span></span>|<span data-ttu-id="49f6b-127">**型**</span><span class="sxs-lookup"><span data-stu-id="49f6b-127">**Type**</span></span>|<span data-ttu-id="49f6b-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="49f6b-128">**Required**</span></span>|<span data-ttu-id="49f6b-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="49f6b-129">**Description**</span></span>|<span data-ttu-id="49f6b-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="49f6b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="49f6b-131">アクション</span><span class="sxs-lookup"><span data-stu-id="49f6b-131">Action</span></span>  <br/> |<span data-ttu-id="49f6b-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49f6b-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49f6b-133">必須</span><span class="sxs-lookup"><span data-stu-id="49f6b-133">required</span></span>  <br/> |<span data-ttu-id="49f6b-134">**EventItem**の親要素のアクション コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="49f6b-135">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49f6b-136">有効</span><span class="sxs-lookup"><span data-stu-id="49f6b-136">Enabled</span></span>  <br/> |<span data-ttu-id="49f6b-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="49f6b-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="49f6b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="49f6b-138">optional</span></span>  <br/> |<span data-ttu-id="49f6b-139">イベントが有効か無効になっているかどうかを示すフラグを表します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="49f6b-140">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="49f6b-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="49f6b-141">EventCode</span></span>  <br/> |<span data-ttu-id="49f6b-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="49f6b-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="49f6b-143">必須</span><span class="sxs-lookup"><span data-stu-id="49f6b-143">required</span></span>  <br/> |<span data-ttu-id="49f6b-144">アドオンをトリガーするイベントを示すコードです。</span><span class="sxs-lookup"><span data-stu-id="49f6b-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="49f6b-145">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="49f6b-146">ID</span><span class="sxs-lookup"><span data-stu-id="49f6b-146">ID</span></span>  <br/> |<span data-ttu-id="49f6b-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="49f6b-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="49f6b-148">必須</span><span class="sxs-lookup"><span data-stu-id="49f6b-148">required</span></span>  <br/> |<span data-ttu-id="49f6b-149">イベントの ID。</span><span class="sxs-lookup"><span data-stu-id="49f6b-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="49f6b-150">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="49f6b-151">ターゲット</span><span class="sxs-lookup"><span data-stu-id="49f6b-151">Target</span></span>  <br/> |<span data-ttu-id="49f6b-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49f6b-152">xsd:string</span></span>  <br/> |<span data-ttu-id="49f6b-153">必須</span><span class="sxs-lookup"><span data-stu-id="49f6b-153">required</span></span>  <br/> |<span data-ttu-id="49f6b-154">イベントのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="49f6b-155">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="49f6b-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="49f6b-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="49f6b-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="49f6b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="49f6b-158">必須</span><span class="sxs-lookup"><span data-stu-id="49f6b-158">required</span></span>  <br/> |<span data-ttu-id="49f6b-159">イベントのターゲットに送る引数を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="49f6b-160">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49f6b-160">Values of the xsd:string type.</span></span>  <br/> |
   

