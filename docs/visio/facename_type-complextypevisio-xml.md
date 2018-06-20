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
# <a name="facenametype-complextype-visio-xml"></a><span data-ttu-id="391d9-102">FaceName_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="391d9-102">FaceName_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="391d9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="391d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="391d9-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="391d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="391d9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="391d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="391d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="391d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="391d9-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="391d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="391d9-108">なし</span><span class="sxs-lookup"><span data-stu-id="391d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="391d9-109">定義</span><span class="sxs-lookup"><span data-stu-id="391d9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="391d9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="391d9-110">Elements and attributes</span></span>

<span data-ttu-id="391d9-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="391d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="391d9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="391d9-112">Child elements</span></span>

<span data-ttu-id="391d9-113">なし。</span><span class="sxs-lookup"><span data-stu-id="391d9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="391d9-114">属性</span><span class="sxs-lookup"><span data-stu-id="391d9-114">Attributes</span></span>

|<span data-ttu-id="391d9-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="391d9-115">**Attribute**</span></span>|<span data-ttu-id="391d9-116">**型**</span><span class="sxs-lookup"><span data-stu-id="391d9-116">**Type**</span></span>|<span data-ttu-id="391d9-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="391d9-117">**Required**</span></span>|<span data-ttu-id="391d9-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="391d9-118">**Description**</span></span>|<span data-ttu-id="391d9-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="391d9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="391d9-120">文字集合</span><span class="sxs-lookup"><span data-stu-id="391d9-120">CharSets</span></span>  <br/> |<span data-ttu-id="391d9-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="391d9-121">xsd:string</span></span>  <br/> |<span data-ttu-id="391d9-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="391d9-122">optional</span></span>  <br/> ||<span data-ttu-id="391d9-123">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="391d9-124">フラグ</span><span class="sxs-lookup"><span data-stu-id="391d9-124">Flags</span></span>  <br/> |<span data-ttu-id="391d9-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="391d9-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="391d9-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="391d9-126">optional</span></span>  <br/> ||<span data-ttu-id="391d9-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="391d9-128">NameU</span><span class="sxs-lookup"><span data-stu-id="391d9-128">NameU</span></span>  <br/> |<span data-ttu-id="391d9-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="391d9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="391d9-130">必須</span><span class="sxs-lookup"><span data-stu-id="391d9-130">required</span></span>  <br/> ||<span data-ttu-id="391d9-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="391d9-132">Panos</span><span class="sxs-lookup"><span data-stu-id="391d9-132">Panos</span></span>  <br/> |<span data-ttu-id="391d9-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="391d9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="391d9-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="391d9-134">optional</span></span>  <br/> ||<span data-ttu-id="391d9-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="391d9-136">Panose</span><span class="sxs-lookup"><span data-stu-id="391d9-136">Panose</span></span>  <br/> |<span data-ttu-id="391d9-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="391d9-137">xsd:string</span></span>  <br/> |<span data-ttu-id="391d9-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="391d9-138">optional</span></span>  <br/> ||<span data-ttu-id="391d9-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="391d9-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="391d9-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="391d9-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="391d9-141">xsd:string</span></span>  <br/> |<span data-ttu-id="391d9-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="391d9-142">optional</span></span>  <br/> ||<span data-ttu-id="391d9-143">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="391d9-143">Values of the xsd:string type.</span></span>  <br/> |
   

