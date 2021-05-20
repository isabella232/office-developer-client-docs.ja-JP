---
title: Validation 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: 図面に対する図の検証に関する情報を格納します。
ms.openlocfilehash: b1b1bcbd70d57d7a7316e91d137cf8c3c3750722
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538551"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="30b74-103">Validation 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="30b74-103">Validation element (Visio XML)</span></span>

<span data-ttu-id="30b74-104">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="30b74-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30b74-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="30b74-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b74-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="30b74-106">**Element type**</span></span> <br/> |[<span data-ttu-id="30b74-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="30b74-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="30b74-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="30b74-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="30b74-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="30b74-109">**Schema file**</span></span> <br/> |<span data-ttu-id="30b74-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="30b74-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="30b74-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="30b74-111">**Document parts**</span></span> <br/> |<span data-ttu-id="30b74-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="30b74-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="30b74-113">定義</span><span class="sxs-lookup"><span data-stu-id="30b74-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="30b74-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="30b74-114">Elements and attributes</span></span>

<span data-ttu-id="30b74-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30b74-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="30b74-116">親要素</span><span class="sxs-lookup"><span data-stu-id="30b74-116">Parent elements</span></span>

<span data-ttu-id="30b74-117">なし。</span><span class="sxs-lookup"><span data-stu-id="30b74-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30b74-118">子要素</span><span class="sxs-lookup"><span data-stu-id="30b74-118">Child elements</span></span>

|<span data-ttu-id="30b74-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="30b74-119">**Element**</span></span>|<span data-ttu-id="30b74-120">**型**</span><span class="sxs-lookup"><span data-stu-id="30b74-120">**Type**</span></span>|<span data-ttu-id="30b74-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="30b74-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30b74-122">Issues</span><span class="sxs-lookup"><span data-stu-id="30b74-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30b74-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="30b74-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30b74-124">ドキュメントのすべての **Issue** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="30b74-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="30b74-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="30b74-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30b74-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="30b74-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30b74-127">ドキュメントの検証ルール セットごとに **RuleSet** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="30b74-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="30b74-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="30b74-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="30b74-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="30b74-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="30b74-130">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="30b74-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="30b74-131">属性</span><span class="sxs-lookup"><span data-stu-id="30b74-131">Attributes</span></span>

<span data-ttu-id="30b74-132">なし。</span><span class="sxs-lookup"><span data-stu-id="30b74-132">None.</span></span>
  

