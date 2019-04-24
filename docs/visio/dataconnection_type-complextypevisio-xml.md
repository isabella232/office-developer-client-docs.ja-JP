---
title: DataConnection_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344605"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="87c8c-102">DataConnection_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="87c8c-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="87c8c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="87c8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87c8c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87c8c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="87c8c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="87c8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="87c8c-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="87c8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="87c8c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="87c8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="87c8c-108">なし</span><span class="sxs-lookup"><span data-stu-id="87c8c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87c8c-109">定義</span><span class="sxs-lookup"><span data-stu-id="87c8c-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87c8c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="87c8c-110">Elements and attributes</span></span>

<span data-ttu-id="87c8c-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="87c8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="87c8c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="87c8c-112">Child elements</span></span>

<span data-ttu-id="87c8c-113">なし。</span><span class="sxs-lookup"><span data-stu-id="87c8c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87c8c-114">属性</span><span class="sxs-lookup"><span data-stu-id="87c8c-114">Attributes</span></span>

|<span data-ttu-id="87c8c-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="87c8c-115">**Attribute**</span></span>|<span data-ttu-id="87c8c-116">**型**</span><span class="sxs-lookup"><span data-stu-id="87c8c-116">**Type**</span></span>|<span data-ttu-id="87c8c-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="87c8c-117">**Required**</span></span>|<span data-ttu-id="87c8c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="87c8c-118">**Description**</span></span>|<span data-ttu-id="87c8c-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="87c8c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="87c8c-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="87c8c-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="87c8c-121">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="87c8c-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="87c8c-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="87c8c-122">optional</span></span>  <br/> ||<span data-ttu-id="87c8c-123">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-124">Command</span><span class="sxs-lookup"><span data-stu-id="87c8c-124">Command</span></span>  <br/> |<span data-ttu-id="87c8c-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87c8c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="87c8c-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="87c8c-126">optional</span></span>  <br/> ||<span data-ttu-id="87c8c-127">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="87c8c-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="87c8c-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87c8c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="87c8c-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="87c8c-130">optional</span></span>  <br/> ||<span data-ttu-id="87c8c-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-132">FileName</span><span class="sxs-lookup"><span data-stu-id="87c8c-132">FileName</span></span>  <br/> |<span data-ttu-id="87c8c-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87c8c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="87c8c-134">必須</span><span class="sxs-lookup"><span data-stu-id="87c8c-134">required</span></span>  <br/> ||<span data-ttu-id="87c8c-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="87c8c-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="87c8c-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="87c8c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="87c8c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="87c8c-138">optional</span></span>  <br/> ||<span data-ttu-id="87c8c-139">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-140">ID</span><span class="sxs-lookup"><span data-stu-id="87c8c-140">ID</span></span>  <br/> |<span data-ttu-id="87c8c-141">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="87c8c-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87c8c-142">必須</span><span class="sxs-lookup"><span data-stu-id="87c8c-142">required</span></span>  <br/> ||<span data-ttu-id="87c8c-143">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="87c8c-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="87c8c-144">Timeout</span></span>  <br/> |<span data-ttu-id="87c8c-145">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="87c8c-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="87c8c-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="87c8c-146">optional</span></span>  <br/> ||<span data-ttu-id="87c8c-147">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="87c8c-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

