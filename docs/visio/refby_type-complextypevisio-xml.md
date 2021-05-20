---
title: RefBy_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538278"
---
# <a name="refby_type-complextype-visio-xml"></a><span data-ttu-id="7f842-102">RefBy_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7f842-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7f842-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7f842-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f842-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f842-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7f842-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7f842-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7f842-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7f842-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7f842-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7f842-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7f842-108">なし</span><span class="sxs-lookup"><span data-stu-id="7f842-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f842-109">定義</span><span class="sxs-lookup"><span data-stu-id="7f842-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7f842-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7f842-110">Elements and attributes</span></span>

<span data-ttu-id="7f842-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f842-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f842-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7f842-112">Child elements</span></span>

<span data-ttu-id="7f842-113">なし。</span><span class="sxs-lookup"><span data-stu-id="7f842-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f842-114">属性</span><span class="sxs-lookup"><span data-stu-id="7f842-114">Attributes</span></span>

|<span data-ttu-id="7f842-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="7f842-115">**Attribute**</span></span>|<span data-ttu-id="7f842-116">**型**</span><span class="sxs-lookup"><span data-stu-id="7f842-116">**Type**</span></span>|<span data-ttu-id="7f842-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="7f842-117">**Required**</span></span>|<span data-ttu-id="7f842-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="7f842-118">**Description**</span></span>|<span data-ttu-id="7f842-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7f842-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f842-120">ID</span><span class="sxs-lookup"><span data-stu-id="7f842-120">ID</span></span>  <br/> |<span data-ttu-id="7f842-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7f842-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7f842-122">必須</span><span class="sxs-lookup"><span data-stu-id="7f842-122">required</span></span>  <br/> ||<span data-ttu-id="7f842-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f842-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7f842-124">T</span><span class="sxs-lookup"><span data-stu-id="7f842-124">T</span></span>  <br/> |<span data-ttu-id="7f842-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7f842-125">xsd:string</span></span>  <br/> |<span data-ttu-id="7f842-126">必須</span><span class="sxs-lookup"><span data-stu-id="7f842-126">required</span></span>  <br/> ||<span data-ttu-id="7f842-127">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="7f842-127">Values of the xsd:string type.</span></span>  <br/> |
   

