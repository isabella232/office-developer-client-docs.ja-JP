---
title: RuleFilter 要素 (Rule_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: 対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806306"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="0a5fa-103">RuleFilter 要素 (Rule_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0a5fa-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0a5fa-104">対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a5fa-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0a5fa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a5fa-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0a5fa-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="0a5fa-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0a5fa-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0a5fa-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0a5fa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0a5fa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0a5fa-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0a5fa-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="0a5fa-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a5fa-113">定義</span><span class="sxs-lookup"><span data-stu-id="0a5fa-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0a5fa-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0a5fa-114">Elements and attributes</span></span>

<span data-ttu-id="0a5fa-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0a5fa-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0a5fa-116">Parent elements</span></span>

|<span data-ttu-id="0a5fa-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-117">**Element**</span></span>|<span data-ttu-id="0a5fa-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-118">**Type**</span></span>|<span data-ttu-id="0a5fa-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a5fa-120">Rule</span><span class="sxs-lookup"><span data-stu-id="0a5fa-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0a5fa-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="0a5fa-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0a5fa-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0a5fa-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0a5fa-123">Child elements</span></span>

<span data-ttu-id="0a5fa-124">なし。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a5fa-125">属性</span><span class="sxs-lookup"><span data-stu-id="0a5fa-125">Attributes</span></span>

|<span data-ttu-id="0a5fa-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-126">**Attribute**</span></span>|<span data-ttu-id="0a5fa-127">**型**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-127">**Type**</span></span>|<span data-ttu-id="0a5fa-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-128">**Required**</span></span>|<span data-ttu-id="0a5fa-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-129">**Description**</span></span>|<span data-ttu-id="0a5fa-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="0a5fa-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a5fa-131">式</span><span class="sxs-lookup"><span data-stu-id="0a5fa-131">Formula</span></span>  <br/> |<span data-ttu-id="0a5fa-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0a5fa-132">xsd:string</span></span>  <br/> |<span data-ttu-id="0a5fa-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="0a5fa-133">optional</span></span>  <br/> |<span data-ttu-id="0a5fa-134">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="0a5fa-135">Xsd:string の値です。</span><span class="sxs-lookup"><span data-stu-id="0a5fa-135">Values of the xsd:string.</span></span>  <br/> |
   

