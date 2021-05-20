---
title: RuleInfo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541646"
---
# <a name="ruleinfo_type-complextype-visio-xml"></a><span data-ttu-id="7c825-102">RuleInfo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7c825-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7c825-103">型情報</span><span class="sxs-lookup"><span data-stu-id="7c825-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c825-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c825-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c825-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7c825-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c825-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7c825-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c825-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="7c825-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c825-108">なし</span><span class="sxs-lookup"><span data-stu-id="7c825-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c825-109">定義</span><span class="sxs-lookup"><span data-stu-id="7c825-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c825-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7c825-110">Elements and attributes</span></span>

<span data-ttu-id="7c825-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c825-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c825-112">子要素</span><span class="sxs-lookup"><span data-stu-id="7c825-112">Child elements</span></span>

<span data-ttu-id="7c825-113">なし。</span><span class="sxs-lookup"><span data-stu-id="7c825-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c825-114">属性</span><span class="sxs-lookup"><span data-stu-id="7c825-114">Attributes</span></span>

|<span data-ttu-id="7c825-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="7c825-115">**Attribute**</span></span>|<span data-ttu-id="7c825-116">**型**</span><span class="sxs-lookup"><span data-stu-id="7c825-116">**Type**</span></span>|<span data-ttu-id="7c825-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="7c825-117">**Required**</span></span>|<span data-ttu-id="7c825-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="7c825-118">**Description**</span></span>|<span data-ttu-id="7c825-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="7c825-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c825-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="7c825-120">RuleID</span></span>  <br/> |<span data-ttu-id="7c825-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c825-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c825-122">必須</span><span class="sxs-lookup"><span data-stu-id="7c825-122">required</span></span>  <br/> ||<span data-ttu-id="7c825-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="7c825-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c825-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="7c825-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="7c825-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c825-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c825-126">必須</span><span class="sxs-lookup"><span data-stu-id="7c825-126">required</span></span>  <br/> ||<span data-ttu-id="7c825-127">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="7c825-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

