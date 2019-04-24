---
title: StyleSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329826"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="fb43e-102">StyleSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="fb43e-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fb43e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="fb43e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb43e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb43e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fb43e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="fb43e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fb43e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="fb43e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fb43e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="fb43e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fb43e-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="fb43e-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb43e-109">定義</span><span class="sxs-lookup"><span data-stu-id="fb43e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fb43e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="fb43e-110">Elements and attributes</span></span>

<span data-ttu-id="fb43e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb43e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fb43e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="fb43e-112">Child elements</span></span>

<span data-ttu-id="fb43e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="fb43e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb43e-114">属性</span><span class="sxs-lookup"><span data-stu-id="fb43e-114">Attributes</span></span>

|<span data-ttu-id="fb43e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="fb43e-115">**Attribute**</span></span>|<span data-ttu-id="fb43e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="fb43e-116">**Type**</span></span>|<span data-ttu-id="fb43e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="fb43e-117">**Required**</span></span>|<span data-ttu-id="fb43e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="fb43e-118">**Description**</span></span>|<span data-ttu-id="fb43e-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="fb43e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb43e-120">ID</span><span class="sxs-lookup"><span data-stu-id="fb43e-120">ID</span></span>  <br/> |<span data-ttu-id="fb43e-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="fb43e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fb43e-122">必須</span><span class="sxs-lookup"><span data-stu-id="fb43e-122">required</span></span>  <br/> ||<span data-ttu-id="fb43e-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="fb43e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fb43e-124">iscustomname</span><span class="sxs-lookup"><span data-stu-id="fb43e-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="fb43e-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="fb43e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fb43e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb43e-126">optional</span></span>  <br/> ||<span data-ttu-id="fb43e-127">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="fb43e-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fb43e-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="fb43e-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="fb43e-129">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="fb43e-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fb43e-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb43e-130">optional</span></span>  <br/> ||<span data-ttu-id="fb43e-131">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="fb43e-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fb43e-132">名前</span><span class="sxs-lookup"><span data-stu-id="fb43e-132">Name</span></span>  <br/> |<span data-ttu-id="fb43e-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb43e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="fb43e-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb43e-134">optional</span></span>  <br/> ||<span data-ttu-id="fb43e-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fb43e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fb43e-136">NameU</span><span class="sxs-lookup"><span data-stu-id="fb43e-136">NameU</span></span>  <br/> |<span data-ttu-id="fb43e-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="fb43e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="fb43e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="fb43e-138">optional</span></span>  <br/> ||<span data-ttu-id="fb43e-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="fb43e-139">Values of the xsd:string type.</span></span>  <br/> |
   

