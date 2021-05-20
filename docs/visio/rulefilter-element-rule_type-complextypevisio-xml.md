---
title: RuleFilter 要素 (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: 検証ルールをターゲット オブジェクトに適用するかどうかを決定する論理式を指定します。
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541681"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a><span data-ttu-id="d2e75-103">RuleFilter 要素 (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d2e75-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d2e75-104">検証ルールをターゲット オブジェクトに適用するかどうかを決定する論理式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2e75-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2e75-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="d2e75-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2e75-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d2e75-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d2e75-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="d2e75-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d2e75-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d2e75-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d2e75-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d2e75-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d2e75-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d2e75-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d2e75-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="d2e75-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d2e75-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="d2e75-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d2e75-113">定義</span><span class="sxs-lookup"><span data-stu-id="d2e75-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d2e75-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d2e75-114">Elements and attributes</span></span>

<span data-ttu-id="d2e75-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2e75-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d2e75-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d2e75-116">Parent elements</span></span>

|<span data-ttu-id="d2e75-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d2e75-117">**Element**</span></span>|<span data-ttu-id="d2e75-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d2e75-118">**Type**</span></span>|<span data-ttu-id="d2e75-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2e75-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d2e75-120">Rule</span><span class="sxs-lookup"><span data-stu-id="d2e75-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d2e75-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="d2e75-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d2e75-122">図の検証ルールセット内の1つの検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="d2e75-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d2e75-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d2e75-123">Child elements</span></span>

<span data-ttu-id="d2e75-124">なし。</span><span class="sxs-lookup"><span data-stu-id="d2e75-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2e75-125">属性</span><span class="sxs-lookup"><span data-stu-id="d2e75-125">Attributes</span></span>

|<span data-ttu-id="d2e75-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="d2e75-126">**Attribute**</span></span>|<span data-ttu-id="d2e75-127">**型**</span><span class="sxs-lookup"><span data-stu-id="d2e75-127">**Type**</span></span>|<span data-ttu-id="d2e75-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="d2e75-128">**Required**</span></span>|<span data-ttu-id="d2e75-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2e75-129">**Description**</span></span>|<span data-ttu-id="d2e75-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d2e75-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d2e75-131">式</span><span class="sxs-lookup"><span data-stu-id="d2e75-131">Formula</span></span>  <br/> |<span data-ttu-id="d2e75-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d2e75-132">xsd:string</span></span>  <br/> |<span data-ttu-id="d2e75-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="d2e75-133">optional</span></span>  <br/> |<span data-ttu-id="d2e75-134">要素の数式を表します。</span><span class="sxs-lookup"><span data-stu-id="d2e75-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="d2e75-135">xsd:string の値。</span><span class="sxs-lookup"><span data-stu-id="d2e75-135">Values of the xsd:string.</span></span>  <br/> |
   

