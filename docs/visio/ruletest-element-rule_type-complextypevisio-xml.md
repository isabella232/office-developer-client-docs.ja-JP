---
title: RuleTest 要素 (Rule_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: 対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。
ms.openlocfilehash: 8fd37040bec383ab61edfa62a09bb766ed8cd3c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384851"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="eb6e4-103">RuleTest 要素 (Rule_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="eb6e4-103">RuleTest element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="eb6e4-104">対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb6e4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="eb6e4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb6e4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="eb6e4-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="eb6e4-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="eb6e4-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="eb6e4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="eb6e4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="eb6e4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="eb6e4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="eb6e4-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="eb6e4-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb6e4-113">定義</span><span class="sxs-lookup"><span data-stu-id="eb6e4-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eb6e4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="eb6e4-114">Elements and attributes</span></span>

<span data-ttu-id="eb6e4-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="eb6e4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="eb6e4-116">Parent elements</span></span>

|<span data-ttu-id="eb6e4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-117">**Element**</span></span>|<span data-ttu-id="eb6e4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-118">**Type**</span></span>|<span data-ttu-id="eb6e4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eb6e4-120">Rule</span><span class="sxs-lookup"><span data-stu-id="eb6e4-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eb6e4-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="eb6e4-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eb6e4-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb6e4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="eb6e4-123">Child elements</span></span>

<span data-ttu-id="eb6e4-124">なし。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb6e4-125">属性</span><span class="sxs-lookup"><span data-stu-id="eb6e4-125">Attributes</span></span>

|<span data-ttu-id="eb6e4-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-126">**Attribute**</span></span>|<span data-ttu-id="eb6e4-127">**型**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-127">**Type**</span></span>|<span data-ttu-id="eb6e4-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-128">**Required**</span></span>|<span data-ttu-id="eb6e4-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-129">**Description**</span></span>|<span data-ttu-id="eb6e4-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="eb6e4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eb6e4-131">式</span><span class="sxs-lookup"><span data-stu-id="eb6e4-131">Formula</span></span>  <br/> |<span data-ttu-id="eb6e4-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eb6e4-132">xsd:string</span></span>  <br/> |<span data-ttu-id="eb6e4-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="eb6e4-133">optional</span></span>  <br/> |<span data-ttu-id="eb6e4-134">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="eb6e4-135">Xsd:string の値です。</span><span class="sxs-lookup"><span data-stu-id="eb6e4-135">Values of the xsd:string.</span></span>  <br/> |
   

