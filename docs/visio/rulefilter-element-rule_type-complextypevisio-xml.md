---
title: RuleFilter 要素 (Rule_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: 対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。
ms.openlocfilehash: 8d4167fbb8dde54c55e49debb77fe307ecab6771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396730"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="9dffe-103">RuleFilter 要素 (Rule_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="9dffe-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9dffe-104">対象オブジェクトに規則を適用するかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9dffe-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dffe-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9dffe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dffe-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9dffe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9dffe-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="9dffe-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9dffe-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9dffe-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9dffe-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9dffe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9dffe-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9dffe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9dffe-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9dffe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9dffe-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="9dffe-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9dffe-113">定義</span><span class="sxs-lookup"><span data-stu-id="9dffe-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9dffe-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9dffe-114">Elements and attributes</span></span>

<span data-ttu-id="9dffe-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9dffe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9dffe-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9dffe-116">Parent elements</span></span>

|<span data-ttu-id="9dffe-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9dffe-117">**Element**</span></span>|<span data-ttu-id="9dffe-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9dffe-118">**Type**</span></span>|<span data-ttu-id="9dffe-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9dffe-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9dffe-120">Rule</span><span class="sxs-lookup"><span data-stu-id="9dffe-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9dffe-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9dffe-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9dffe-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="9dffe-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9dffe-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9dffe-123">Child elements</span></span>

<span data-ttu-id="9dffe-124">なし。</span><span class="sxs-lookup"><span data-stu-id="9dffe-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dffe-125">属性</span><span class="sxs-lookup"><span data-stu-id="9dffe-125">Attributes</span></span>

|<span data-ttu-id="9dffe-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="9dffe-126">**Attribute**</span></span>|<span data-ttu-id="9dffe-127">**型**</span><span class="sxs-lookup"><span data-stu-id="9dffe-127">**Type**</span></span>|<span data-ttu-id="9dffe-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="9dffe-128">**Required**</span></span>|<span data-ttu-id="9dffe-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="9dffe-129">**Description**</span></span>|<span data-ttu-id="9dffe-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9dffe-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9dffe-131">式</span><span class="sxs-lookup"><span data-stu-id="9dffe-131">Formula</span></span>  <br/> |<span data-ttu-id="9dffe-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9dffe-132">xsd:string</span></span>  <br/> |<span data-ttu-id="9dffe-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="9dffe-133">optional</span></span>  <br/> |<span data-ttu-id="9dffe-134">要素の式を表します。</span><span class="sxs-lookup"><span data-stu-id="9dffe-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="9dffe-135">Xsd:string の値です。</span><span class="sxs-lookup"><span data-stu-id="9dffe-135">Values of the xsd:string.</span></span>  <br/> |
   

