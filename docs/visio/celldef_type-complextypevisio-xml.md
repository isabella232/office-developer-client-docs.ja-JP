---
title: CellDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327126"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="7cf47-102">CellDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7cf47-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7cf47-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7cf47-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cf47-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7cf47-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7cf47-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7cf47-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7cf47-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7cf47-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7cf47-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7cf47-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7cf47-108">なし</span><span class="sxs-lookup"><span data-stu-id="7cf47-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cf47-109">定義</span><span class="sxs-lookup"><span data-stu-id="7cf47-109">Definition</span></span>

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7cf47-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7cf47-110">Elements and attributes</span></span>

<span data-ttu-id="7cf47-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7cf47-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7cf47-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7cf47-112">Child elements</span></span>

<span data-ttu-id="7cf47-113">なし。</span><span class="sxs-lookup"><span data-stu-id="7cf47-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cf47-114">属性</span><span class="sxs-lookup"><span data-stu-id="7cf47-114">Attributes</span></span>

|<span data-ttu-id="7cf47-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="7cf47-115">**Attribute**</span></span>|<span data-ttu-id="7cf47-116">**型**</span><span class="sxs-lookup"><span data-stu-id="7cf47-116">**Type**</span></span>|<span data-ttu-id="7cf47-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="7cf47-117">**Required**</span></span>|<span data-ttu-id="7cf47-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="7cf47-118">**Description**</span></span>|<span data-ttu-id="7cf47-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7cf47-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7cf47-120">F</span><span class="sxs-lookup"><span data-stu-id="7cf47-120">F</span></span>  <br/> |<span data-ttu-id="7cf47-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7cf47-121">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf47-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="7cf47-122">optional</span></span>  <br/> ||<span data-ttu-id="7cf47-123">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7cf47-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf47-124">IX</span><span class="sxs-lookup"><span data-stu-id="7cf47-124">IX</span></span>  <br/> |<span data-ttu-id="7cf47-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7cf47-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7cf47-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="7cf47-126">optional</span></span>  <br/> ||<span data-ttu-id="7cf47-127">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="7cf47-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7cf47-128">N</span><span class="sxs-lookup"><span data-stu-id="7cf47-128">N</span></span>  <br/> |<span data-ttu-id="7cf47-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7cf47-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7cf47-130">必須</span><span class="sxs-lookup"><span data-stu-id="7cf47-130">required</span></span>  <br/> ||<span data-ttu-id="7cf47-131">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7cf47-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7cf47-132">S</span><span class="sxs-lookup"><span data-stu-id="7cf47-132">S</span></span>  <br/> |<span data-ttu-id="7cf47-133">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="7cf47-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="7cf47-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="7cf47-134">optional</span></span>  <br/> ||<span data-ttu-id="7cf47-135">xsd:unsignedByte 型の値。</span><span class="sxs-lookup"><span data-stu-id="7cf47-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="7cf47-136">T</span><span class="sxs-lookup"><span data-stu-id="7cf47-136">T</span></span>  <br/> |<span data-ttu-id="7cf47-137">xsd:token</span><span class="sxs-lookup"><span data-stu-id="7cf47-137">xsd:token</span></span>  <br/> |<span data-ttu-id="7cf47-138">必須</span><span class="sxs-lookup"><span data-stu-id="7cf47-138">required</span></span>  <br/> ||<span data-ttu-id="7cf47-139">xsd:token 型の値。</span><span class="sxs-lookup"><span data-stu-id="7cf47-139">Values of the xsd:token type.</span></span>  <br/> |
   

