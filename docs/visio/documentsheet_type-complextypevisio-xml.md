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
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="64236-102">DocumentSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="64236-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="64236-103">型情報</span><span class="sxs-lookup"><span data-stu-id="64236-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64236-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64236-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="64236-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="64236-105">**Schema file**</span></span> <br/> |<span data-ttu-id="64236-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="64236-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="64236-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="64236-107">**Extension base**</span></span> <br/> |<span data-ttu-id="64236-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="64236-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64236-109">定義</span><span class="sxs-lookup"><span data-stu-id="64236-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="64236-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="64236-110">Elements and attributes</span></span>

<span data-ttu-id="64236-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64236-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64236-112">子要素</span><span class="sxs-lookup"><span data-stu-id="64236-112">Child elements</span></span>

<span data-ttu-id="64236-113">なし。</span><span class="sxs-lookup"><span data-stu-id="64236-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64236-114">属性</span><span class="sxs-lookup"><span data-stu-id="64236-114">Attributes</span></span>

|<span data-ttu-id="64236-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="64236-115">**Attribute**</span></span>|<span data-ttu-id="64236-116">**型**</span><span class="sxs-lookup"><span data-stu-id="64236-116">**Type**</span></span>|<span data-ttu-id="64236-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="64236-117">**Required**</span></span>|<span data-ttu-id="64236-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="64236-118">**Description**</span></span>|<span data-ttu-id="64236-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="64236-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64236-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="64236-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="64236-121">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="64236-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64236-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="64236-122">optional</span></span>  <br/> ||<span data-ttu-id="64236-123">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="64236-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64236-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="64236-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="64236-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="64236-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64236-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="64236-126">optional</span></span>  <br/> ||<span data-ttu-id="64236-127">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="64236-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64236-128">名前</span><span class="sxs-lookup"><span data-stu-id="64236-128">Name</span></span>  <br/> |<span data-ttu-id="64236-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="64236-129">xsd:string</span></span>  <br/> |<span data-ttu-id="64236-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="64236-130">optional</span></span>  <br/> ||<span data-ttu-id="64236-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="64236-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64236-132">NameU</span><span class="sxs-lookup"><span data-stu-id="64236-132">NameU</span></span>  <br/> |<span data-ttu-id="64236-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="64236-133">xsd:string</span></span>  <br/> |<span data-ttu-id="64236-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="64236-134">optional</span></span>  <br/> ||<span data-ttu-id="64236-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="64236-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64236-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="64236-136">UniqueID</span></span>  <br/> |<span data-ttu-id="64236-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="64236-137">xsd:string</span></span>  <br/> |<span data-ttu-id="64236-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="64236-138">optional</span></span>  <br/> ||<span data-ttu-id="64236-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="64236-139">Values of the xsd:string type.</span></span>  <br/> |
   

