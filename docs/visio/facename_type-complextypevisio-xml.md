---
title: FaceName_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382443"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="1af8c-102">FaceName_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1af8c-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1af8c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1af8c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1af8c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1af8c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1af8c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1af8c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1af8c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1af8c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1af8c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1af8c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1af8c-108">なし</span><span class="sxs-lookup"><span data-stu-id="1af8c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1af8c-109">定義</span><span class="sxs-lookup"><span data-stu-id="1af8c-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1af8c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1af8c-110">Elements and attributes</span></span>

<span data-ttu-id="1af8c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1af8c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1af8c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1af8c-112">Child elements</span></span>

<span data-ttu-id="1af8c-113">なし。</span><span class="sxs-lookup"><span data-stu-id="1af8c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1af8c-114">属性</span><span class="sxs-lookup"><span data-stu-id="1af8c-114">Attributes</span></span>

|<span data-ttu-id="1af8c-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="1af8c-115">**Attribute**</span></span>|<span data-ttu-id="1af8c-116">**型**</span><span class="sxs-lookup"><span data-stu-id="1af8c-116">**Type**</span></span>|<span data-ttu-id="1af8c-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="1af8c-117">**Required**</span></span>|<span data-ttu-id="1af8c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1af8c-118">**Description**</span></span>|<span data-ttu-id="1af8c-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1af8c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1af8c-120">文字集合</span><span class="sxs-lookup"><span data-stu-id="1af8c-120">CharSets</span></span>  <br/> |<span data-ttu-id="1af8c-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1af8c-121">xsd:string</span></span>  <br/> |<span data-ttu-id="1af8c-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="1af8c-122">optional</span></span>  <br/> ||<span data-ttu-id="1af8c-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1af8c-124">Flags</span><span class="sxs-lookup"><span data-stu-id="1af8c-124">Flags</span></span>  <br/> |<span data-ttu-id="1af8c-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1af8c-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1af8c-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="1af8c-126">optional</span></span>  <br/> ||<span data-ttu-id="1af8c-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1af8c-128">NameU</span><span class="sxs-lookup"><span data-stu-id="1af8c-128">NameU</span></span>  <br/> |<span data-ttu-id="1af8c-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1af8c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1af8c-130">必須</span><span class="sxs-lookup"><span data-stu-id="1af8c-130">required</span></span>  <br/> ||<span data-ttu-id="1af8c-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1af8c-132">Panos</span><span class="sxs-lookup"><span data-stu-id="1af8c-132">Panos</span></span>  <br/> |<span data-ttu-id="1af8c-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1af8c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1af8c-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="1af8c-134">optional</span></span>  <br/> ||<span data-ttu-id="1af8c-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1af8c-136">Panose</span><span class="sxs-lookup"><span data-stu-id="1af8c-136">Panose</span></span>  <br/> |<span data-ttu-id="1af8c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1af8c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1af8c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="1af8c-138">optional</span></span>  <br/> ||<span data-ttu-id="1af8c-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1af8c-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="1af8c-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="1af8c-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="1af8c-141">xsd:string</span></span>  <br/> |<span data-ttu-id="1af8c-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="1af8c-142">optional</span></span>  <br/> ||<span data-ttu-id="1af8c-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1af8c-143">Values of the xsd:string type.</span></span>  <br/> |
   

