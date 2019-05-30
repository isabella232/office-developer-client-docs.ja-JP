---
title: RuleTest 要素 (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。
ms.openlocfilehash: bb1f0cf9b3f712903f6e45d6d09f96607089f920
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541520"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="898e2-103">RuleTest 要素 (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="898e2-103">RuleTest element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="898e2-104">ターゲットオブジェクトが検証規則を満たしているかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="898e2-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="898e2-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="898e2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="898e2-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="898e2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="898e2-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="898e2-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="898e2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="898e2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="898e2-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="898e2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="898e2-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="898e2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="898e2-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="898e2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="898e2-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="898e2-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="898e2-113">定義</span><span class="sxs-lookup"><span data-stu-id="898e2-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="898e2-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="898e2-114">Elements and attributes</span></span>

<span data-ttu-id="898e2-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="898e2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="898e2-116">親要素</span><span class="sxs-lookup"><span data-stu-id="898e2-116">Parent elements</span></span>

|<span data-ttu-id="898e2-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="898e2-117">**Element**</span></span>|<span data-ttu-id="898e2-118">**型**</span><span class="sxs-lookup"><span data-stu-id="898e2-118">**Type**</span></span>|<span data-ttu-id="898e2-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="898e2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="898e2-120">Rule</span><span class="sxs-lookup"><span data-stu-id="898e2-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="898e2-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="898e2-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="898e2-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="898e2-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="898e2-123">子要素</span><span class="sxs-lookup"><span data-stu-id="898e2-123">Child elements</span></span>

<span data-ttu-id="898e2-124">なし。</span><span class="sxs-lookup"><span data-stu-id="898e2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="898e2-125">属性</span><span class="sxs-lookup"><span data-stu-id="898e2-125">Attributes</span></span>

|<span data-ttu-id="898e2-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="898e2-126">**Attribute**</span></span>|<span data-ttu-id="898e2-127">**型**</span><span class="sxs-lookup"><span data-stu-id="898e2-127">**Type**</span></span>|<span data-ttu-id="898e2-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="898e2-128">**Required**</span></span>|<span data-ttu-id="898e2-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="898e2-129">**Description**</span></span>|<span data-ttu-id="898e2-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="898e2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="898e2-131">式</span><span class="sxs-lookup"><span data-stu-id="898e2-131">Formula</span></span>  <br/> |<span data-ttu-id="898e2-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="898e2-132">xsd:string</span></span>  <br/> |<span data-ttu-id="898e2-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="898e2-133">optional</span></span>  <br/> |<span data-ttu-id="898e2-134">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="898e2-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="898e2-135">Xsd: string の値。</span><span class="sxs-lookup"><span data-stu-id="898e2-135">Values of the xsd:string.</span></span>  <br/> |
   

