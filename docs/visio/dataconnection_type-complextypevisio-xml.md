---
title: DataConnection_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 3a900e22fd36c936f689081149b484bd5e7460fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805175"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="c9e1e-102">DataConnection_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c9e1e-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c9e1e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c9e1e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9e1e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9e1e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9e1e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9e1e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9e1e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9e1e-108">なし</span><span class="sxs-lookup"><span data-stu-id="c9e1e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9e1e-109">定義</span><span class="sxs-lookup"><span data-stu-id="c9e1e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c9e1e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c9e1e-110">Elements and attributes</span></span>

<span data-ttu-id="c9e1e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9e1e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c9e1e-112">Child elements</span></span>

<span data-ttu-id="c9e1e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9e1e-114">属性</span><span class="sxs-lookup"><span data-stu-id="c9e1e-114">Attributes</span></span>

|<span data-ttu-id="c9e1e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-115">**Attribute**</span></span>|<span data-ttu-id="c9e1e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-116">**Type**</span></span>|<span data-ttu-id="c9e1e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-117">**Required**</span></span>|<span data-ttu-id="c9e1e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-118">**Description**</span></span>|<span data-ttu-id="c9e1e-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c9e1e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c9e1e-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="c9e1e-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="c9e1e-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c9e1e-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c9e1e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="c9e1e-122">optional</span></span>  <br/> ||<span data-ttu-id="c9e1e-123">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-124">コマンド</span><span class="sxs-lookup"><span data-stu-id="c9e1e-124">Command</span></span>  <br/> |<span data-ttu-id="c9e1e-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c9e1e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="c9e1e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="c9e1e-126">optional</span></span>  <br/> ||<span data-ttu-id="c9e1e-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9e1e-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="c9e1e-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c9e1e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="c9e1e-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="c9e1e-130">optional</span></span>  <br/> ||<span data-ttu-id="c9e1e-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-132">FileName</span><span class="sxs-lookup"><span data-stu-id="c9e1e-132">FileName</span></span>  <br/> |<span data-ttu-id="c9e1e-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c9e1e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c9e1e-134">必須</span><span class="sxs-lookup"><span data-stu-id="c9e1e-134">required</span></span>  <br/> ||<span data-ttu-id="c9e1e-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c9e1e-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="c9e1e-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c9e1e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="c9e1e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="c9e1e-138">optional</span></span>  <br/> ||<span data-ttu-id="c9e1e-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-140">ID</span><span class="sxs-lookup"><span data-stu-id="c9e1e-140">ID</span></span>  <br/> |<span data-ttu-id="c9e1e-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9e1e-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9e1e-142">必須</span><span class="sxs-lookup"><span data-stu-id="c9e1e-142">required</span></span>  <br/> ||<span data-ttu-id="c9e1e-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9e1e-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="c9e1e-144">Timeout</span></span>  <br/> |<span data-ttu-id="c9e1e-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9e1e-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9e1e-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="c9e1e-146">optional</span></span>  <br/> ||<span data-ttu-id="c9e1e-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9e1e-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

