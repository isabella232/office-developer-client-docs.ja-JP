---
title: Issue 要素 (Issues_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: 文書内の1つの検証問題を表します。
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317907"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="8023f-103">Issue 要素 (Issues_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8023f-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8023f-104">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="8023f-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8023f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8023f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8023f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8023f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8023f-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8023f-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8023f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8023f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8023f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8023f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8023f-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8023f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8023f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8023f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8023f-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="8023f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8023f-113">定義</span><span class="sxs-lookup"><span data-stu-id="8023f-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8023f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8023f-114">Elements and attributes</span></span>

<span data-ttu-id="8023f-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8023f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8023f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8023f-116">Parent elements</span></span>

|<span data-ttu-id="8023f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8023f-117">**Element**</span></span>|<span data-ttu-id="8023f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8023f-118">**Type**</span></span>|<span data-ttu-id="8023f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8023f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8023f-120">Issues</span><span class="sxs-lookup"><span data-stu-id="8023f-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8023f-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="8023f-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8023f-122">文書のすべての**Issue**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="8023f-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8023f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8023f-123">Child elements</span></span>

|<span data-ttu-id="8023f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8023f-124">**Element**</span></span>|<span data-ttu-id="8023f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8023f-125">**Type**</span></span>|<span data-ttu-id="8023f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="8023f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8023f-127">"発信先"</span><span class="sxs-lookup"><span data-stu-id="8023f-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8023f-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="8023f-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8023f-129">親の検証問題のターゲットに応じて、親の検証の問題に関連付けられているページまたはページと図形の両方を指定します。</span><span class="sxs-lookup"><span data-stu-id="8023f-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="8023f-130">ruleinfo</span><span class="sxs-lookup"><span data-stu-id="8023f-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8023f-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8023f-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8023f-132">親の検証問題に関連する検証ルールについての情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8023f-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8023f-133">属性</span><span class="sxs-lookup"><span data-stu-id="8023f-133">Attributes</span></span>

|<span data-ttu-id="8023f-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="8023f-134">**Attribute**</span></span>|<span data-ttu-id="8023f-135">**型**</span><span class="sxs-lookup"><span data-stu-id="8023f-135">**Type**</span></span>|<span data-ttu-id="8023f-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="8023f-136">**Required**</span></span>|<span data-ttu-id="8023f-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="8023f-137">**Description**</span></span>|<span data-ttu-id="8023f-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8023f-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8023f-139">ID</span><span class="sxs-lookup"><span data-stu-id="8023f-139">ID</span></span>  <br/> |<span data-ttu-id="8023f-140">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="8023f-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8023f-141">必須</span><span class="sxs-lookup"><span data-stu-id="8023f-141">required</span></span>  <br/> |<span data-ttu-id="8023f-142">検証の問題の一意識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8023f-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="8023f-143">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="8023f-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8023f-144">Ignored</span><span class="sxs-lookup"><span data-stu-id="8023f-144">Ignored</span></span>  <br/> |<span data-ttu-id="8023f-145">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="8023f-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8023f-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="8023f-146">optional</span></span>  <br/> |<span data-ttu-id="8023f-147">親の検証問題に関連する検証ルールについての情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8023f-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="8023f-148">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="8023f-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

