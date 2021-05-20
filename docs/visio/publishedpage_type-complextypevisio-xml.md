---
title: PublishedPage_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39bf8983-ff70-3c81-e65b-1db5666b9969
ms.openlocfilehash: 686c63583d611e8efcc0173145dfa415400c5be3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538250"
---
# <a name="publishedpage_type-complextype-visio-xml"></a><span data-ttu-id="776ca-102">PublishedPage_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="776ca-102">PublishedPage_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="776ca-103">型情報</span><span class="sxs-lookup"><span data-stu-id="776ca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="776ca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="776ca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="776ca-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="776ca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="776ca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="776ca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="776ca-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="776ca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="776ca-108">なし</span><span class="sxs-lookup"><span data-stu-id="776ca-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="776ca-109">定義</span><span class="sxs-lookup"><span data-stu-id="776ca-109">Definition</span></span>

```XML
      <xs:complexType name="PublishedPage_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="776ca-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="776ca-110">Elements and attributes</span></span>

<span data-ttu-id="776ca-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="776ca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="776ca-112">子要素</span><span class="sxs-lookup"><span data-stu-id="776ca-112">Child elements</span></span>

<span data-ttu-id="776ca-113">なし。</span><span class="sxs-lookup"><span data-stu-id="776ca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="776ca-114">属性</span><span class="sxs-lookup"><span data-stu-id="776ca-114">Attributes</span></span>

|<span data-ttu-id="776ca-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="776ca-115">**Attribute**</span></span>|<span data-ttu-id="776ca-116">**型**</span><span class="sxs-lookup"><span data-stu-id="776ca-116">**Type**</span></span>|<span data-ttu-id="776ca-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="776ca-117">**Required**</span></span>|<span data-ttu-id="776ca-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="776ca-118">**Description**</span></span>|<span data-ttu-id="776ca-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="776ca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="776ca-120">ID</span><span class="sxs-lookup"><span data-stu-id="776ca-120">ID</span></span>  <br/> |<span data-ttu-id="776ca-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="776ca-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="776ca-122">必須</span><span class="sxs-lookup"><span data-stu-id="776ca-122">required</span></span>  <br/> ||<span data-ttu-id="776ca-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="776ca-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

