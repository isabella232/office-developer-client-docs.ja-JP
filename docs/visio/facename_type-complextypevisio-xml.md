---
title: FaceName_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542899"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="0640f-102">FaceName_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0640f-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0640f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0640f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0640f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0640f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0640f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0640f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0640f-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="0640f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0640f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0640f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0640f-108">None</span><span class="sxs-lookup"><span data-stu-id="0640f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0640f-109">定義</span><span class="sxs-lookup"><span data-stu-id="0640f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0640f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0640f-110">Elements and attributes</span></span>

<span data-ttu-id="0640f-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0640f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0640f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0640f-112">Child elements</span></span>

<span data-ttu-id="0640f-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0640f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0640f-114">属性</span><span class="sxs-lookup"><span data-stu-id="0640f-114">Attributes</span></span>

|<span data-ttu-id="0640f-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="0640f-115">**Attribute**</span></span>|<span data-ttu-id="0640f-116">**型**</span><span class="sxs-lookup"><span data-stu-id="0640f-116">**Type**</span></span>|<span data-ttu-id="0640f-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="0640f-117">**Required**</span></span>|<span data-ttu-id="0640f-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0640f-118">**Description**</span></span>|<span data-ttu-id="0640f-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0640f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0640f-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="0640f-120">CharSets</span></span>  <br/> |<span data-ttu-id="0640f-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0640f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="0640f-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="0640f-122">optional</span></span>  <br/> ||<span data-ttu-id="0640f-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0640f-124">フラグ</span><span class="sxs-lookup"><span data-stu-id="0640f-124">Flags</span></span>  <br/> |<span data-ttu-id="0640f-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="0640f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0640f-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="0640f-126">optional</span></span>  <br/> ||<span data-ttu-id="0640f-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0640f-128">NameU</span><span class="sxs-lookup"><span data-stu-id="0640f-128">NameU</span></span>  <br/> |<span data-ttu-id="0640f-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0640f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0640f-130">必須</span><span class="sxs-lookup"><span data-stu-id="0640f-130">required</span></span>  <br/> ||<span data-ttu-id="0640f-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0640f-132">Panos</span><span class="sxs-lookup"><span data-stu-id="0640f-132">Panos</span></span>  <br/> |<span data-ttu-id="0640f-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0640f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0640f-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="0640f-134">optional</span></span>  <br/> ||<span data-ttu-id="0640f-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0640f-136">Panose</span><span class="sxs-lookup"><span data-stu-id="0640f-136">Panose</span></span>  <br/> |<span data-ttu-id="0640f-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0640f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0640f-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0640f-138">optional</span></span>  <br/> ||<span data-ttu-id="0640f-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0640f-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="0640f-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="0640f-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0640f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="0640f-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="0640f-142">optional</span></span>  <br/> ||<span data-ttu-id="0640f-143">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0640f-143">Values of the xsd:string type.</span></span>  <br/> |
   

