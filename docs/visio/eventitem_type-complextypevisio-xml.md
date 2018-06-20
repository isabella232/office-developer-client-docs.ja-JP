---
title: EventItem_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 7fc23d9e2a9e4567693a4979b796804b16f148e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805336"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="1c41d-102">EventItem_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1c41d-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1c41d-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1c41d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c41d-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1c41d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1c41d-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1c41d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1c41d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1c41d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1c41d-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="1c41d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1c41d-108">なし</span><span class="sxs-lookup"><span data-stu-id="1c41d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1c41d-109">定義</span><span class="sxs-lookup"><span data-stu-id="1c41d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1c41d-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1c41d-110">Elements and attributes</span></span>

<span data-ttu-id="1c41d-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c41d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1c41d-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1c41d-112">Child elements</span></span>

<span data-ttu-id="1c41d-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1c41d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c41d-114">属性</span><span class="sxs-lookup"><span data-stu-id="1c41d-114">Attributes</span></span>

|<span data-ttu-id="1c41d-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1c41d-115">**Attribute**</span></span>|<span data-ttu-id="1c41d-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1c41d-116">**Type**</span></span>|<span data-ttu-id="1c41d-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1c41d-117">**Required**</span></span>|<span data-ttu-id="1c41d-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1c41d-118">**Description**</span></span>|<span data-ttu-id="1c41d-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1c41d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1c41d-120">アクション</span><span class="sxs-lookup"><span data-stu-id="1c41d-120">Action</span></span>  <br/> |<span data-ttu-id="1c41d-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1c41d-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1c41d-122">必須</span><span class="sxs-lookup"><span data-stu-id="1c41d-122">required</span></span>  <br/> ||<span data-ttu-id="1c41d-123">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1c41d-124">Enabled</span><span class="sxs-lookup"><span data-stu-id="1c41d-124">Enabled</span></span>  <br/> |<span data-ttu-id="1c41d-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1c41d-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1c41d-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="1c41d-126">optional</span></span>  <br/> ||<span data-ttu-id="1c41d-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1c41d-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="1c41d-128">EventCode</span></span>  <br/> |<span data-ttu-id="1c41d-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1c41d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1c41d-130">必須</span><span class="sxs-lookup"><span data-stu-id="1c41d-130">required</span></span>  <br/> ||<span data-ttu-id="1c41d-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1c41d-132">ID</span><span class="sxs-lookup"><span data-stu-id="1c41d-132">ID</span></span>  <br/> |<span data-ttu-id="1c41d-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1c41d-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1c41d-134">必須</span><span class="sxs-lookup"><span data-stu-id="1c41d-134">required</span></span>  <br/> ||<span data-ttu-id="1c41d-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1c41d-136">ターゲット</span><span class="sxs-lookup"><span data-stu-id="1c41d-136">Target</span></span>  <br/> |<span data-ttu-id="1c41d-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1c41d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1c41d-138">必須</span><span class="sxs-lookup"><span data-stu-id="1c41d-138">required</span></span>  <br/> ||<span data-ttu-id="1c41d-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1c41d-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="1c41d-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="1c41d-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1c41d-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1c41d-142">必須</span><span class="sxs-lookup"><span data-stu-id="1c41d-142">required</span></span>  <br/> ||<span data-ttu-id="1c41d-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c41d-143">Values of the xsd:string type.</span></span>  <br/> |
   

