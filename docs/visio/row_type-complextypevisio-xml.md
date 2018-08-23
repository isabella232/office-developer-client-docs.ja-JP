---
title: Row_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: dfa3a90aaec51ba89845934c1d4fad484914afa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806303"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="cf3a6-102">Row_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cf3a6-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cf3a6-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cf3a6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf3a6-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cf3a6-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cf3a6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cf3a6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cf3a6-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cf3a6-108">なし</span><span class="sxs-lookup"><span data-stu-id="cf3a6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf3a6-109">定義</span><span class="sxs-lookup"><span data-stu-id="cf3a6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cf3a6-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cf3a6-110">Elements and attributes</span></span>

<span data-ttu-id="cf3a6-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cf3a6-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cf3a6-112">Child elements</span></span>

|<span data-ttu-id="cf3a6-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-113">**Element**</span></span>|<span data-ttu-id="cf3a6-114">**型**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-114">**Type**</span></span>|<span data-ttu-id="cf3a6-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf3a6-116">Cell</span><span class="sxs-lookup"><span data-stu-id="cf3a6-116">Cell</span></span>](http://msdn.microsoft.com/library/5e060a3f-e804-834f-531b-78a544fee61f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="cf3a6-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="cf3a6-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cf3a6-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="cf3a6-118">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="cf3a6-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="cf3a6-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cf3a6-120">属性</span><span class="sxs-lookup"><span data-stu-id="cf3a6-120">Attributes</span></span>

|<span data-ttu-id="cf3a6-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-121">**Attribute**</span></span>|<span data-ttu-id="cf3a6-122">**型**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-122">**Type**</span></span>|<span data-ttu-id="cf3a6-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-123">**Required**</span></span>|<span data-ttu-id="cf3a6-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-124">**Description**</span></span>|<span data-ttu-id="cf3a6-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="cf3a6-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf3a6-126">Del</span><span class="sxs-lookup"><span data-stu-id="cf3a6-126">Del</span></span>  <br/> |<span data-ttu-id="cf3a6-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cf3a6-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cf3a6-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="cf3a6-128">optional</span></span>  <br/> ||<span data-ttu-id="cf3a6-129">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cf3a6-130">IX</span><span class="sxs-lookup"><span data-stu-id="cf3a6-130">IX</span></span>  <br/> |<span data-ttu-id="cf3a6-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cf3a6-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cf3a6-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="cf3a6-132">optional</span></span>  <br/> ||<span data-ttu-id="cf3a6-133">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cf3a6-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="cf3a6-134">LocalName</span></span>  <br/> |<span data-ttu-id="cf3a6-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cf3a6-135">xsd:string</span></span>  <br/> |<span data-ttu-id="cf3a6-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="cf3a6-136">optional</span></span>  <br/> ||<span data-ttu-id="cf3a6-137">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cf3a6-138">N</span><span class="sxs-lookup"><span data-stu-id="cf3a6-138">N</span></span>  <br/> |<span data-ttu-id="cf3a6-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cf3a6-139">xsd:string</span></span>  <br/> |<span data-ttu-id="cf3a6-140">省略可能</span><span class="sxs-lookup"><span data-stu-id="cf3a6-140">optional</span></span>  <br/> ||<span data-ttu-id="cf3a6-141">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cf3a6-142">SV 要素</span><span class="sxs-lookup"><span data-stu-id="cf3a6-142">T</span></span>  <br/> |<span data-ttu-id="cf3a6-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cf3a6-143">xsd:string</span></span>  <br/> |<span data-ttu-id="cf3a6-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="cf3a6-144">optional</span></span>  <br/> ||<span data-ttu-id="cf3a6-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf3a6-145">Values of the xsd:string type.</span></span>  <br/> |
   

