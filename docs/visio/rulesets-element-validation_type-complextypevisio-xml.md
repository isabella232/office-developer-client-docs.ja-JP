---
title: ルールセット要素 (Validation_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: 文書内の各入力規則のルールセット要素が含まれています。
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319048"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="9fc17-103">ルールセット要素 (Validation_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9fc17-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9fc17-104">文書内\*\*\*\* の各入力規則のルールセット要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fc17-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9fc17-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9fc17-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fc17-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9fc17-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9fc17-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="9fc17-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9fc17-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9fc17-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9fc17-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9fc17-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9fc17-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9fc17-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9fc17-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9fc17-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9fc17-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="9fc17-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9fc17-113">定義</span><span class="sxs-lookup"><span data-stu-id="9fc17-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9fc17-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9fc17-114">Elements and attributes</span></span>

<span data-ttu-id="9fc17-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fc17-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9fc17-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9fc17-116">Parent elements</span></span>

|<span data-ttu-id="9fc17-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="9fc17-117">**Element**</span></span>|<span data-ttu-id="9fc17-118">**型**</span><span class="sxs-lookup"><span data-stu-id="9fc17-118">**Type**</span></span>|<span data-ttu-id="9fc17-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fc17-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fc17-120">Validation</span><span class="sxs-lookup"><span data-stu-id="9fc17-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="9fc17-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="9fc17-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fc17-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="9fc17-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9fc17-123">子要素</span><span class="sxs-lookup"><span data-stu-id="9fc17-123">Child elements</span></span>

|<span data-ttu-id="9fc17-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fc17-124">**Element**</span></span>|<span data-ttu-id="9fc17-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9fc17-125">**Type**</span></span>|<span data-ttu-id="9fc17-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fc17-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9fc17-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="9fc17-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9fc17-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9fc17-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9fc17-129">1組のダイアグラム検証ルールを表します。</span><span class="sxs-lookup"><span data-stu-id="9fc17-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9fc17-130">属性</span><span class="sxs-lookup"><span data-stu-id="9fc17-130">Attributes</span></span>

<span data-ttu-id="9fc17-131">なし。</span><span class="sxs-lookup"><span data-stu-id="9fc17-131">None.</span></span>
  

