---
title: Cell_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: 4e0cedaab755dab669d79ff52742b8ac2b9f9725
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542304"
---
# <a name="cell_type-complextype-visio-xml"></a><span data-ttu-id="c1fc0-102">Cell_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c1fc0-102">Cell_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c1fc0-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c1fc0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1fc0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c1fc0-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c1fc0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c1fc0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c1fc0-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c1fc0-108">なし</span><span class="sxs-lookup"><span data-stu-id="c1fc0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1fc0-109">定義</span><span class="sxs-lookup"><span data-stu-id="c1fc0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c1fc0-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c1fc0-110">Elements and attributes</span></span>

<span data-ttu-id="c1fc0-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c1fc0-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c1fc0-112">Child elements</span></span>

|<span data-ttu-id="c1fc0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-113">**Element**</span></span>|<span data-ttu-id="c1fc0-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-114">**Type**</span></span>|<span data-ttu-id="c1fc0-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1fc0-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="c1fc0-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1fc0-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c1fc0-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c1fc0-118">属性</span><span class="sxs-lookup"><span data-stu-id="c1fc0-118">Attributes</span></span>

|<span data-ttu-id="c1fc0-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-119">**Attribute**</span></span>|<span data-ttu-id="c1fc0-120">**型**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-120">**Type**</span></span>|<span data-ttu-id="c1fc0-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-121">**Required**</span></span>|<span data-ttu-id="c1fc0-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-122">**Description**</span></span>|<span data-ttu-id="c1fc0-123">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="c1fc0-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1fc0-124">E</span><span class="sxs-lookup"><span data-stu-id="c1fc0-124">E</span></span>  <br/> |<span data-ttu-id="c1fc0-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1fc0-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c1fc0-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="c1fc0-126">optional</span></span>  <br/> ||<span data-ttu-id="c1fc0-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1fc0-128">F</span><span class="sxs-lookup"><span data-stu-id="c1fc0-128">F</span></span>  <br/> |<span data-ttu-id="c1fc0-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1fc0-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c1fc0-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="c1fc0-130">optional</span></span>  <br/> ||<span data-ttu-id="c1fc0-131">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1fc0-132">N</span><span class="sxs-lookup"><span data-stu-id="c1fc0-132">N</span></span>  <br/> |<span data-ttu-id="c1fc0-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1fc0-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c1fc0-134">必須</span><span class="sxs-lookup"><span data-stu-id="c1fc0-134">required</span></span>  <br/> ||<span data-ttu-id="c1fc0-135">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1fc0-136">U</span><span class="sxs-lookup"><span data-stu-id="c1fc0-136">U</span></span>  <br/> |<span data-ttu-id="c1fc0-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1fc0-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c1fc0-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c1fc0-138">optional</span></span>  <br/> ||<span data-ttu-id="c1fc0-139">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1fc0-140">V</span><span class="sxs-lookup"><span data-stu-id="c1fc0-140">V</span></span>  <br/> |<span data-ttu-id="c1fc0-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1fc0-141">xsd:string</span></span>  <br/> |<span data-ttu-id="c1fc0-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="c1fc0-142">optional</span></span>  <br/> ||<span data-ttu-id="c1fc0-143">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="c1fc0-143">Values of the xsd:string type.</span></span>  <br/> |
   

