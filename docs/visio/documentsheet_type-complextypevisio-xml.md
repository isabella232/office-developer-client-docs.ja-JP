---
title: DocumentSheet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326139"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="8617e-102">DocumentSheet_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8617e-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="8617e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="8617e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8617e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8617e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8617e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8617e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8617e-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="8617e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8617e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="8617e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8617e-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="8617e-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8617e-109">定義</span><span class="sxs-lookup"><span data-stu-id="8617e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8617e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8617e-110">Elements and attributes</span></span>

<span data-ttu-id="8617e-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8617e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8617e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="8617e-112">Child elements</span></span>

<span data-ttu-id="8617e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="8617e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8617e-114">属性</span><span class="sxs-lookup"><span data-stu-id="8617e-114">Attributes</span></span>

|<span data-ttu-id="8617e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="8617e-115">**Attribute**</span></span>|<span data-ttu-id="8617e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="8617e-116">**Type**</span></span>|<span data-ttu-id="8617e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="8617e-117">**Required**</span></span>|<span data-ttu-id="8617e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="8617e-118">**Description**</span></span>|<span data-ttu-id="8617e-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8617e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8617e-120">iscustomname</span><span class="sxs-lookup"><span data-stu-id="8617e-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="8617e-121">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="8617e-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8617e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="8617e-122">optional</span></span>  <br/> ||<span data-ttu-id="8617e-123">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="8617e-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8617e-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="8617e-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="8617e-125">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="8617e-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8617e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="8617e-126">optional</span></span>  <br/> ||<span data-ttu-id="8617e-127">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="8617e-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8617e-128">名前</span><span class="sxs-lookup"><span data-stu-id="8617e-128">Name</span></span>  <br/> |<span data-ttu-id="8617e-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8617e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="8617e-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="8617e-130">optional</span></span>  <br/> ||<span data-ttu-id="8617e-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8617e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8617e-132">NameU</span><span class="sxs-lookup"><span data-stu-id="8617e-132">NameU</span></span>  <br/> |<span data-ttu-id="8617e-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8617e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8617e-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="8617e-134">optional</span></span>  <br/> ||<span data-ttu-id="8617e-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8617e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8617e-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="8617e-136">UniqueID</span></span>  <br/> |<span data-ttu-id="8617e-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="8617e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="8617e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="8617e-138">optional</span></span>  <br/> ||<span data-ttu-id="8617e-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="8617e-139">Values of the xsd:string type.</span></span>  <br/> |
   

