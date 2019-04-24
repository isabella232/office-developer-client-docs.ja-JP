---
title: rulefilter 要素 (Rule_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349386"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="d8cf4-103">rulefilter 要素 (Rule_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d8cf4-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d8cf4-104">ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8cf4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d8cf4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8cf4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d8cf4-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="d8cf4-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d8cf4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d8cf4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d8cf4-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d8cf4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d8cf4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d8cf4-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="d8cf4-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8cf4-113">定義</span><span class="sxs-lookup"><span data-stu-id="d8cf4-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8cf4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d8cf4-114">Elements and attributes</span></span>

<span data-ttu-id="d8cf4-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d8cf4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d8cf4-116">Parent elements</span></span>

|<span data-ttu-id="d8cf4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-117">**Element**</span></span>|<span data-ttu-id="d8cf4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-118">**Type**</span></span>|<span data-ttu-id="d8cf4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8cf4-120">Rule</span><span class="sxs-lookup"><span data-stu-id="d8cf4-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8cf4-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="d8cf4-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8cf4-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8cf4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d8cf4-123">Child elements</span></span>

<span data-ttu-id="d8cf4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8cf4-125">属性</span><span class="sxs-lookup"><span data-stu-id="d8cf4-125">Attributes</span></span>

|<span data-ttu-id="d8cf4-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-126">**Attribute**</span></span>|<span data-ttu-id="d8cf4-127">**型**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-127">**Type**</span></span>|<span data-ttu-id="d8cf4-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-128">**Required**</span></span>|<span data-ttu-id="d8cf4-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-129">**Description**</span></span>|<span data-ttu-id="d8cf4-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d8cf4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8cf4-131">Formula</span><span class="sxs-lookup"><span data-stu-id="d8cf4-131">Formula</span></span>  <br/> |<span data-ttu-id="d8cf4-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="d8cf4-132">xsd:string</span></span>  <br/> |<span data-ttu-id="d8cf4-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="d8cf4-133">optional</span></span>  <br/> |<span data-ttu-id="d8cf4-134">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="d8cf4-135">xsd: string の値。</span><span class="sxs-lookup"><span data-stu-id="d8cf4-135">Values of the xsd:string.</span></span>  <br/> |
   

