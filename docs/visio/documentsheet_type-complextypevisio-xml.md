---
title: DocumentSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396345"
---
# <a name="documentsheettype-complextype-visio-xml"></a><span data-ttu-id="2c69c-102">DocumentSheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="2c69c-102">DocumentSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2c69c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="2c69c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c69c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="2c69c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2c69c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2c69c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2c69c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2c69c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2c69c-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2c69c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2c69c-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="2c69c-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2c69c-109">定義</span><span class="sxs-lookup"><span data-stu-id="2c69c-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2c69c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2c69c-110">Elements and attributes</span></span>

<span data-ttu-id="2c69c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c69c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2c69c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="2c69c-112">Child elements</span></span>

<span data-ttu-id="2c69c-113">なし。</span><span class="sxs-lookup"><span data-stu-id="2c69c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c69c-114">属性</span><span class="sxs-lookup"><span data-stu-id="2c69c-114">Attributes</span></span>

|<span data-ttu-id="2c69c-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="2c69c-115">**Attribute**</span></span>|<span data-ttu-id="2c69c-116">**型**</span><span class="sxs-lookup"><span data-stu-id="2c69c-116">**Type**</span></span>|<span data-ttu-id="2c69c-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="2c69c-117">**Required**</span></span>|<span data-ttu-id="2c69c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="2c69c-118">**Description**</span></span>|<span data-ttu-id="2c69c-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="2c69c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2c69c-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="2c69c-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="2c69c-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2c69c-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2c69c-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="2c69c-122">optional</span></span>  <br/> ||<span data-ttu-id="2c69c-123">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c69c-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2c69c-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="2c69c-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="2c69c-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="2c69c-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2c69c-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="2c69c-126">optional</span></span>  <br/> ||<span data-ttu-id="2c69c-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c69c-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2c69c-128">名前</span><span class="sxs-lookup"><span data-stu-id="2c69c-128">Name</span></span>  <br/> |<span data-ttu-id="2c69c-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c69c-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2c69c-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="2c69c-130">optional</span></span>  <br/> ||<span data-ttu-id="2c69c-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c69c-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2c69c-132">NameU</span><span class="sxs-lookup"><span data-stu-id="2c69c-132">NameU</span></span>  <br/> |<span data-ttu-id="2c69c-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c69c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2c69c-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="2c69c-134">optional</span></span>  <br/> ||<span data-ttu-id="2c69c-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c69c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2c69c-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="2c69c-136">UniqueID</span></span>  <br/> |<span data-ttu-id="2c69c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2c69c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2c69c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="2c69c-138">optional</span></span>  <br/> ||<span data-ttu-id="2c69c-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c69c-139">Values of the xsd:string type.</span></span>  <br/> |
   

