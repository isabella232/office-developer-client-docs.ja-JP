---
title: RuleSets 要素 (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: ドキュメントの検証ルール セットごとに RuleSet 要素が含まれます。
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541576"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="a3daa-103">RuleSets 要素 (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a3daa-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a3daa-104">ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3daa-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a3daa-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a3daa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3daa-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a3daa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a3daa-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="a3daa-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3daa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a3daa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3daa-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a3daa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a3daa-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a3daa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3daa-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a3daa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a3daa-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="a3daa-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3daa-113">定義</span><span class="sxs-lookup"><span data-stu-id="a3daa-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3daa-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a3daa-114">Elements and attributes</span></span>

<span data-ttu-id="a3daa-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3daa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3daa-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a3daa-116">Parent elements</span></span>

|<span data-ttu-id="a3daa-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a3daa-117">**Element**</span></span>|<span data-ttu-id="a3daa-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a3daa-118">**Type**</span></span>|<span data-ttu-id="a3daa-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3daa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3daa-120">Validation</span><span class="sxs-lookup"><span data-stu-id="a3daa-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="a3daa-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a3daa-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3daa-122">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="a3daa-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3daa-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a3daa-123">Child elements</span></span>

|<span data-ttu-id="a3daa-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3daa-124">**Element**</span></span>|<span data-ttu-id="a3daa-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a3daa-125">**Type**</span></span>|<span data-ttu-id="a3daa-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3daa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3daa-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="a3daa-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3daa-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="a3daa-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3daa-129">図の検証ルール セットの 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="a3daa-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a3daa-130">属性</span><span class="sxs-lookup"><span data-stu-id="a3daa-130">Attributes</span></span>

<span data-ttu-id="a3daa-131">なし。</span><span class="sxs-lookup"><span data-stu-id="a3daa-131">None.</span></span>
  

