---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539650"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="7f054-102">DataConnection_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7f054-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7f054-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7f054-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f054-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f054-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7f054-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7f054-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7f054-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="7f054-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7f054-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7f054-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7f054-108">None</span><span class="sxs-lookup"><span data-stu-id="7f054-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f054-109">定義</span><span class="sxs-lookup"><span data-stu-id="7f054-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7f054-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7f054-110">Elements and attributes</span></span>

<span data-ttu-id="7f054-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f054-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f054-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7f054-112">Child elements</span></span>

<span data-ttu-id="7f054-113">なし。</span><span class="sxs-lookup"><span data-stu-id="7f054-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f054-114">属性</span><span class="sxs-lookup"><span data-stu-id="7f054-114">Attributes</span></span>

|<span data-ttu-id="7f054-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="7f054-115">**Attribute**</span></span>|<span data-ttu-id="7f054-116">**型**</span><span class="sxs-lookup"><span data-stu-id="7f054-116">**Type**</span></span>|<span data-ttu-id="7f054-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="7f054-117">**Required**</span></span>|<span data-ttu-id="7f054-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="7f054-118">**Description**</span></span>|<span data-ttu-id="7f054-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7f054-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f054-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="7f054-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="7f054-121">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="7f054-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7f054-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="7f054-122">optional</span></span>  <br/> ||<span data-ttu-id="7f054-123">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7f054-124">Command</span><span class="sxs-lookup"><span data-stu-id="7f054-124">Command</span></span>  <br/> |<span data-ttu-id="7f054-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7f054-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7f054-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="7f054-126">optional</span></span>  <br/> ||<span data-ttu-id="7f054-127">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f054-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7f054-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="7f054-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7f054-129">xsd:string</span></span>  <br/> |<span data-ttu-id="7f054-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="7f054-130">optional</span></span>  <br/> ||<span data-ttu-id="7f054-131">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f054-132">FileName</span><span class="sxs-lookup"><span data-stu-id="7f054-132">FileName</span></span>  <br/> |<span data-ttu-id="7f054-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7f054-133">xsd:string</span></span>  <br/> |<span data-ttu-id="7f054-134">必須</span><span class="sxs-lookup"><span data-stu-id="7f054-134">required</span></span>  <br/> ||<span data-ttu-id="7f054-135">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f054-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f054-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="7f054-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="7f054-137">xsd:string</span></span>  <br/> |<span data-ttu-id="7f054-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="7f054-138">optional</span></span>  <br/> ||<span data-ttu-id="7f054-139">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7f054-140">ID</span><span class="sxs-lookup"><span data-stu-id="7f054-140">ID</span></span>  <br/> |<span data-ttu-id="7f054-141">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="7f054-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f054-142">必須</span><span class="sxs-lookup"><span data-stu-id="7f054-142">required</span></span>  <br/> ||<span data-ttu-id="7f054-143">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7f054-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="7f054-144">Timeout</span></span>  <br/> |<span data-ttu-id="7f054-145">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="7f054-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f054-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="7f054-146">optional</span></span>  <br/> ||<span data-ttu-id="7f054-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f054-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

