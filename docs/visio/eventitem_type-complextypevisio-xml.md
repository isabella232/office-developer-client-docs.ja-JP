---
title: EventItem_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: 77c51ab76a1d7c5c4450c429b1d3ccb8e3442f34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395729"
---
# <a name="eventitemtype-complextype-visio-xml"></a><span data-ttu-id="06f56-102">EventItem_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="06f56-102">EventItem_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="06f56-103">型情報</span><span class="sxs-lookup"><span data-stu-id="06f56-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06f56-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="06f56-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="06f56-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="06f56-105">**Schema file**</span></span> <br/> |<span data-ttu-id="06f56-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="06f56-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="06f56-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="06f56-107">**Extension base**</span></span> <br/> |<span data-ttu-id="06f56-108">なし</span><span class="sxs-lookup"><span data-stu-id="06f56-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06f56-109">定義</span><span class="sxs-lookup"><span data-stu-id="06f56-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="06f56-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="06f56-110">Elements and attributes</span></span>

<span data-ttu-id="06f56-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="06f56-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06f56-112">子要素</span><span class="sxs-lookup"><span data-stu-id="06f56-112">Child elements</span></span>

<span data-ttu-id="06f56-113">なし。</span><span class="sxs-lookup"><span data-stu-id="06f56-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06f56-114">属性</span><span class="sxs-lookup"><span data-stu-id="06f56-114">Attributes</span></span>

|<span data-ttu-id="06f56-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="06f56-115">**Attribute**</span></span>|<span data-ttu-id="06f56-116">**型**</span><span class="sxs-lookup"><span data-stu-id="06f56-116">**Type**</span></span>|<span data-ttu-id="06f56-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="06f56-117">**Required**</span></span>|<span data-ttu-id="06f56-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="06f56-118">**Description**</span></span>|<span data-ttu-id="06f56-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="06f56-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06f56-120">アクション</span><span class="sxs-lookup"><span data-stu-id="06f56-120">Action</span></span>  <br/> |<span data-ttu-id="06f56-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="06f56-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="06f56-122">必須</span><span class="sxs-lookup"><span data-stu-id="06f56-122">required</span></span>  <br/> ||<span data-ttu-id="06f56-123">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="06f56-124">有効</span><span class="sxs-lookup"><span data-stu-id="06f56-124">Enabled</span></span>  <br/> |<span data-ttu-id="06f56-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="06f56-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="06f56-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="06f56-126">optional</span></span>  <br/> ||<span data-ttu-id="06f56-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="06f56-128">EventCode</span><span class="sxs-lookup"><span data-stu-id="06f56-128">EventCode</span></span>  <br/> |<span data-ttu-id="06f56-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="06f56-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="06f56-130">必須</span><span class="sxs-lookup"><span data-stu-id="06f56-130">required</span></span>  <br/> ||<span data-ttu-id="06f56-131">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="06f56-132">ID</span><span class="sxs-lookup"><span data-stu-id="06f56-132">ID</span></span>  <br/> |<span data-ttu-id="06f56-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="06f56-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="06f56-134">必須</span><span class="sxs-lookup"><span data-stu-id="06f56-134">required</span></span>  <br/> ||<span data-ttu-id="06f56-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="06f56-136">ターゲット</span><span class="sxs-lookup"><span data-stu-id="06f56-136">Target</span></span>  <br/> |<span data-ttu-id="06f56-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="06f56-137">xsd:string</span></span>  <br/> |<span data-ttu-id="06f56-138">必須</span><span class="sxs-lookup"><span data-stu-id="06f56-138">required</span></span>  <br/> ||<span data-ttu-id="06f56-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="06f56-140">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="06f56-140">TargetArgs</span></span>  <br/> |<span data-ttu-id="06f56-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="06f56-141">xsd:string</span></span>  <br/> |<span data-ttu-id="06f56-142">必須</span><span class="sxs-lookup"><span data-stu-id="06f56-142">required</span></span>  <br/> ||<span data-ttu-id="06f56-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="06f56-143">Values of the xsd:string type.</span></span>  <br/> |
   

