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
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="025bc-102">RuleInfo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="025bc-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="025bc-103">型情報</span><span class="sxs-lookup"><span data-stu-id="025bc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="025bc-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="025bc-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="025bc-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="025bc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="025bc-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="025bc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="025bc-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="025bc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="025bc-108">None</span><span class="sxs-lookup"><span data-stu-id="025bc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="025bc-109">定義</span><span class="sxs-lookup"><span data-stu-id="025bc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="025bc-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="025bc-110">Elements and attributes</span></span>

<span data-ttu-id="025bc-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="025bc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="025bc-112">子要素</span><span class="sxs-lookup"><span data-stu-id="025bc-112">Child elements</span></span>

<span data-ttu-id="025bc-113">なし。</span><span class="sxs-lookup"><span data-stu-id="025bc-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="025bc-114">属性</span><span class="sxs-lookup"><span data-stu-id="025bc-114">Attributes</span></span>

|<span data-ttu-id="025bc-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="025bc-115">**Attribute**</span></span>|<span data-ttu-id="025bc-116">**型**</span><span class="sxs-lookup"><span data-stu-id="025bc-116">**Type**</span></span>|<span data-ttu-id="025bc-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="025bc-117">**Required**</span></span>|<span data-ttu-id="025bc-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="025bc-118">**Description**</span></span>|<span data-ttu-id="025bc-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="025bc-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="025bc-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="025bc-120">RuleID</span></span>  <br/> |<span data-ttu-id="025bc-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="025bc-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="025bc-122">必須</span><span class="sxs-lookup"><span data-stu-id="025bc-122">required</span></span>  <br/> ||<span data-ttu-id="025bc-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="025bc-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="025bc-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="025bc-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="025bc-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="025bc-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="025bc-126">必須</span><span class="sxs-lookup"><span data-stu-id="025bc-126">required</span></span>  <br/> ||<span data-ttu-id="025bc-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="025bc-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

