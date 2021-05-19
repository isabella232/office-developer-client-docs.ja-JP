---
title: EventItem_Type complexType (xml Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541793"
---
# <a name="eventitem_type-complextype-visio-xml"></a><span data-ttu-id="52728-102">EventItem_Type complexType (xml Visio)</span><span class="sxs-lookup"><span data-stu-id="52728-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="52728-103">型情報</span><span class="sxs-lookup"><span data-stu-id="52728-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52728-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52728-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52728-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="52728-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52728-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="52728-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52728-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="52728-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52728-108">なし</span><span class="sxs-lookup"><span data-stu-id="52728-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52728-109">定義</span><span class="sxs-lookup"><span data-stu-id="52728-109">Definition</span></span>

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="52728-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="52728-110">Elements and attributes</span></span>

<span data-ttu-id="52728-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="52728-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52728-112">子要素</span><span class="sxs-lookup"><span data-stu-id="52728-112">Child elements</span></span>

<span data-ttu-id="52728-113">なし。</span><span class="sxs-lookup"><span data-stu-id="52728-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52728-114">属性</span><span class="sxs-lookup"><span data-stu-id="52728-114">Attributes</span></span>

|<span data-ttu-id="52728-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="52728-115">**Attribute**</span></span>|<span data-ttu-id="52728-116">**型**</span><span class="sxs-lookup"><span data-stu-id="52728-116">**Type**</span></span>|<span data-ttu-id="52728-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="52728-117">**Required**</span></span>|<span data-ttu-id="52728-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="52728-118">**Description**</span></span>|<span data-ttu-id="52728-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="52728-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52728-120">Action</span><span class="sxs-lookup"><span data-stu-id="52728-120">Action</span></span>  <br/> |<span data-ttu-id="52728-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52728-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52728-122">必須</span><span class="sxs-lookup"><span data-stu-id="52728-122">required</span></span>  <br/> ||<span data-ttu-id="52728-123">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52728-124">有効</span><span class="sxs-lookup"><span data-stu-id="52728-124">Enabled</span></span>  <br/> |<span data-ttu-id="52728-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="52728-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52728-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="52728-126">optional</span></span>  <br/> ||<span data-ttu-id="52728-127">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52728-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="52728-128">EventCode</span></span>  <br/> |<span data-ttu-id="52728-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52728-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52728-130">必須</span><span class="sxs-lookup"><span data-stu-id="52728-130">required</span></span>  <br/> ||<span data-ttu-id="52728-131">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52728-132">ID</span><span class="sxs-lookup"><span data-stu-id="52728-132">ID</span></span>  <br/> |<span data-ttu-id="52728-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="52728-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52728-134">必須</span><span class="sxs-lookup"><span data-stu-id="52728-134">required</span></span>  <br/> ||<span data-ttu-id="52728-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52728-136">Target</span><span class="sxs-lookup"><span data-stu-id="52728-136">Target</span></span>  <br/> |<span data-ttu-id="52728-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="52728-137">xsd:string</span></span>  <br/> |<span data-ttu-id="52728-138">必須</span><span class="sxs-lookup"><span data-stu-id="52728-138">required</span></span>  <br/> ||<span data-ttu-id="52728-139">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52728-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="52728-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="52728-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="52728-141">xsd:string</span></span>  <br/> |<span data-ttu-id="52728-142">必須</span><span class="sxs-lookup"><span data-stu-id="52728-142">required</span></span>  <br/> ||<span data-ttu-id="52728-143">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="52728-143">Values of the xsd:string type.</span></span>  <br/> |
   

