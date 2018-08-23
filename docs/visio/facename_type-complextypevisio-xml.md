---
title: FaceName_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 554a8144fd38c34d59aa2fd0ae25d171c20cd8ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805343"
---
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="cb82e-102">FaceName_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cb82e-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cb82e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="cb82e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb82e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cb82e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cb82e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cb82e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cb82e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cb82e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cb82e-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="cb82e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cb82e-108">なし</span><span class="sxs-lookup"><span data-stu-id="cb82e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb82e-109">定義</span><span class="sxs-lookup"><span data-stu-id="cb82e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cb82e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cb82e-110">Elements and attributes</span></span>

<span data-ttu-id="cb82e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb82e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cb82e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="cb82e-112">Child elements</span></span>

<span data-ttu-id="cb82e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="cb82e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb82e-114">属性</span><span class="sxs-lookup"><span data-stu-id="cb82e-114">Attributes</span></span>

|<span data-ttu-id="cb82e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb82e-115">**Attribute**</span></span>|<span data-ttu-id="cb82e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="cb82e-116">**Type**</span></span>|<span data-ttu-id="cb82e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="cb82e-117">**Required**</span></span>|<span data-ttu-id="cb82e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="cb82e-118">**Description**</span></span>|<span data-ttu-id="cb82e-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="cb82e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb82e-120">文字集合</span><span class="sxs-lookup"><span data-stu-id="cb82e-120">CharSets</span></span>  <br/> |<span data-ttu-id="cb82e-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb82e-121">xsd:string</span></span>  <br/> |<span data-ttu-id="cb82e-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb82e-122">optional</span></span>  <br/> ||<span data-ttu-id="cb82e-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb82e-124">Flags</span><span class="sxs-lookup"><span data-stu-id="cb82e-124">Flags</span></span>  <br/> |<span data-ttu-id="cb82e-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cb82e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb82e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb82e-126">optional</span></span>  <br/> ||<span data-ttu-id="cb82e-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb82e-128">NameU</span><span class="sxs-lookup"><span data-stu-id="cb82e-128">NameU</span></span>  <br/> |<span data-ttu-id="cb82e-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb82e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="cb82e-130">必須</span><span class="sxs-lookup"><span data-stu-id="cb82e-130">required</span></span>  <br/> ||<span data-ttu-id="cb82e-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb82e-132">Panos</span><span class="sxs-lookup"><span data-stu-id="cb82e-132">Panos</span></span>  <br/> |<span data-ttu-id="cb82e-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb82e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cb82e-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb82e-134">optional</span></span>  <br/> ||<span data-ttu-id="cb82e-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb82e-136">Panose</span><span class="sxs-lookup"><span data-stu-id="cb82e-136">Panose</span></span>  <br/> |<span data-ttu-id="cb82e-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb82e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="cb82e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb82e-138">optional</span></span>  <br/> ||<span data-ttu-id="cb82e-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb82e-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="cb82e-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="cb82e-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb82e-141">xsd:string</span></span>  <br/> |<span data-ttu-id="cb82e-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="cb82e-142">optional</span></span>  <br/> ||<span data-ttu-id="cb82e-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb82e-143">Values of the xsd:string type.</span></span>  <br/> |
   

