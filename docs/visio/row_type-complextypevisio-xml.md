---
title: Row_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: ebd3b666590e6144d2a3cb6e0059b64eb6e8dab5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391578"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="c707c-102">Row_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c707c-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c707c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="c707c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c707c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c707c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c707c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c707c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c707c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c707c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c707c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="c707c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c707c-108">なし</span><span class="sxs-lookup"><span data-stu-id="c707c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c707c-109">定義</span><span class="sxs-lookup"><span data-stu-id="c707c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c707c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c707c-110">Elements and attributes</span></span>

<span data-ttu-id="c707c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c707c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c707c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="c707c-112">Child elements</span></span>

|<span data-ttu-id="c707c-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="c707c-113">**Element**</span></span>|<span data-ttu-id="c707c-114">**型**</span><span class="sxs-lookup"><span data-stu-id="c707c-114">**Type**</span></span>|<span data-ttu-id="c707c-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="c707c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c707c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="c707c-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="c707c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="c707c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c707c-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="c707c-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="c707c-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c707c-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c707c-120">属性</span><span class="sxs-lookup"><span data-stu-id="c707c-120">Attributes</span></span>

|<span data-ttu-id="c707c-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="c707c-121">**Attribute**</span></span>|<span data-ttu-id="c707c-122">**型**</span><span class="sxs-lookup"><span data-stu-id="c707c-122">**Type**</span></span>|<span data-ttu-id="c707c-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="c707c-123">**Required**</span></span>|<span data-ttu-id="c707c-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="c707c-124">**Description**</span></span>|<span data-ttu-id="c707c-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c707c-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c707c-126">Del</span><span class="sxs-lookup"><span data-stu-id="c707c-126">Del</span></span>  <br/> |<span data-ttu-id="c707c-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c707c-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c707c-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="c707c-128">optional</span></span>  <br/> ||<span data-ttu-id="c707c-129">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c707c-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c707c-130">IX</span><span class="sxs-lookup"><span data-stu-id="c707c-130">IX</span></span>  <br/> |<span data-ttu-id="c707c-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c707c-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c707c-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="c707c-132">optional</span></span>  <br/> ||<span data-ttu-id="c707c-133">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c707c-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c707c-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="c707c-134">LocalName</span></span>  <br/> |<span data-ttu-id="c707c-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c707c-135">xsd:string</span></span>  <br/> |<span data-ttu-id="c707c-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="c707c-136">optional</span></span>  <br/> ||<span data-ttu-id="c707c-137">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c707c-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c707c-138">N</span><span class="sxs-lookup"><span data-stu-id="c707c-138">N</span></span>  <br/> |<span data-ttu-id="c707c-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c707c-139">xsd:string</span></span>  <br/> |<span data-ttu-id="c707c-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="c707c-140">optional</span></span>  <br/> ||<span data-ttu-id="c707c-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c707c-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c707c-142">SV 要素</span><span class="sxs-lookup"><span data-stu-id="c707c-142">T</span></span>  <br/> |<span data-ttu-id="c707c-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c707c-143">xsd:string</span></span>  <br/> |<span data-ttu-id="c707c-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="c707c-144">optional</span></span>  <br/> ||<span data-ttu-id="c707c-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c707c-145">Values of the xsd:string type.</span></span>  <br/> |
   

