---
title: 検証要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: 図面に対する図の検証に関する情報を格納します。
ms.openlocfilehash: f4a7c0893baebb09dccd743c3006a5512dec533d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806744"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="40b48-103">検証要素 ' Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="40b48-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="40b48-104">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="40b48-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40b48-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="40b48-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40b48-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="40b48-106">**Element type**</span></span> <br/> |[<span data-ttu-id="40b48-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="40b48-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="40b48-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="40b48-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="40b48-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="40b48-109">**Schema file**</span></span> <br/> |<span data-ttu-id="40b48-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="40b48-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="40b48-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="40b48-111">**Document parts**</span></span> <br/> |<span data-ttu-id="40b48-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="40b48-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40b48-113">定義</span><span class="sxs-lookup"><span data-stu-id="40b48-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="40b48-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="40b48-114">Elements and attributes</span></span>

<span data-ttu-id="40b48-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="40b48-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="40b48-116">親要素</span><span class="sxs-lookup"><span data-stu-id="40b48-116">Parent elements</span></span>

<span data-ttu-id="40b48-117">なし。</span><span class="sxs-lookup"><span data-stu-id="40b48-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40b48-118">子要素</span><span class="sxs-lookup"><span data-stu-id="40b48-118">Child elements</span></span>

|<span data-ttu-id="40b48-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="40b48-119">**Element**</span></span>|<span data-ttu-id="40b48-120">**型**</span><span class="sxs-lookup"><span data-stu-id="40b48-120">**Type**</span></span>|<span data-ttu-id="40b48-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="40b48-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40b48-122">問題</span><span class="sxs-lookup"><span data-stu-id="40b48-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40b48-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="40b48-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40b48-124">ドキュメントのすべての**問題**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="40b48-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="40b48-125">ルールセット</span><span class="sxs-lookup"><span data-stu-id="40b48-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40b48-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="40b48-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40b48-127">各入力規則に違反、文書内の**ルール セット**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="40b48-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="40b48-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="40b48-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="40b48-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="40b48-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="40b48-130">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="40b48-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="40b48-131">属性</span><span class="sxs-lookup"><span data-stu-id="40b48-131">Attributes</span></span>

<span data-ttu-id="40b48-132">なし。</span><span class="sxs-lookup"><span data-stu-id="40b48-132">None.</span></span>
  

