---
title: ruletest 要素 (Rule_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。
ms.openlocfilehash: 8fd37040bec383ab61edfa62a09bb766ed8cd3c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319083"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="ed249-103">ruletest 要素 (Rule_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ed249-103">RuleTest element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ed249-104">ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed249-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed249-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ed249-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed249-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ed249-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ed249-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="ed249-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ed249-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ed249-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ed249-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ed249-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ed249-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="ed249-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ed249-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ed249-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ed249-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="ed249-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ed249-113">定義</span><span class="sxs-lookup"><span data-stu-id="ed249-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ed249-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ed249-114">Elements and attributes</span></span>

<span data-ttu-id="ed249-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed249-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ed249-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ed249-116">Parent elements</span></span>

|<span data-ttu-id="ed249-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ed249-117">**Element**</span></span>|<span data-ttu-id="ed249-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ed249-118">**Type**</span></span>|<span data-ttu-id="ed249-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ed249-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ed249-120">Rule</span><span class="sxs-lookup"><span data-stu-id="ed249-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ed249-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="ed249-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ed249-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="ed249-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed249-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ed249-123">Child elements</span></span>

<span data-ttu-id="ed249-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ed249-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed249-125">属性</span><span class="sxs-lookup"><span data-stu-id="ed249-125">Attributes</span></span>

|<span data-ttu-id="ed249-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ed249-126">**Attribute**</span></span>|<span data-ttu-id="ed249-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ed249-127">**Type**</span></span>|<span data-ttu-id="ed249-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ed249-128">**Required**</span></span>|<span data-ttu-id="ed249-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ed249-129">**Description**</span></span>|<span data-ttu-id="ed249-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ed249-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed249-131">Formula</span><span class="sxs-lookup"><span data-stu-id="ed249-131">Formula</span></span>  <br/> |<span data-ttu-id="ed249-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="ed249-132">xsd:string</span></span>  <br/> |<span data-ttu-id="ed249-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="ed249-133">optional</span></span>  <br/> |<span data-ttu-id="ed249-134">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="ed249-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="ed249-135">xsd: string の値。</span><span class="sxs-lookup"><span data-stu-id="ed249-135">Values of the xsd:string.</span></span>  <br/> |
   

