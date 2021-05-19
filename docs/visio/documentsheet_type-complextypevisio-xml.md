---
title: DocumentSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540008"
---
# <a name="documentsheet_type-complextype-visio-xml"></a><span data-ttu-id="016a2-102">DocumentSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="016a2-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="016a2-103">型情報</span><span class="sxs-lookup"><span data-stu-id="016a2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="016a2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="016a2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="016a2-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="016a2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="016a2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="016a2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="016a2-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="016a2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="016a2-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="016a2-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="016a2-109">定義</span><span class="sxs-lookup"><span data-stu-id="016a2-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="016a2-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="016a2-110">Elements and attributes</span></span>

<span data-ttu-id="016a2-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="016a2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="016a2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="016a2-112">Child elements</span></span>

<span data-ttu-id="016a2-113">なし。</span><span class="sxs-lookup"><span data-stu-id="016a2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="016a2-114">属性</span><span class="sxs-lookup"><span data-stu-id="016a2-114">Attributes</span></span>

|<span data-ttu-id="016a2-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="016a2-115">**Attribute**</span></span>|<span data-ttu-id="016a2-116">**型**</span><span class="sxs-lookup"><span data-stu-id="016a2-116">**Type**</span></span>|<span data-ttu-id="016a2-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="016a2-117">**Required**</span></span>|<span data-ttu-id="016a2-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="016a2-118">**Description**</span></span>|<span data-ttu-id="016a2-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="016a2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="016a2-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="016a2-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="016a2-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="016a2-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="016a2-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="016a2-122">optional</span></span>  <br/> ||<span data-ttu-id="016a2-123">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="016a2-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="016a2-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="016a2-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="016a2-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="016a2-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="016a2-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="016a2-126">optional</span></span>  <br/> ||<span data-ttu-id="016a2-127">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="016a2-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="016a2-128">名前</span><span class="sxs-lookup"><span data-stu-id="016a2-128">Name</span></span>  <br/> |<span data-ttu-id="016a2-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="016a2-129">xsd:string</span></span>  <br/> |<span data-ttu-id="016a2-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="016a2-130">optional</span></span>  <br/> ||<span data-ttu-id="016a2-131">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="016a2-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="016a2-132">NameU</span><span class="sxs-lookup"><span data-stu-id="016a2-132">NameU</span></span>  <br/> |<span data-ttu-id="016a2-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="016a2-133">xsd:string</span></span>  <br/> |<span data-ttu-id="016a2-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="016a2-134">optional</span></span>  <br/> ||<span data-ttu-id="016a2-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="016a2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="016a2-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="016a2-136">UniqueID</span></span>  <br/> |<span data-ttu-id="016a2-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="016a2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="016a2-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="016a2-138">optional</span></span>  <br/> ||<span data-ttu-id="016a2-139">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="016a2-139">Values of the xsd:string type.</span></span>  <br/> |
   

