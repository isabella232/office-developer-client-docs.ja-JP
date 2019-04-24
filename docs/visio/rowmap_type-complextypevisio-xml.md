---
title: RowMap_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2abe0572-53bb-20fc-333f-2b69b07e99be
ms.openlocfilehash: bdc76f35cf2824d5159e945bce7e9dd2a8abe2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355735"
---
# <a name="rowmaptype-complextype-visio-xml"></a><span data-ttu-id="b7027-102">RowMap_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b7027-102">RowMap_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b7027-103">型情報</span><span class="sxs-lookup"><span data-stu-id="b7027-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7027-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b7027-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b7027-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b7027-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b7027-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="b7027-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b7027-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="b7027-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b7027-108">なし</span><span class="sxs-lookup"><span data-stu-id="b7027-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7027-109">定義</span><span class="sxs-lookup"><span data-stu-id="b7027-109">Definition</span></span>

```XML
      <xs:complexType name="RowMap_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7027-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b7027-110">Elements and attributes</span></span>

<span data-ttu-id="b7027-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7027-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b7027-112">子要素</span><span class="sxs-lookup"><span data-stu-id="b7027-112">Child elements</span></span>

<span data-ttu-id="b7027-113">なし。</span><span class="sxs-lookup"><span data-stu-id="b7027-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7027-114">属性</span><span class="sxs-lookup"><span data-stu-id="b7027-114">Attributes</span></span>

|<span data-ttu-id="b7027-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="b7027-115">**Attribute**</span></span>|<span data-ttu-id="b7027-116">**型**</span><span class="sxs-lookup"><span data-stu-id="b7027-116">**Type**</span></span>|<span data-ttu-id="b7027-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="b7027-117">**Required**</span></span>|<span data-ttu-id="b7027-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="b7027-118">**Description**</span></span>|<span data-ttu-id="b7027-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b7027-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b7027-120">PageID</span><span class="sxs-lookup"><span data-stu-id="b7027-120">PageID</span></span>  <br/> |<span data-ttu-id="b7027-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b7027-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7027-122">必須</span><span class="sxs-lookup"><span data-stu-id="b7027-122">required</span></span>  <br/> ||<span data-ttu-id="b7027-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b7027-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7027-124">RowID</span><span class="sxs-lookup"><span data-stu-id="b7027-124">RowID</span></span>  <br/> |<span data-ttu-id="b7027-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b7027-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7027-126">必須</span><span class="sxs-lookup"><span data-stu-id="b7027-126">required</span></span>  <br/> ||<span data-ttu-id="b7027-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b7027-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7027-128">ShapeID</span><span class="sxs-lookup"><span data-stu-id="b7027-128">ShapeID</span></span>  <br/> |<span data-ttu-id="b7027-129">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="b7027-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7027-130">必須</span><span class="sxs-lookup"><span data-stu-id="b7027-130">required</span></span>  <br/> ||<span data-ttu-id="b7027-131">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="b7027-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

