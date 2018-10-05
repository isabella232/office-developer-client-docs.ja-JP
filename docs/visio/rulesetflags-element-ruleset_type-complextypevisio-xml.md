---
title: RuleSetFlags 要素 (RuleSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: ルール ・ セットのプロパティを指定します。
ms.openlocfilehash: 4a8ba44e2c77281f3d68fb3f5a7a2c58884ce66b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400101"
---
# <a name="rulesetflags-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="abbfc-103">RuleSetFlags 要素 (RuleSet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="abbfc-103">RuleSetFlags element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="abbfc-104">ルール ・ セットのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="abbfc-104">Specifies rule-set properties.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abbfc-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="abbfc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abbfc-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="abbfc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="abbfc-107">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="abbfc-107">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="abbfc-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="abbfc-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="abbfc-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="abbfc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="abbfc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="abbfc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="abbfc-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="abbfc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="abbfc-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="abbfc-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="abbfc-113">定義</span><span class="sxs-lookup"><span data-stu-id="abbfc-113">Definition</span></span>

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="abbfc-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="abbfc-114">Elements and attributes</span></span>

<span data-ttu-id="abbfc-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="abbfc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="abbfc-116">親要素</span><span class="sxs-lookup"><span data-stu-id="abbfc-116">Parent elements</span></span>

|<span data-ttu-id="abbfc-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="abbfc-117">**Element**</span></span>|<span data-ttu-id="abbfc-118">**型**</span><span class="sxs-lookup"><span data-stu-id="abbfc-118">**Type**</span></span>|<span data-ttu-id="abbfc-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="abbfc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="abbfc-120">ルールセット</span><span class="sxs-lookup"><span data-stu-id="abbfc-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="abbfc-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="abbfc-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="abbfc-122">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="abbfc-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abbfc-123">子要素</span><span class="sxs-lookup"><span data-stu-id="abbfc-123">Child elements</span></span>

<span data-ttu-id="abbfc-124">なし。</span><span class="sxs-lookup"><span data-stu-id="abbfc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abbfc-125">属性</span><span class="sxs-lookup"><span data-stu-id="abbfc-125">Attributes</span></span>

|<span data-ttu-id="abbfc-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="abbfc-126">**Attribute**</span></span>|<span data-ttu-id="abbfc-127">**型**</span><span class="sxs-lookup"><span data-stu-id="abbfc-127">**Type**</span></span>|<span data-ttu-id="abbfc-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="abbfc-128">**Required**</span></span>|<span data-ttu-id="abbfc-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="abbfc-129">**Description**</span></span>|<span data-ttu-id="abbfc-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="abbfc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="abbfc-131">非表示</span><span class="sxs-lookup"><span data-stu-id="abbfc-131">Hidden</span></span>  <br/> |<span data-ttu-id="abbfc-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="abbfc-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="abbfc-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="abbfc-133">optional</span></span>  <br/> |<span data-ttu-id="abbfc-134">チェック] ボックスの一覧を規則でルール セットが表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="abbfc-134">Specifies whether the rule set appears in the Rules to Check list.</span></span>  <br/> |<span data-ttu-id="abbfc-135">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="abbfc-135">Values of the xsd:boolean type.</span></span>  <br/> |
   

