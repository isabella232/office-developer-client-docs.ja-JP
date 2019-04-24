---
title: PublishedPage_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39bf8983-ff70-3c81-e65b-1db5666b9969
ms.openlocfilehash: e8fe5f1ba3541ba367f5c56a9bdb926358cd68cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326832"
---
# <a name="publishedpagetype-complextype-visio-xml"></a><span data-ttu-id="d773b-102">PublishedPage_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d773b-102">PublishedPage_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d773b-103">型情報</span><span class="sxs-lookup"><span data-stu-id="d773b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d773b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d773b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d773b-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d773b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d773b-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="d773b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d773b-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d773b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d773b-108">なし</span><span class="sxs-lookup"><span data-stu-id="d773b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d773b-109">定義</span><span class="sxs-lookup"><span data-stu-id="d773b-109">Definition</span></span>

```XML
      <xs:complexType name="PublishedPage_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d773b-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d773b-110">Elements and attributes</span></span>

<span data-ttu-id="d773b-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d773b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d773b-112">子要素</span><span class="sxs-lookup"><span data-stu-id="d773b-112">Child elements</span></span>

<span data-ttu-id="d773b-113">なし。</span><span class="sxs-lookup"><span data-stu-id="d773b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d773b-114">属性</span><span class="sxs-lookup"><span data-stu-id="d773b-114">Attributes</span></span>

|<span data-ttu-id="d773b-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="d773b-115">**Attribute**</span></span>|<span data-ttu-id="d773b-116">**型**</span><span class="sxs-lookup"><span data-stu-id="d773b-116">**Type**</span></span>|<span data-ttu-id="d773b-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="d773b-117">**Required**</span></span>|<span data-ttu-id="d773b-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="d773b-118">**Description**</span></span>|<span data-ttu-id="d773b-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d773b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d773b-120">ID</span><span class="sxs-lookup"><span data-stu-id="d773b-120">ID</span></span>  <br/> |<span data-ttu-id="d773b-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="d773b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d773b-122">必須</span><span class="sxs-lookup"><span data-stu-id="d773b-122">required</span></span>  <br/> ||<span data-ttu-id="d773b-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="d773b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

