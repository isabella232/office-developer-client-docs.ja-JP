---
title: AuthorEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 7d43d34559f212e3de1a91291cbf14b75a3b2e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341385"
---
# <a name="authorentrytype-complextype-visio-xml"></a><span data-ttu-id="75b1a-102">AuthorEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="75b1a-102">AuthorEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="75b1a-103">型情報</span><span class="sxs-lookup"><span data-stu-id="75b1a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75b1a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75b1a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="75b1a-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="75b1a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="75b1a-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="75b1a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="75b1a-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="75b1a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="75b1a-108">なし</span><span class="sxs-lookup"><span data-stu-id="75b1a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75b1a-109">定義</span><span class="sxs-lookup"><span data-stu-id="75b1a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="75b1a-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="75b1a-110">Elements and attributes</span></span>

<span data-ttu-id="75b1a-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75b1a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75b1a-112">子要素</span><span class="sxs-lookup"><span data-stu-id="75b1a-112">Child elements</span></span>

<span data-ttu-id="75b1a-113">なし。</span><span class="sxs-lookup"><span data-stu-id="75b1a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75b1a-114">属性</span><span class="sxs-lookup"><span data-stu-id="75b1a-114">Attributes</span></span>

|<span data-ttu-id="75b1a-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="75b1a-115">**Attribute**</span></span>|<span data-ttu-id="75b1a-116">**型**</span><span class="sxs-lookup"><span data-stu-id="75b1a-116">**Type**</span></span>|<span data-ttu-id="75b1a-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="75b1a-117">**Required**</span></span>|<span data-ttu-id="75b1a-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="75b1a-118">**Description**</span></span>|<span data-ttu-id="75b1a-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="75b1a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75b1a-120">ID</span><span class="sxs-lookup"><span data-stu-id="75b1a-120">ID</span></span>  <br/> |<span data-ttu-id="75b1a-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="75b1a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="75b1a-122">必須</span><span class="sxs-lookup"><span data-stu-id="75b1a-122">required</span></span>  <br/> ||<span data-ttu-id="75b1a-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="75b1a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="75b1a-124">イニシャル</span><span class="sxs-lookup"><span data-stu-id="75b1a-124">Initials</span></span>  <br/> |<span data-ttu-id="75b1a-125">xsd: string</span><span class="sxs-lookup"><span data-stu-id="75b1a-125">xsd:string</span></span>  <br/> |<span data-ttu-id="75b1a-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="75b1a-126">optional</span></span>  <br/> ||<span data-ttu-id="75b1a-127">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="75b1a-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75b1a-128">名前</span><span class="sxs-lookup"><span data-stu-id="75b1a-128">Name</span></span>  <br/> |<span data-ttu-id="75b1a-129">xsd: string</span><span class="sxs-lookup"><span data-stu-id="75b1a-129">xsd:string</span></span>  <br/> |<span data-ttu-id="75b1a-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="75b1a-130">optional</span></span>  <br/> ||<span data-ttu-id="75b1a-131">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="75b1a-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="75b1a-132">解決 id</span><span class="sxs-lookup"><span data-stu-id="75b1a-132">ResolutionID</span></span>  <br/> |<span data-ttu-id="75b1a-133">xsd: string</span><span class="sxs-lookup"><span data-stu-id="75b1a-133">xsd:string</span></span>  <br/> |<span data-ttu-id="75b1a-134">省略可能</span><span class="sxs-lookup"><span data-stu-id="75b1a-134">optional</span></span>  <br/> ||<span data-ttu-id="75b1a-135">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="75b1a-135">Values of the xsd:string type.</span></span>  <br/> |
   

