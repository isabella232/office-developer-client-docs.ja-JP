---
title: EventItem_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337206"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="1b5c5-102">EventItem_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1b5c5-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1b5c5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1b5c5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b5c5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b5c5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b5c5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1b5c5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b5c5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b5c5-108">なし</span><span class="sxs-lookup"><span data-stu-id="1b5c5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b5c5-109">定義</span><span class="sxs-lookup"><span data-stu-id="1b5c5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1b5c5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1b5c5-110">Elements and attributes</span></span>

<span data-ttu-id="1b5c5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b5c5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1b5c5-112">Child elements</span></span>

<span data-ttu-id="1b5c5-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b5c5-114">属性</span><span class="sxs-lookup"><span data-stu-id="1b5c5-114">Attributes</span></span>

|<span data-ttu-id="1b5c5-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-115">**Attribute**</span></span>|<span data-ttu-id="1b5c5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-116">**Type**</span></span>|<span data-ttu-id="1b5c5-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-117">**Required**</span></span>|<span data-ttu-id="1b5c5-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-118">**Description**</span></span>|<span data-ttu-id="1b5c5-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1b5c5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b5c5-120">アクション</span><span class="sxs-lookup"><span data-stu-id="1b5c5-120">Action</span></span>  <br/> |<span data-ttu-id="1b5c5-121">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="1b5c5-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1b5c5-122">必須</span><span class="sxs-lookup"><span data-stu-id="1b5c5-122">required</span></span>  <br/> ||<span data-ttu-id="1b5c5-123">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1b5c5-124">有効</span><span class="sxs-lookup"><span data-stu-id="1b5c5-124">Enabled</span></span>  <br/> |<span data-ttu-id="1b5c5-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="1b5c5-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b5c5-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="1b5c5-126">optional</span></span>  <br/> ||<span data-ttu-id="1b5c5-127">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1b5c5-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="1b5c5-128">EventCode</span></span>  <br/> |<span data-ttu-id="1b5c5-129">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="1b5c5-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1b5c5-130">必須</span><span class="sxs-lookup"><span data-stu-id="1b5c5-130">required</span></span>  <br/> ||<span data-ttu-id="1b5c5-131">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1b5c5-132">ID</span><span class="sxs-lookup"><span data-stu-id="1b5c5-132">ID</span></span>  <br/> |<span data-ttu-id="1b5c5-133">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="1b5c5-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b5c5-134">必須</span><span class="sxs-lookup"><span data-stu-id="1b5c5-134">required</span></span>  <br/> ||<span data-ttu-id="1b5c5-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b5c5-136">Target</span><span class="sxs-lookup"><span data-stu-id="1b5c5-136">Target</span></span>  <br/> |<span data-ttu-id="1b5c5-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1b5c5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1b5c5-138">必須</span><span class="sxs-lookup"><span data-stu-id="1b5c5-138">required</span></span>  <br/> ||<span data-ttu-id="1b5c5-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1b5c5-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="1b5c5-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="1b5c5-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1b5c5-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1b5c5-142">必須</span><span class="sxs-lookup"><span data-stu-id="1b5c5-142">required</span></span>  <br/> ||<span data-ttu-id="1b5c5-143">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1b5c5-143">Values of the xsd:string type.</span></span>  <br/> |
   

