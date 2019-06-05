---
title: Row_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: d728363e6a3e7cd7fca2b95d91469f0d50ae1c39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538159"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="0e04f-102">Row_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0e04f-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0e04f-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0e04f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e04f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0e04f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0e04f-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0e04f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0e04f-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="0e04f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0e04f-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="0e04f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0e04f-108">None</span><span class="sxs-lookup"><span data-stu-id="0e04f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0e04f-109">定義</span><span class="sxs-lookup"><span data-stu-id="0e04f-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0e04f-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0e04f-110">Elements and attributes</span></span>

<span data-ttu-id="0e04f-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e04f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0e04f-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0e04f-112">Child elements</span></span>

|<span data-ttu-id="0e04f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e04f-113">**Element**</span></span>|<span data-ttu-id="0e04f-114">**型**</span><span class="sxs-lookup"><span data-stu-id="0e04f-114">**Type**</span></span>|<span data-ttu-id="0e04f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e04f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0e04f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0e04f-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="0e04f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0e04f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0e04f-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="0e04f-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="0e04f-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="0e04f-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0e04f-120">属性</span><span class="sxs-lookup"><span data-stu-id="0e04f-120">Attributes</span></span>

|<span data-ttu-id="0e04f-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="0e04f-121">**Attribute**</span></span>|<span data-ttu-id="0e04f-122">**型**</span><span class="sxs-lookup"><span data-stu-id="0e04f-122">**Type**</span></span>|<span data-ttu-id="0e04f-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="0e04f-123">**Required**</span></span>|<span data-ttu-id="0e04f-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e04f-124">**Description**</span></span>|<span data-ttu-id="0e04f-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="0e04f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0e04f-126">Del</span><span class="sxs-lookup"><span data-stu-id="0e04f-126">Del</span></span>  <br/> |<span data-ttu-id="0e04f-127">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="0e04f-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0e04f-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="0e04f-128">optional</span></span>  <br/> ||<span data-ttu-id="0e04f-129">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="0e04f-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0e04f-130">IX</span><span class="sxs-lookup"><span data-stu-id="0e04f-130">IX</span></span>  <br/> |<span data-ttu-id="0e04f-131">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="0e04f-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0e04f-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="0e04f-132">optional</span></span>  <br/> ||<span data-ttu-id="0e04f-133">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="0e04f-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0e04f-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="0e04f-134">LocalName</span></span>  <br/> |<span data-ttu-id="0e04f-135">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0e04f-135">xsd:string</span></span>  <br/> |<span data-ttu-id="0e04f-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="0e04f-136">optional</span></span>  <br/> ||<span data-ttu-id="0e04f-137">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0e04f-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e04f-138">N</span><span class="sxs-lookup"><span data-stu-id="0e04f-138">N</span></span>  <br/> |<span data-ttu-id="0e04f-139">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0e04f-139">xsd:string</span></span>  <br/> |<span data-ttu-id="0e04f-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="0e04f-140">optional</span></span>  <br/> ||<span data-ttu-id="0e04f-141">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0e04f-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0e04f-142">T</span><span class="sxs-lookup"><span data-stu-id="0e04f-142">T</span></span>  <br/> |<span data-ttu-id="0e04f-143">xsd: string</span><span class="sxs-lookup"><span data-stu-id="0e04f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="0e04f-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="0e04f-144">optional</span></span>  <br/> ||<span data-ttu-id="0e04f-145">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="0e04f-145">Values of the xsd:string type.</span></span>  <br/> |
   

