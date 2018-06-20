---
title: RuleTest 要素 (Rule_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: 対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。
ms.openlocfilehash: 25569530af5bc6f4b00e8600d1e25d968a01f246
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806334"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="43069-103">RuleTest 要素 (Rule_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="43069-103">RuleTest element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="43069-104">対象のオブジェクトが、検証規則を満たすかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="43069-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43069-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="43069-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43069-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="43069-106">**Element type**</span></span> <br/> |[<span data-ttu-id="43069-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="43069-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="43069-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="43069-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="43069-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="43069-109">**Schema file**</span></span> <br/> |<span data-ttu-id="43069-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="43069-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="43069-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="43069-111">**Document parts**</span></span> <br/> |<span data-ttu-id="43069-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="43069-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="43069-113">定義</span><span class="sxs-lookup"><span data-stu-id="43069-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="43069-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="43069-114">Elements and attributes</span></span>

<span data-ttu-id="43069-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43069-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="43069-116">親要素</span><span class="sxs-lookup"><span data-stu-id="43069-116">Parent elements</span></span>

|<span data-ttu-id="43069-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="43069-117">**Element**</span></span>|<span data-ttu-id="43069-118">**型**</span><span class="sxs-lookup"><span data-stu-id="43069-118">**Type**</span></span>|<span data-ttu-id="43069-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="43069-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="43069-120">Rule</span><span class="sxs-lookup"><span data-stu-id="43069-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="43069-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="43069-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="43069-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="43069-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43069-123">子要素</span><span class="sxs-lookup"><span data-stu-id="43069-123">Child elements</span></span>

<span data-ttu-id="43069-124">なし。</span><span class="sxs-lookup"><span data-stu-id="43069-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43069-125">属性</span><span class="sxs-lookup"><span data-stu-id="43069-125">Attributes</span></span>

|<span data-ttu-id="43069-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="43069-126">**Attribute**</span></span>|<span data-ttu-id="43069-127">**型**</span><span class="sxs-lookup"><span data-stu-id="43069-127">**Type**</span></span>|<span data-ttu-id="43069-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="43069-128">**Required**</span></span>|<span data-ttu-id="43069-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="43069-129">**Description**</span></span>|<span data-ttu-id="43069-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="43069-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="43069-131">式</span><span class="sxs-lookup"><span data-stu-id="43069-131">Formula</span></span>  <br/> |<span data-ttu-id="43069-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="43069-132">xsd:string</span></span>  <br/> |<span data-ttu-id="43069-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="43069-133">optional</span></span>  <br/> |<span data-ttu-id="43069-134">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="43069-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="43069-135">Xsd:string の値です。</span><span class="sxs-lookup"><span data-stu-id="43069-135">Values of the xsd:string.</span></span>  <br/> |
   

