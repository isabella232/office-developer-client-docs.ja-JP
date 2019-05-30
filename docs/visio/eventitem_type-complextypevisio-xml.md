---
title: EventItem_Type complexType (Visio XML)
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
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="09cf6-102">EventItem_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="09cf6-102">EventItem_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="09cf6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="09cf6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09cf6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="09cf6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="09cf6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="09cf6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="09cf6-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="09cf6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="09cf6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="09cf6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="09cf6-108">None</span><span class="sxs-lookup"><span data-stu-id="09cf6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09cf6-109">定義</span><span class="sxs-lookup"><span data-stu-id="09cf6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="09cf6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="09cf6-110">Elements and attributes</span></span>

<span data-ttu-id="09cf6-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="09cf6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="09cf6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="09cf6-112">Child elements</span></span>

<span data-ttu-id="09cf6-113">なし。</span><span class="sxs-lookup"><span data-stu-id="09cf6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09cf6-114">属性</span><span class="sxs-lookup"><span data-stu-id="09cf6-114">Attributes</span></span>

|<span data-ttu-id="09cf6-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="09cf6-115">**Attribute**</span></span>|<span data-ttu-id="09cf6-116">**型**</span><span class="sxs-lookup"><span data-stu-id="09cf6-116">**Type**</span></span>|<span data-ttu-id="09cf6-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="09cf6-117">**Required**</span></span>|<span data-ttu-id="09cf6-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="09cf6-118">**Description**</span></span>|<span data-ttu-id="09cf6-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="09cf6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09cf6-120">Action</span><span class="sxs-lookup"><span data-stu-id="09cf6-120">Action</span></span>  <br/> |<span data-ttu-id="09cf6-121">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="09cf6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="09cf6-122">必須</span><span class="sxs-lookup"><span data-stu-id="09cf6-122">required</span></span>  <br/> ||<span data-ttu-id="09cf6-123">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="09cf6-124">有効</span><span class="sxs-lookup"><span data-stu-id="09cf6-124">Enabled</span></span>  <br/> |<span data-ttu-id="09cf6-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="09cf6-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="09cf6-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="09cf6-126">optional</span></span>  <br/> ||<span data-ttu-id="09cf6-127">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="09cf6-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="09cf6-128">EventCode</span></span>  <br/> |<span data-ttu-id="09cf6-129">xsd: アン Signedshort</span><span class="sxs-lookup"><span data-stu-id="09cf6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="09cf6-130">必須</span><span class="sxs-lookup"><span data-stu-id="09cf6-130">required</span></span>  <br/> ||<span data-ttu-id="09cf6-131">Xsd: _ Signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="09cf6-132">ID</span><span class="sxs-lookup"><span data-stu-id="09cf6-132">ID</span></span>  <br/> |<span data-ttu-id="09cf6-133">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="09cf6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09cf6-134">必須</span><span class="sxs-lookup"><span data-stu-id="09cf6-134">required</span></span>  <br/> ||<span data-ttu-id="09cf6-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09cf6-136">Target</span><span class="sxs-lookup"><span data-stu-id="09cf6-136">Target</span></span>  <br/> |<span data-ttu-id="09cf6-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="09cf6-137">xsd:string</span></span>  <br/> |<span data-ttu-id="09cf6-138">必須</span><span class="sxs-lookup"><span data-stu-id="09cf6-138">required</span></span>  <br/> ||<span data-ttu-id="09cf6-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09cf6-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="09cf6-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="09cf6-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="09cf6-141">xsd:string</span></span>  <br/> |<span data-ttu-id="09cf6-142">必須</span><span class="sxs-lookup"><span data-stu-id="09cf6-142">required</span></span>  <br/> ||<span data-ttu-id="09cf6-143">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="09cf6-143">Values of the xsd:string type.</span></span>  <br/> |
   

