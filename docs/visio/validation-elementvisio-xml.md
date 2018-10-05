---
title: 検証要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: 図面に対する図の検証に関する情報を格納します。
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382359"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="62c1c-103">検証要素 ' Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="62c1c-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="62c1c-104">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="62c1c-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62c1c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="62c1c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62c1c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="62c1c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62c1c-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="62c1c-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62c1c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="62c1c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62c1c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="62c1c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62c1c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62c1c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62c1c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="62c1c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62c1c-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="62c1c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62c1c-113">定義</span><span class="sxs-lookup"><span data-stu-id="62c1c-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62c1c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="62c1c-114">Elements and attributes</span></span>

<span data-ttu-id="62c1c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62c1c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62c1c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="62c1c-116">Parent elements</span></span>

<span data-ttu-id="62c1c-117">なし。</span><span class="sxs-lookup"><span data-stu-id="62c1c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62c1c-118">子要素</span><span class="sxs-lookup"><span data-stu-id="62c1c-118">Child elements</span></span>

|<span data-ttu-id="62c1c-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="62c1c-119">**Element**</span></span>|<span data-ttu-id="62c1c-120">**型**</span><span class="sxs-lookup"><span data-stu-id="62c1c-120">**Type**</span></span>|<span data-ttu-id="62c1c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="62c1c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62c1c-122">問題</span><span class="sxs-lookup"><span data-stu-id="62c1c-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62c1c-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="62c1c-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62c1c-124">ドキュメントのすべての**問題**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62c1c-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="62c1c-125">ルールセット</span><span class="sxs-lookup"><span data-stu-id="62c1c-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62c1c-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="62c1c-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62c1c-127">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62c1c-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="62c1c-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="62c1c-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62c1c-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="62c1c-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62c1c-130">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="62c1c-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="62c1c-131">属性</span><span class="sxs-lookup"><span data-stu-id="62c1c-131">Attributes</span></span>

<span data-ttu-id="62c1c-132">なし。</span><span class="sxs-lookup"><span data-stu-id="62c1c-132">None.</span></span>
  

