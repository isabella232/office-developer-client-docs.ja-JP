---
title: CellDef_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: bdcfadc36f278fc97b8589b2989d214e5f4b3333
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327126"
---
# <a name="celldeftype-complextype-visio-xml"></a><span data-ttu-id="da2bf-102">CellDef_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="da2bf-102">CellDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="da2bf-103">型情報</span><span class="sxs-lookup"><span data-stu-id="da2bf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da2bf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="da2bf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="da2bf-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="da2bf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="da2bf-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="da2bf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="da2bf-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="da2bf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="da2bf-108">なし</span><span class="sxs-lookup"><span data-stu-id="da2bf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="da2bf-109">定義</span><span class="sxs-lookup"><span data-stu-id="da2bf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="da2bf-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="da2bf-110">Elements and attributes</span></span>

<span data-ttu-id="da2bf-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="da2bf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="da2bf-112">子要素</span><span class="sxs-lookup"><span data-stu-id="da2bf-112">Child elements</span></span>

<span data-ttu-id="da2bf-113">なし。</span><span class="sxs-lookup"><span data-stu-id="da2bf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da2bf-114">属性</span><span class="sxs-lookup"><span data-stu-id="da2bf-114">Attributes</span></span>

|<span data-ttu-id="da2bf-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="da2bf-115">**Attribute**</span></span>|<span data-ttu-id="da2bf-116">**型**</span><span class="sxs-lookup"><span data-stu-id="da2bf-116">**Type**</span></span>|<span data-ttu-id="da2bf-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="da2bf-117">**Required**</span></span>|<span data-ttu-id="da2bf-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="da2bf-118">**Description**</span></span>|<span data-ttu-id="da2bf-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="da2bf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="da2bf-120">F</span><span class="sxs-lookup"><span data-stu-id="da2bf-120">F</span></span>  <br/> |<span data-ttu-id="da2bf-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="da2bf-121">xsd:string</span></span>  <br/> |<span data-ttu-id="da2bf-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="da2bf-122">optional</span></span>  <br/> ||<span data-ttu-id="da2bf-123">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="da2bf-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="da2bf-124">IX</span><span class="sxs-lookup"><span data-stu-id="da2bf-124">IX</span></span>  <br/> |<span data-ttu-id="da2bf-125">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="da2bf-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="da2bf-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="da2bf-126">optional</span></span>  <br/> ||<span data-ttu-id="da2bf-127">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="da2bf-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="da2bf-128">N</span><span class="sxs-lookup"><span data-stu-id="da2bf-128">N</span></span>  <br/> |<span data-ttu-id="da2bf-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="da2bf-129">xsd:string</span></span>  <br/> |<span data-ttu-id="da2bf-130">必須</span><span class="sxs-lookup"><span data-stu-id="da2bf-130">required</span></span>  <br/> ||<span data-ttu-id="da2bf-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="da2bf-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="da2bf-132">S</span><span class="sxs-lookup"><span data-stu-id="da2bf-132">S</span></span>  <br/> |<span data-ttu-id="da2bf-133">xsd: アン signedbyte</span><span class="sxs-lookup"><span data-stu-id="da2bf-133">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="da2bf-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="da2bf-134">optional</span></span>  <br/> ||<span data-ttu-id="da2bf-135">xsd:/signedbyte 型の値。</span><span class="sxs-lookup"><span data-stu-id="da2bf-135">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="da2bf-136">T</span><span class="sxs-lookup"><span data-stu-id="da2bf-136">T</span></span>  <br/> |<span data-ttu-id="da2bf-137">xsd: token</span><span class="sxs-lookup"><span data-stu-id="da2bf-137">xsd:token</span></span>  <br/> |<span data-ttu-id="da2bf-138">必須</span><span class="sxs-lookup"><span data-stu-id="da2bf-138">required</span></span>  <br/> ||<span data-ttu-id="da2bf-139">xsd: token 型の値。</span><span class="sxs-lookup"><span data-stu-id="da2bf-139">Values of the xsd:token type.</span></span>  <br/> |
   

