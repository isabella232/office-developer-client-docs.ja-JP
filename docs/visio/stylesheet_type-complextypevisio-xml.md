---
title: StyleSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 6dcb6bbfd01c37b499dfca4d54d6cb0832e59b5a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541982"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="a7b90-102">StyleSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a7b90-102">StyleSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a7b90-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a7b90-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7b90-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a7b90-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a7b90-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a7b90-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a7b90-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="a7b90-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a7b90-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a7b90-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a7b90-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a7b90-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a7b90-109">定義</span><span class="sxs-lookup"><span data-stu-id="a7b90-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a7b90-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a7b90-110">Elements and attributes</span></span>

<span data-ttu-id="a7b90-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7b90-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a7b90-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a7b90-112">Child elements</span></span>

<span data-ttu-id="a7b90-113">なし。</span><span class="sxs-lookup"><span data-stu-id="a7b90-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7b90-114">属性</span><span class="sxs-lookup"><span data-stu-id="a7b90-114">Attributes</span></span>

|<span data-ttu-id="a7b90-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="a7b90-115">**Attribute**</span></span>|<span data-ttu-id="a7b90-116">**型**</span><span class="sxs-lookup"><span data-stu-id="a7b90-116">**Type**</span></span>|<span data-ttu-id="a7b90-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="a7b90-117">**Required**</span></span>|<span data-ttu-id="a7b90-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a7b90-118">**Description**</span></span>|<span data-ttu-id="a7b90-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a7b90-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a7b90-120">ID</span><span class="sxs-lookup"><span data-stu-id="a7b90-120">ID</span></span>  <br/> |<span data-ttu-id="a7b90-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="a7b90-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a7b90-122">必須</span><span class="sxs-lookup"><span data-stu-id="a7b90-122">required</span></span>  <br/> ||<span data-ttu-id="a7b90-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="a7b90-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a7b90-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a7b90-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="a7b90-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="a7b90-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a7b90-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a7b90-126">optional</span></span>  <br/> ||<span data-ttu-id="a7b90-127">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a7b90-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a7b90-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a7b90-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a7b90-129">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="a7b90-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a7b90-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="a7b90-130">optional</span></span>  <br/> ||<span data-ttu-id="a7b90-131">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="a7b90-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a7b90-132">名前</span><span class="sxs-lookup"><span data-stu-id="a7b90-132">Name</span></span>  <br/> |<span data-ttu-id="a7b90-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a7b90-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a7b90-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="a7b90-134">optional</span></span>  <br/> ||<span data-ttu-id="a7b90-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a7b90-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a7b90-136">NameU</span><span class="sxs-lookup"><span data-stu-id="a7b90-136">NameU</span></span>  <br/> |<span data-ttu-id="a7b90-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="a7b90-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a7b90-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a7b90-138">optional</span></span>  <br/> ||<span data-ttu-id="a7b90-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="a7b90-139">Values of the xsd:string type.</span></span>  <br/> |
   

