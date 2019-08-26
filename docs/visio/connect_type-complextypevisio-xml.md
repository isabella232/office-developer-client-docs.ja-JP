---
title: Connect_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9dee421915cb3e69ef5223280a425e785d29e4ec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538740"
---
# <a name="connect_type-complextype-visio-xml"></a><span data-ttu-id="d0f03-102">Connect_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d0f03-102">Connect_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d0f03-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d0f03-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0f03-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0f03-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d0f03-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d0f03-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d0f03-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d0f03-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d0f03-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d0f03-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d0f03-108">なし</span><span class="sxs-lookup"><span data-stu-id="d0f03-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0f03-109">定義</span><span class="sxs-lookup"><span data-stu-id="d0f03-109">Definition</span></span>

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0f03-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d0f03-110">Elements and attributes</span></span>

<span data-ttu-id="d0f03-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0f03-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d0f03-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d0f03-112">Child elements</span></span>

<span data-ttu-id="d0f03-113">なし。</span><span class="sxs-lookup"><span data-stu-id="d0f03-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0f03-114">属性</span><span class="sxs-lookup"><span data-stu-id="d0f03-114">Attributes</span></span>

|<span data-ttu-id="d0f03-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="d0f03-115">**Attribute**</span></span>|<span data-ttu-id="d0f03-116">**型**</span><span class="sxs-lookup"><span data-stu-id="d0f03-116">**Type**</span></span>|<span data-ttu-id="d0f03-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="d0f03-117">**Required**</span></span>|<span data-ttu-id="d0f03-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0f03-118">**Description**</span></span>|<span data-ttu-id="d0f03-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d0f03-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0f03-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="d0f03-120">FromCell</span></span>  <br/> |<span data-ttu-id="d0f03-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0f03-121">xsd:string</span></span>  <br/> |<span data-ttu-id="d0f03-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0f03-122">optional</span></span>  <br/> ||<span data-ttu-id="d0f03-123">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0f03-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="d0f03-124">FromPart</span></span>  <br/> |<span data-ttu-id="d0f03-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="d0f03-125">xsd:int</span></span>  <br/> |<span data-ttu-id="d0f03-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0f03-126">optional</span></span>  <br/> ||<span data-ttu-id="d0f03-127">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d0f03-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="d0f03-128">FromSheet</span></span>  <br/> |<span data-ttu-id="d0f03-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0f03-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0f03-130">必須</span><span class="sxs-lookup"><span data-stu-id="d0f03-130">required</span></span>  <br/> ||<span data-ttu-id="d0f03-131">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0f03-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="d0f03-132">ToCell</span></span>  <br/> |<span data-ttu-id="d0f03-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d0f03-133">xsd:string</span></span>  <br/> |<span data-ttu-id="d0f03-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0f03-134">optional</span></span>  <br/> ||<span data-ttu-id="d0f03-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d0f03-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="d0f03-136">ToPart</span></span>  <br/> |<span data-ttu-id="d0f03-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="d0f03-137">xsd:int</span></span>  <br/> |<span data-ttu-id="d0f03-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="d0f03-138">optional</span></span>  <br/> ||<span data-ttu-id="d0f03-139">xsd:int 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="d0f03-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="d0f03-140">ToSheet</span></span>  <br/> |<span data-ttu-id="d0f03-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0f03-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0f03-142">必須</span><span class="sxs-lookup"><span data-stu-id="d0f03-142">required</span></span>  <br/> ||<span data-ttu-id="d0f03-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="d0f03-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

