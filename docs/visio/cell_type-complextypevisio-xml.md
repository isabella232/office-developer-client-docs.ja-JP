---
title: Cell_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804980"
---
# <a name="celltype-complextype-visio-xml"></a><span data-ttu-id="04a9f-102">Cell_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="04a9f-102">Cell_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04a9f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="04a9f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04a9f-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="04a9f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04a9f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="04a9f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04a9f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04a9f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04a9f-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="04a9f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04a9f-108">なし</span><span class="sxs-lookup"><span data-stu-id="04a9f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04a9f-109">定義</span><span class="sxs-lookup"><span data-stu-id="04a9f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="04a9f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="04a9f-110">Elements and attributes</span></span>

<span data-ttu-id="04a9f-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="04a9f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04a9f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="04a9f-112">Child elements</span></span>

|<span data-ttu-id="04a9f-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="04a9f-113">**Element**</span></span>|<span data-ttu-id="04a9f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="04a9f-114">**Type**</span></span>|<span data-ttu-id="04a9f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="04a9f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="04a9f-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="04a9f-116">RefBy</span></span>](refby-element-cell_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="04a9f-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="04a9f-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="04a9f-118">属性</span><span class="sxs-lookup"><span data-stu-id="04a9f-118">Attributes</span></span>

|<span data-ttu-id="04a9f-119">**属性**</span><span class="sxs-lookup"><span data-stu-id="04a9f-119">**Attribute**</span></span>|<span data-ttu-id="04a9f-120">**型**</span><span class="sxs-lookup"><span data-stu-id="04a9f-120">**Type**</span></span>|<span data-ttu-id="04a9f-121">**必須**</span><span class="sxs-lookup"><span data-stu-id="04a9f-121">**Required**</span></span>|<span data-ttu-id="04a9f-122">**説明**</span><span class="sxs-lookup"><span data-stu-id="04a9f-122">**Description**</span></span>|<span data-ttu-id="04a9f-123">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="04a9f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04a9f-124">DurationFormat 要素</span><span class="sxs-lookup"><span data-stu-id="04a9f-124">E</span></span>  <br/> |<span data-ttu-id="04a9f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04a9f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="04a9f-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="04a9f-126">optional</span></span>  <br/> ||<span data-ttu-id="04a9f-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a9f-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04a9f-128">ExternalTaskProject 要素</span><span class="sxs-lookup"><span data-stu-id="04a9f-128">F</span></span>  <br/> |<span data-ttu-id="04a9f-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04a9f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="04a9f-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="04a9f-130">optional</span></span>  <br/> ||<span data-ttu-id="04a9f-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a9f-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04a9f-132">MultipleCriticalPaths 要素</span><span class="sxs-lookup"><span data-stu-id="04a9f-132">N</span></span>  <br/> |<span data-ttu-id="04a9f-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04a9f-133">xsd:string</span></span>  <br/> |<span data-ttu-id="04a9f-134">必須</span><span class="sxs-lookup"><span data-stu-id="04a9f-134">required</span></span>  <br/> ||<span data-ttu-id="04a9f-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a9f-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04a9f-136">U</span><span class="sxs-lookup"><span data-stu-id="04a9f-136">U</span></span>  <br/> |<span data-ttu-id="04a9f-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04a9f-137">xsd:string</span></span>  <br/> |<span data-ttu-id="04a9f-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="04a9f-138">optional</span></span>  <br/> ||<span data-ttu-id="04a9f-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a9f-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="04a9f-140">V</span><span class="sxs-lookup"><span data-stu-id="04a9f-140">V</span></span>  <br/> |<span data-ttu-id="04a9f-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="04a9f-141">xsd:string</span></span>  <br/> |<span data-ttu-id="04a9f-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="04a9f-142">optional</span></span>  <br/> ||<span data-ttu-id="04a9f-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="04a9f-143">Values of the xsd:string type.</span></span>  <br/> |
   

