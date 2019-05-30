---
title: RuleFilter 要素 (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541681"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="dbc53-103">RuleFilter 要素 (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dbc53-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="dbc53-104">ターゲットオブジェクトに検証ルールを適用する必要があるかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="dbc53-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dbc53-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="dbc53-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbc53-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="dbc53-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dbc53-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="dbc53-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dbc53-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dbc53-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dbc53-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dbc53-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dbc53-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="dbc53-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dbc53-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="dbc53-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dbc53-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="dbc53-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dbc53-113">定義</span><span class="sxs-lookup"><span data-stu-id="dbc53-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dbc53-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dbc53-114">Elements and attributes</span></span>

<span data-ttu-id="dbc53-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbc53-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dbc53-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dbc53-116">Parent elements</span></span>

|<span data-ttu-id="dbc53-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dbc53-117">**Element**</span></span>|<span data-ttu-id="dbc53-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dbc53-118">**Type**</span></span>|<span data-ttu-id="dbc53-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dbc53-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dbc53-120">Rule</span><span class="sxs-lookup"><span data-stu-id="dbc53-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dbc53-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="dbc53-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dbc53-122">図の検証ルール セットに含まれる 1 つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="dbc53-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dbc53-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dbc53-123">Child elements</span></span>

<span data-ttu-id="dbc53-124">なし。</span><span class="sxs-lookup"><span data-stu-id="dbc53-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbc53-125">属性</span><span class="sxs-lookup"><span data-stu-id="dbc53-125">Attributes</span></span>

|<span data-ttu-id="dbc53-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="dbc53-126">**Attribute**</span></span>|<span data-ttu-id="dbc53-127">**型**</span><span class="sxs-lookup"><span data-stu-id="dbc53-127">**Type**</span></span>|<span data-ttu-id="dbc53-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="dbc53-128">**Required**</span></span>|<span data-ttu-id="dbc53-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="dbc53-129">**Description**</span></span>|<span data-ttu-id="dbc53-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="dbc53-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dbc53-131">式</span><span class="sxs-lookup"><span data-stu-id="dbc53-131">Formula</span></span>  <br/> |<span data-ttu-id="dbc53-132">xsd: string</span><span class="sxs-lookup"><span data-stu-id="dbc53-132">xsd:string</span></span>  <br/> |<span data-ttu-id="dbc53-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="dbc53-133">optional</span></span>  <br/> |<span data-ttu-id="dbc53-134">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="dbc53-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="dbc53-135">Xsd: string の値。</span><span class="sxs-lookup"><span data-stu-id="dbc53-135">Values of the xsd:string.</span></span>  <br/> |
   

