---
title: AuthorEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386839"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="e50f9-102">AuthorEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e50f9-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e50f9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="e50f9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e50f9-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e50f9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e50f9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e50f9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e50f9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e50f9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e50f9-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="e50f9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e50f9-108">なし</span><span class="sxs-lookup"><span data-stu-id="e50f9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e50f9-109">定義</span><span class="sxs-lookup"><span data-stu-id="e50f9-109">Definition</span></span>

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e50f9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e50f9-110">Elements and attributes</span></span>

<span data-ttu-id="e50f9-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e50f9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e50f9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="e50f9-112">Child elements</span></span>

<span data-ttu-id="e50f9-113">なし。</span><span class="sxs-lookup"><span data-stu-id="e50f9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e50f9-114">属性</span><span class="sxs-lookup"><span data-stu-id="e50f9-114">Attributes</span></span>

|<span data-ttu-id="e50f9-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="e50f9-115">**Attribute**</span></span>|<span data-ttu-id="e50f9-116">**型**</span><span class="sxs-lookup"><span data-stu-id="e50f9-116">**Type**</span></span>|<span data-ttu-id="e50f9-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="e50f9-117">**Required**</span></span>|<span data-ttu-id="e50f9-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="e50f9-118">**Description**</span></span>|<span data-ttu-id="e50f9-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="e50f9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e50f9-120">ID</span><span class="sxs-lookup"><span data-stu-id="e50f9-120">ID</span></span>  <br/> |<span data-ttu-id="e50f9-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e50f9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e50f9-122">必須</span><span class="sxs-lookup"><span data-stu-id="e50f9-122">required</span></span>  <br/> ||<span data-ttu-id="e50f9-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e50f9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e50f9-124">Initials</span><span class="sxs-lookup"><span data-stu-id="e50f9-124">Initials</span></span>  <br/> |<span data-ttu-id="e50f9-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50f9-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e50f9-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="e50f9-126">optional</span></span>  <br/> ||<span data-ttu-id="e50f9-127">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e50f9-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e50f9-128">名前</span><span class="sxs-lookup"><span data-stu-id="e50f9-128">Name</span></span>  <br/> |<span data-ttu-id="e50f9-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50f9-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e50f9-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="e50f9-130">optional</span></span>  <br/> ||<span data-ttu-id="e50f9-131">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e50f9-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e50f9-132">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="e50f9-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="e50f9-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e50f9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="e50f9-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="e50f9-134">optional</span></span>  <br/> ||<span data-ttu-id="e50f9-135">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e50f9-135">Values of the xsd:string type.</span></span>  <br/> |
   

