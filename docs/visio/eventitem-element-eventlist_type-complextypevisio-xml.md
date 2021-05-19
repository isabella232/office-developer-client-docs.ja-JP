---
title: EventItem 要素 (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベント コードをカプセル化します。
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541842"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a><span data-ttu-id="ae690-103">EventItem 要素 (EventList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ae690-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ae690-104">イベント コードをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="ae690-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae690-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ae690-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae690-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ae690-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae690-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="ae690-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae690-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ae690-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae690-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ae690-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae690-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae690-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae690-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ae690-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae690-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ae690-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae690-113">定義</span><span class="sxs-lookup"><span data-stu-id="ae690-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae690-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ae690-114">Elements and attributes</span></span>

<span data-ttu-id="ae690-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae690-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae690-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ae690-116">Parent elements</span></span>

|<span data-ttu-id="ae690-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ae690-117">**Element**</span></span>|<span data-ttu-id="ae690-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ae690-118">**Type**</span></span>|<span data-ttu-id="ae690-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae690-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae690-120">EventList</span><span class="sxs-lookup"><span data-stu-id="ae690-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae690-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="ae690-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae690-122">オブジェクトが応答 **するイベントごとに EventItem** 要素を含む。</span><span class="sxs-lookup"><span data-stu-id="ae690-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae690-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ae690-123">Child elements</span></span>

<span data-ttu-id="ae690-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ae690-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae690-125">属性</span><span class="sxs-lookup"><span data-stu-id="ae690-125">Attributes</span></span>

|<span data-ttu-id="ae690-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ae690-126">**Attribute**</span></span>|<span data-ttu-id="ae690-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ae690-127">**Type**</span></span>|<span data-ttu-id="ae690-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ae690-128">**Required**</span></span>|<span data-ttu-id="ae690-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ae690-129">**Description**</span></span>|<span data-ttu-id="ae690-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ae690-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ae690-131">Action</span><span class="sxs-lookup"><span data-stu-id="ae690-131">Action</span></span>  <br/> |<span data-ttu-id="ae690-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ae690-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ae690-133">必須</span><span class="sxs-lookup"><span data-stu-id="ae690-133">required</span></span>  <br/> |<span data-ttu-id="ae690-134">親 EventItem 要素のアクション コード **を指定** します。</span><span class="sxs-lookup"><span data-stu-id="ae690-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="ae690-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ae690-136">有効</span><span class="sxs-lookup"><span data-stu-id="ae690-136">Enabled</span></span>  <br/> |<span data-ttu-id="ae690-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ae690-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ae690-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="ae690-138">optional</span></span>  <br/> |<span data-ttu-id="ae690-139">イベントが有効または無効かどうかを示すフラグを表します。</span><span class="sxs-lookup"><span data-stu-id="ae690-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="ae690-140">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ae690-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="ae690-141">EventCode</span></span>  <br/> |<span data-ttu-id="ae690-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ae690-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ae690-143">必須</span><span class="sxs-lookup"><span data-stu-id="ae690-143">required</span></span>  <br/> |<span data-ttu-id="ae690-144">アドオンをトリガーするイベントを示すコード。</span><span class="sxs-lookup"><span data-stu-id="ae690-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="ae690-145">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ae690-146">ID</span><span class="sxs-lookup"><span data-stu-id="ae690-146">ID</span></span>  <br/> |<span data-ttu-id="ae690-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae690-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ae690-148">必須</span><span class="sxs-lookup"><span data-stu-id="ae690-148">required</span></span>  <br/> |<span data-ttu-id="ae690-149">イベントの ID。</span><span class="sxs-lookup"><span data-stu-id="ae690-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="ae690-150">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ae690-151">Target</span><span class="sxs-lookup"><span data-stu-id="ae690-151">Target</span></span>  <br/> |<span data-ttu-id="ae690-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ae690-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ae690-153">必須</span><span class="sxs-lookup"><span data-stu-id="ae690-153">required</span></span>  <br/> |<span data-ttu-id="ae690-154">イベントのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="ae690-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="ae690-155">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ae690-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="ae690-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="ae690-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ae690-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ae690-158">必須</span><span class="sxs-lookup"><span data-stu-id="ae690-158">required</span></span>  <br/> |<span data-ttu-id="ae690-159">イベントのターゲットに送信する引数を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae690-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="ae690-160">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="ae690-160">Values of the xsd:string type.</span></span>  <br/> |
   

