---
title: ルールセットの要素 (Validation_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: 各入力規則に違反、文書内のルール セットの要素が含まれています。
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399642"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="cdfa0-103">ルールセットの要素 (Validation_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="cdfa0-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cdfa0-104">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdfa0-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cdfa0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="cdfa0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdfa0-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cdfa0-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="cdfa0-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cdfa0-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cdfa0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cdfa0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cdfa0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cdfa0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cdfa0-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="cdfa0-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cdfa0-113">定義</span><span class="sxs-lookup"><span data-stu-id="cdfa0-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cdfa0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="cdfa0-114">Elements and attributes</span></span>

<span data-ttu-id="cdfa0-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cdfa0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cdfa0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="cdfa0-116">Parent elements</span></span>

|<span data-ttu-id="cdfa0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-117">**Element**</span></span>|<span data-ttu-id="cdfa0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-118">**Type**</span></span>|<span data-ttu-id="cdfa0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cdfa0-120">検証</span><span class="sxs-lookup"><span data-stu-id="cdfa0-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="cdfa0-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="cdfa0-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cdfa0-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="cdfa0-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cdfa0-123">子要素</span><span class="sxs-lookup"><span data-stu-id="cdfa0-123">Child elements</span></span>

|<span data-ttu-id="cdfa0-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-124">**Element**</span></span>|<span data-ttu-id="cdfa0-125">**型**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-125">**Type**</span></span>|<span data-ttu-id="cdfa0-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="cdfa0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cdfa0-127">ルールセット</span><span class="sxs-lookup"><span data-stu-id="cdfa0-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cdfa0-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="cdfa0-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cdfa0-129">ダイアグラムの検証ルールの 1 つのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="cdfa0-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cdfa0-130">属性</span><span class="sxs-lookup"><span data-stu-id="cdfa0-130">Attributes</span></span>

<span data-ttu-id="cdfa0-131">なし。</span><span class="sxs-lookup"><span data-stu-id="cdfa0-131">None.</span></span>
  

