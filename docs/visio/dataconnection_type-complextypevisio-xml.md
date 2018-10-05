---
title: DataConnection_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389142"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="1ae23-102">DataConnection_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1ae23-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1ae23-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1ae23-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ae23-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1ae23-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1ae23-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1ae23-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1ae23-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1ae23-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1ae23-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1ae23-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1ae23-108">なし</span><span class="sxs-lookup"><span data-stu-id="1ae23-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ae23-109">定義</span><span class="sxs-lookup"><span data-stu-id="1ae23-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1ae23-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1ae23-110">Elements and attributes</span></span>

<span data-ttu-id="1ae23-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ae23-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1ae23-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1ae23-112">Child elements</span></span>

<span data-ttu-id="1ae23-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1ae23-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ae23-114">属性</span><span class="sxs-lookup"><span data-stu-id="1ae23-114">Attributes</span></span>

|<span data-ttu-id="1ae23-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1ae23-115">**Attribute**</span></span>|<span data-ttu-id="1ae23-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1ae23-116">**Type**</span></span>|<span data-ttu-id="1ae23-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1ae23-117">**Required**</span></span>|<span data-ttu-id="1ae23-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1ae23-118">**Description**</span></span>|<span data-ttu-id="1ae23-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1ae23-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1ae23-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="1ae23-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="1ae23-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="1ae23-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1ae23-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="1ae23-122">optional</span></span>  <br/> ||<span data-ttu-id="1ae23-123">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-124">コマンド</span><span class="sxs-lookup"><span data-stu-id="1ae23-124">Command</span></span>  <br/> |<span data-ttu-id="1ae23-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1ae23-125">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae23-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="1ae23-126">optional</span></span>  <br/> ||<span data-ttu-id="1ae23-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ae23-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="1ae23-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1ae23-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae23-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="1ae23-130">optional</span></span>  <br/> ||<span data-ttu-id="1ae23-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-132">FileName</span><span class="sxs-lookup"><span data-stu-id="1ae23-132">FileName</span></span>  <br/> |<span data-ttu-id="1ae23-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1ae23-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae23-134">必須</span><span class="sxs-lookup"><span data-stu-id="1ae23-134">required</span></span>  <br/> ||<span data-ttu-id="1ae23-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1ae23-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="1ae23-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1ae23-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1ae23-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="1ae23-138">optional</span></span>  <br/> ||<span data-ttu-id="1ae23-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-140">ID</span><span class="sxs-lookup"><span data-stu-id="1ae23-140">ID</span></span>  <br/> |<span data-ttu-id="1ae23-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ae23-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ae23-142">必須</span><span class="sxs-lookup"><span data-stu-id="1ae23-142">required</span></span>  <br/> ||<span data-ttu-id="1ae23-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1ae23-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="1ae23-144">Timeout</span></span>  <br/> |<span data-ttu-id="1ae23-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1ae23-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1ae23-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="1ae23-146">optional</span></span>  <br/> ||<span data-ttu-id="1ae23-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae23-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

