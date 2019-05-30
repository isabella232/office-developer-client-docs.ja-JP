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
# <a name="validation-element-visio-xml"></a><span data-ttu-id="78df7-103">Validation 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="78df7-103">Validation element (Visio XML)</span></span>

<span data-ttu-id="78df7-104">図面に対する図の検証に関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="78df7-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78df7-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="78df7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78df7-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="78df7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="78df7-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="78df7-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="78df7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="78df7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="78df7-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="78df7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="78df7-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="78df7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="78df7-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="78df7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="78df7-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="78df7-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78df7-113">定義</span><span class="sxs-lookup"><span data-stu-id="78df7-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78df7-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="78df7-114">Elements and attributes</span></span>

<span data-ttu-id="78df7-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="78df7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="78df7-116">親要素</span><span class="sxs-lookup"><span data-stu-id="78df7-116">Parent elements</span></span>

<span data-ttu-id="78df7-117">なし。</span><span class="sxs-lookup"><span data-stu-id="78df7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78df7-118">子要素</span><span class="sxs-lookup"><span data-stu-id="78df7-118">Child elements</span></span>

|<span data-ttu-id="78df7-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="78df7-119">**Element**</span></span>|<span data-ttu-id="78df7-120">**型**</span><span class="sxs-lookup"><span data-stu-id="78df7-120">**Type**</span></span>|<span data-ttu-id="78df7-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="78df7-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78df7-122">Issues</span><span class="sxs-lookup"><span data-stu-id="78df7-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78df7-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="78df7-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78df7-124">文書のすべての**Issue**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="78df7-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="78df7-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="78df7-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78df7-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="78df7-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78df7-127">文書内\*\*\*\* の各入力規則のルールセット要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="78df7-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="78df7-128">ValidationProperties プロパティ</span><span class="sxs-lookup"><span data-stu-id="78df7-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78df7-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="78df7-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78df7-130">ドキュメントの検証に関連するプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="78df7-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="78df7-131">属性</span><span class="sxs-lookup"><span data-stu-id="78df7-131">Attributes</span></span>

<span data-ttu-id="78df7-132">なし。</span><span class="sxs-lookup"><span data-stu-id="78df7-132">None.</span></span>
  

