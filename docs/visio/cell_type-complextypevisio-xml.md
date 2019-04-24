---
title: Cell_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: ae5f481d787ae5d07968df8cd0ef0eba6af26f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327119"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="43ac5-102">Cell_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="43ac5-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="43ac5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="43ac5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43ac5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="43ac5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="43ac5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="43ac5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="43ac5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="43ac5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="43ac5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="43ac5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="43ac5-108">なし</span><span class="sxs-lookup"><span data-stu-id="43ac5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43ac5-109">定義</span><span class="sxs-lookup"><span data-stu-id="43ac5-109">Definition</span></span>

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43ac5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="43ac5-110">Elements and attributes</span></span>

<span data-ttu-id="43ac5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43ac5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="43ac5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="43ac5-112">Child elements</span></span>

|<span data-ttu-id="43ac5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="43ac5-113">**Element**</span></span>|<span data-ttu-id="43ac5-114">**型**</span><span class="sxs-lookup"><span data-stu-id="43ac5-114">**Type**</span></span>|<span data-ttu-id="43ac5-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="43ac5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43ac5-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="43ac5-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43ac5-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="43ac5-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="43ac5-118">属性</span><span class="sxs-lookup"><span data-stu-id="43ac5-118">Attributes</span></span>

|<span data-ttu-id="43ac5-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="43ac5-119">**Attribute**</span></span>|<span data-ttu-id="43ac5-120">**型**</span><span class="sxs-lookup"><span data-stu-id="43ac5-120">**Type**</span></span>|<span data-ttu-id="43ac5-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="43ac5-121">**Required**</span></span>|<span data-ttu-id="43ac5-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="43ac5-122">**Description**</span></span>|<span data-ttu-id="43ac5-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="43ac5-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43ac5-124">E</span><span class="sxs-lookup"><span data-stu-id="43ac5-124">E</span></span>  <br/> |<span data-ttu-id="43ac5-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43ac5-125">xsd:string</span></span>  <br/> |<span data-ttu-id="43ac5-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="43ac5-126">optional</span></span>  <br/> ||<span data-ttu-id="43ac5-127">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43ac5-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43ac5-128">F</span><span class="sxs-lookup"><span data-stu-id="43ac5-128">F</span></span>  <br/> |<span data-ttu-id="43ac5-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43ac5-129">xsd:string</span></span>  <br/> |<span data-ttu-id="43ac5-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="43ac5-130">optional</span></span>  <br/> ||<span data-ttu-id="43ac5-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43ac5-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43ac5-132">N</span><span class="sxs-lookup"><span data-stu-id="43ac5-132">N</span></span>  <br/> |<span data-ttu-id="43ac5-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43ac5-133">xsd:string</span></span>  <br/> |<span data-ttu-id="43ac5-134">必須</span><span class="sxs-lookup"><span data-stu-id="43ac5-134">required</span></span>  <br/> ||<span data-ttu-id="43ac5-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43ac5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43ac5-136">U</span><span class="sxs-lookup"><span data-stu-id="43ac5-136">U</span></span>  <br/> |<span data-ttu-id="43ac5-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43ac5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="43ac5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="43ac5-138">optional</span></span>  <br/> ||<span data-ttu-id="43ac5-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43ac5-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="43ac5-140">V</span><span class="sxs-lookup"><span data-stu-id="43ac5-140">V</span></span>  <br/> |<span data-ttu-id="43ac5-141">xsd: string</span><span class="sxs-lookup"><span data-stu-id="43ac5-141">xsd:string</span></span>  <br/> |<span data-ttu-id="43ac5-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="43ac5-142">optional</span></span>  <br/> ||<span data-ttu-id="43ac5-143">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="43ac5-143">Values of the xsd:string type.</span></span>  <br/> |
   

