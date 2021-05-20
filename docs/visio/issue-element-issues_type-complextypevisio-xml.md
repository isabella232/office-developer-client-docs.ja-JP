---
title: Issue 要素 (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: 文書内の1つの検証問題を表します。
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541128"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="65856-103">Issue 要素 (Issues_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="65856-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="65856-104">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="65856-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65856-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="65856-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65856-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="65856-106">**Element type**</span></span> <br/> |[<span data-ttu-id="65856-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="65856-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65856-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65856-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65856-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="65856-109">**Schema file**</span></span> <br/> |<span data-ttu-id="65856-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="65856-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65856-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="65856-111">**Document parts**</span></span> <br/> |<span data-ttu-id="65856-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="65856-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65856-113">定義</span><span class="sxs-lookup"><span data-stu-id="65856-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65856-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="65856-114">Elements and attributes</span></span>

<span data-ttu-id="65856-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65856-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65856-116">親要素</span><span class="sxs-lookup"><span data-stu-id="65856-116">Parent elements</span></span>

|<span data-ttu-id="65856-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="65856-117">**Element**</span></span>|<span data-ttu-id="65856-118">**型**</span><span class="sxs-lookup"><span data-stu-id="65856-118">**Type**</span></span>|<span data-ttu-id="65856-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="65856-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65856-120">Issues</span><span class="sxs-lookup"><span data-stu-id="65856-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65856-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="65856-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65856-122">ドキュメントのすべての **Issue** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="65856-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65856-123">子要素</span><span class="sxs-lookup"><span data-stu-id="65856-123">Child elements</span></span>

|<span data-ttu-id="65856-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="65856-124">**Element**</span></span>|<span data-ttu-id="65856-125">**型**</span><span class="sxs-lookup"><span data-stu-id="65856-125">**Type**</span></span>|<span data-ttu-id="65856-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="65856-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65856-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="65856-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65856-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="65856-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65856-129">親の検証の問題の対象に応じて、親の検証の問題に関連付けられているページ、またはページと図形の両方を指定します。</span><span class="sxs-lookup"><span data-stu-id="65856-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="65856-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="65856-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65856-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="65856-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65856-132">親検証の問題に関連する検証ルールに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="65856-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="65856-133">属性</span><span class="sxs-lookup"><span data-stu-id="65856-133">Attributes</span></span>

|<span data-ttu-id="65856-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="65856-134">**Attribute**</span></span>|<span data-ttu-id="65856-135">**型**</span><span class="sxs-lookup"><span data-stu-id="65856-135">**Type**</span></span>|<span data-ttu-id="65856-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="65856-136">**Required**</span></span>|<span data-ttu-id="65856-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="65856-137">**Description**</span></span>|<span data-ttu-id="65856-138">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="65856-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65856-139">ID</span><span class="sxs-lookup"><span data-stu-id="65856-139">ID</span></span>  <br/> |<span data-ttu-id="65856-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65856-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65856-141">必須</span><span class="sxs-lookup"><span data-stu-id="65856-141">required</span></span>  <br/> |<span data-ttu-id="65856-142">検証の問題の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="65856-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="65856-143">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65856-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65856-144">無視</span><span class="sxs-lookup"><span data-stu-id="65856-144">Ignored</span></span>  <br/> |<span data-ttu-id="65856-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="65856-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65856-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="65856-146">optional</span></span>  <br/> |<span data-ttu-id="65856-147">親検証の問題に関連する検証ルールに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="65856-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="65856-148">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="65856-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

