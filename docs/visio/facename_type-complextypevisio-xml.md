---
title: FaceName_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322555"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="1e47e-102">FaceName_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1e47e-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1e47e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1e47e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e47e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e47e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e47e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1e47e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e47e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="1e47e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e47e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1e47e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e47e-108">なし</span><span class="sxs-lookup"><span data-stu-id="1e47e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e47e-109">定義</span><span class="sxs-lookup"><span data-stu-id="1e47e-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e47e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1e47e-110">Elements and attributes</span></span>

<span data-ttu-id="1e47e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e47e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e47e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1e47e-112">Child elements</span></span>

<span data-ttu-id="1e47e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1e47e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e47e-114">属性</span><span class="sxs-lookup"><span data-stu-id="1e47e-114">Attributes</span></span>

|<span data-ttu-id="1e47e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1e47e-115">**Attribute**</span></span>|<span data-ttu-id="1e47e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1e47e-116">**Type**</span></span>|<span data-ttu-id="1e47e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1e47e-117">**Required**</span></span>|<span data-ttu-id="1e47e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e47e-118">**Description**</span></span>|<span data-ttu-id="1e47e-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="1e47e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e47e-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="1e47e-120">CharSets</span></span>  <br/> |<span data-ttu-id="1e47e-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1e47e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1e47e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e47e-122">optional</span></span>  <br/> ||<span data-ttu-id="1e47e-123">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e47e-124">フラグ</span><span class="sxs-lookup"><span data-stu-id="1e47e-124">Flags</span></span>  <br/> |<span data-ttu-id="1e47e-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="1e47e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1e47e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e47e-126">optional</span></span>  <br/> ||<span data-ttu-id="1e47e-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1e47e-128">NameU</span><span class="sxs-lookup"><span data-stu-id="1e47e-128">NameU</span></span>  <br/> |<span data-ttu-id="1e47e-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1e47e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1e47e-130">必須</span><span class="sxs-lookup"><span data-stu-id="1e47e-130">required</span></span>  <br/> ||<span data-ttu-id="1e47e-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e47e-132">panos</span><span class="sxs-lookup"><span data-stu-id="1e47e-132">Panos</span></span>  <br/> |<span data-ttu-id="1e47e-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1e47e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1e47e-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e47e-134">optional</span></span>  <br/> ||<span data-ttu-id="1e47e-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e47e-136">Panose</span><span class="sxs-lookup"><span data-stu-id="1e47e-136">Panose</span></span>  <br/> |<span data-ttu-id="1e47e-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1e47e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1e47e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e47e-138">optional</span></span>  <br/> ||<span data-ttu-id="1e47e-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e47e-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="1e47e-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="1e47e-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="1e47e-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1e47e-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="1e47e-142">optional</span></span>  <br/> ||<span data-ttu-id="1e47e-143">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="1e47e-143">Values of the xsd:string type.</span></span>  <br/> |
   

