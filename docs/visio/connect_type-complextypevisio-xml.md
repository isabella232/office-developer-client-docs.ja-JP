---
title: Connect_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 9a321a3ff910afb183e1a697eaad9dfb51125524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805080"
---
# <a name="connecttype-complextype-visio-xml"></a><span data-ttu-id="0d23e-102">Connect_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0d23e-102">Connect_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0d23e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0d23e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d23e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0d23e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d23e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0d23e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d23e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0d23e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d23e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0d23e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d23e-108">なし</span><span class="sxs-lookup"><span data-stu-id="0d23e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d23e-109">定義</span><span class="sxs-lookup"><span data-stu-id="0d23e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0d23e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0d23e-110">Elements and attributes</span></span>

<span data-ttu-id="0d23e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d23e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d23e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0d23e-112">Child elements</span></span>

<span data-ttu-id="0d23e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0d23e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d23e-114">属性</span><span class="sxs-lookup"><span data-stu-id="0d23e-114">Attributes</span></span>

|<span data-ttu-id="0d23e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="0d23e-115">**Attribute**</span></span>|<span data-ttu-id="0d23e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="0d23e-116">**Type**</span></span>|<span data-ttu-id="0d23e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="0d23e-117">**Required**</span></span>|<span data-ttu-id="0d23e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d23e-118">**Description**</span></span>|<span data-ttu-id="0d23e-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0d23e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d23e-120">FromCell</span><span class="sxs-lookup"><span data-stu-id="0d23e-120">FromCell</span></span>  <br/> |<span data-ttu-id="0d23e-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0d23e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0d23e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d23e-122">optional</span></span>  <br/> ||<span data-ttu-id="0d23e-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d23e-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d23e-124">FromPart</span><span class="sxs-lookup"><span data-stu-id="0d23e-124">FromPart</span></span>  <br/> |<span data-ttu-id="0d23e-125">xsd:int</span><span class="sxs-lookup"><span data-stu-id="0d23e-125">xsd:int</span></span>  <br/> |<span data-ttu-id="0d23e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d23e-126">optional</span></span>  <br/> ||<span data-ttu-id="0d23e-127">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="0d23e-127">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="0d23e-128">FromSheet</span><span class="sxs-lookup"><span data-stu-id="0d23e-128">FromSheet</span></span>  <br/> |<span data-ttu-id="0d23e-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0d23e-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0d23e-130">必須</span><span class="sxs-lookup"><span data-stu-id="0d23e-130">required</span></span>  <br/> ||<span data-ttu-id="0d23e-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d23e-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0d23e-132">ToCell</span><span class="sxs-lookup"><span data-stu-id="0d23e-132">ToCell</span></span>  <br/> |<span data-ttu-id="0d23e-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0d23e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0d23e-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d23e-134">optional</span></span>  <br/> ||<span data-ttu-id="0d23e-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d23e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d23e-136">ToPart</span><span class="sxs-lookup"><span data-stu-id="0d23e-136">ToPart</span></span>  <br/> |<span data-ttu-id="0d23e-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="0d23e-137">xsd:int</span></span>  <br/> |<span data-ttu-id="0d23e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d23e-138">optional</span></span>  <br/> ||<span data-ttu-id="0d23e-139">Xsd:int 型の値です。</span><span class="sxs-lookup"><span data-stu-id="0d23e-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="0d23e-140">ToSheet</span><span class="sxs-lookup"><span data-stu-id="0d23e-140">ToSheet</span></span>  <br/> |<span data-ttu-id="0d23e-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0d23e-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0d23e-142">必須</span><span class="sxs-lookup"><span data-stu-id="0d23e-142">required</span></span>  <br/> ||<span data-ttu-id="0d23e-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d23e-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

