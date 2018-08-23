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
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="6b214-102">EventItem_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6b214-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6b214-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6b214-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b214-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6b214-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6b214-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6b214-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6b214-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6b214-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6b214-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6b214-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6b214-108">なし</span><span class="sxs-lookup"><span data-stu-id="6b214-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b214-109">定義</span><span class="sxs-lookup"><span data-stu-id="6b214-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6b214-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6b214-110">Elements and attributes</span></span>

<span data-ttu-id="6b214-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b214-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6b214-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6b214-112">Child elements</span></span>

<span data-ttu-id="6b214-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6b214-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b214-114">属性</span><span class="sxs-lookup"><span data-stu-id="6b214-114">Attributes</span></span>

|<span data-ttu-id="6b214-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6b214-115">**Attribute**</span></span>|<span data-ttu-id="6b214-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6b214-116">**Type**</span></span>|<span data-ttu-id="6b214-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6b214-117">**Required**</span></span>|<span data-ttu-id="6b214-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b214-118">**Description**</span></span>|<span data-ttu-id="6b214-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6b214-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b214-120">アクション</span><span class="sxs-lookup"><span data-stu-id="6b214-120">Action</span></span>  <br/> |<span data-ttu-id="6b214-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6b214-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6b214-122">必須</span><span class="sxs-lookup"><span data-stu-id="6b214-122">required</span></span>  <br/> ||<span data-ttu-id="6b214-123">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6b214-124">有効</span><span class="sxs-lookup"><span data-stu-id="6b214-124">Enabled</span></span>  <br/> |<span data-ttu-id="6b214-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6b214-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6b214-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="6b214-126">optional</span></span>  <br/> ||<span data-ttu-id="6b214-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6b214-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="6b214-128">EventCode</span></span>  <br/> |<span data-ttu-id="6b214-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6b214-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6b214-130">必須</span><span class="sxs-lookup"><span data-stu-id="6b214-130">required</span></span>  <br/> ||<span data-ttu-id="6b214-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6b214-132">ID</span><span class="sxs-lookup"><span data-stu-id="6b214-132">ID</span></span>  <br/> |<span data-ttu-id="6b214-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6b214-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b214-134">必須</span><span class="sxs-lookup"><span data-stu-id="6b214-134">required</span></span>  <br/> ||<span data-ttu-id="6b214-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b214-136">ターゲット</span><span class="sxs-lookup"><span data-stu-id="6b214-136">Target</span></span>  <br/> |<span data-ttu-id="6b214-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b214-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6b214-138">必須</span><span class="sxs-lookup"><span data-stu-id="6b214-138">required</span></span>  <br/> ||<span data-ttu-id="6b214-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b214-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="6b214-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="6b214-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6b214-141">xsd:string</span></span>  <br/> |<span data-ttu-id="6b214-142">必須</span><span class="sxs-lookup"><span data-stu-id="6b214-142">required</span></span>  <br/> ||<span data-ttu-id="6b214-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b214-143">Values of the xsd:string type.</span></span>  <br/> |
   

