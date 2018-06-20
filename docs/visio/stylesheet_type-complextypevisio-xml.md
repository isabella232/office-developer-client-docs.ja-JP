---
title: StyleSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806598"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="0888c-102">StyleSheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0888c-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0888c-103">型情報</span><span class="sxs-lookup"><span data-stu-id="0888c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0888c-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0888c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0888c-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0888c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0888c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0888c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0888c-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="0888c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0888c-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0888c-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0888c-109">定義</span><span class="sxs-lookup"><span data-stu-id="0888c-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0888c-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0888c-110">Elements and attributes</span></span>

<span data-ttu-id="0888c-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0888c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0888c-112">子要素</span><span class="sxs-lookup"><span data-stu-id="0888c-112">Child elements</span></span>

<span data-ttu-id="0888c-113">なし。</span><span class="sxs-lookup"><span data-stu-id="0888c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0888c-114">属性</span><span class="sxs-lookup"><span data-stu-id="0888c-114">Attributes</span></span>

|<span data-ttu-id="0888c-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="0888c-115">**Attribute**</span></span>|<span data-ttu-id="0888c-116">**型**</span><span class="sxs-lookup"><span data-stu-id="0888c-116">**Type**</span></span>|<span data-ttu-id="0888c-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="0888c-117">**Required**</span></span>|<span data-ttu-id="0888c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0888c-118">**Description**</span></span>|<span data-ttu-id="0888c-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0888c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0888c-120">ID</span><span class="sxs-lookup"><span data-stu-id="0888c-120">ID</span></span>  <br/> |<span data-ttu-id="0888c-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0888c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0888c-122">必須</span><span class="sxs-lookup"><span data-stu-id="0888c-122">required</span></span>  <br/> ||<span data-ttu-id="0888c-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0888c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0888c-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0888c-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="0888c-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0888c-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0888c-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="0888c-126">optional</span></span>  <br/> ||<span data-ttu-id="0888c-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0888c-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0888c-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0888c-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0888c-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0888c-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0888c-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="0888c-130">optional</span></span>  <br/> ||<span data-ttu-id="0888c-131">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0888c-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0888c-132">名前</span><span class="sxs-lookup"><span data-stu-id="0888c-132">Name</span></span>  <br/> |<span data-ttu-id="0888c-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0888c-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0888c-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="0888c-134">optional</span></span>  <br/> ||<span data-ttu-id="0888c-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0888c-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0888c-136">NameU</span><span class="sxs-lookup"><span data-stu-id="0888c-136">NameU</span></span>  <br/> |<span data-ttu-id="0888c-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0888c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0888c-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="0888c-138">optional</span></span>  <br/> ||<span data-ttu-id="0888c-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0888c-139">Values of the xsd:string type.</span></span>  <br/> |
   

