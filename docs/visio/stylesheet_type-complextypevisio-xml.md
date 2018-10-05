---
title: StyleSheet_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396002"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="a1e05-102">StyleSheet_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a1e05-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a1e05-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a1e05-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1e05-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a1e05-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1e05-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a1e05-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1e05-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1e05-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1e05-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a1e05-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1e05-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="a1e05-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1e05-109">定義</span><span class="sxs-lookup"><span data-stu-id="a1e05-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a1e05-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a1e05-110">Elements and attributes</span></span>

<span data-ttu-id="a1e05-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1e05-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1e05-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a1e05-112">Child elements</span></span>

<span data-ttu-id="a1e05-113">なし。</span><span class="sxs-lookup"><span data-stu-id="a1e05-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1e05-114">属性</span><span class="sxs-lookup"><span data-stu-id="a1e05-114">Attributes</span></span>

|<span data-ttu-id="a1e05-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="a1e05-115">**Attribute**</span></span>|<span data-ttu-id="a1e05-116">**型**</span><span class="sxs-lookup"><span data-stu-id="a1e05-116">**Type**</span></span>|<span data-ttu-id="a1e05-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="a1e05-117">**Required**</span></span>|<span data-ttu-id="a1e05-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a1e05-118">**Description**</span></span>|<span data-ttu-id="a1e05-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a1e05-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a1e05-120">ID</span><span class="sxs-lookup"><span data-stu-id="a1e05-120">ID</span></span>  <br/> |<span data-ttu-id="a1e05-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a1e05-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1e05-122">必須</span><span class="sxs-lookup"><span data-stu-id="a1e05-122">required</span></span>  <br/> ||<span data-ttu-id="a1e05-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1e05-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a1e05-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a1e05-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="a1e05-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a1e05-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1e05-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a1e05-126">optional</span></span>  <br/> ||<span data-ttu-id="a1e05-127">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1e05-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1e05-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a1e05-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a1e05-129">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a1e05-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1e05-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="a1e05-130">optional</span></span>  <br/> ||<span data-ttu-id="a1e05-131">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1e05-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1e05-132">名前</span><span class="sxs-lookup"><span data-stu-id="a1e05-132">Name</span></span>  <br/> |<span data-ttu-id="a1e05-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a1e05-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a1e05-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="a1e05-134">optional</span></span>  <br/> ||<span data-ttu-id="a1e05-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1e05-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a1e05-136">NameU</span><span class="sxs-lookup"><span data-stu-id="a1e05-136">NameU</span></span>  <br/> |<span data-ttu-id="a1e05-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a1e05-137">xsd:string</span></span>  <br/> |<span data-ttu-id="a1e05-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a1e05-138">optional</span></span>  <br/> ||<span data-ttu-id="a1e05-139">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a1e05-139">Values of the xsd:string type.</span></span>  <br/> |
   

