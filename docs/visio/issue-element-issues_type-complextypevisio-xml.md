---
title: 問題の要素 (Issues_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: 文書の 1 つの検証の問題を表します。
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805633"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="17222-103">問題の要素 (Issues_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="17222-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="17222-104">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="17222-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17222-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="17222-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17222-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="17222-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17222-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="17222-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17222-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="17222-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17222-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="17222-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17222-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17222-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17222-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="17222-111">**Document parts**</span></span> <br/> |<span data-ttu-id="17222-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="17222-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17222-113">定義</span><span class="sxs-lookup"><span data-stu-id="17222-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17222-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="17222-114">Elements and attributes</span></span>

<span data-ttu-id="17222-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17222-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17222-116">親要素</span><span class="sxs-lookup"><span data-stu-id="17222-116">Parent elements</span></span>

|<span data-ttu-id="17222-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="17222-117">**Element**</span></span>|<span data-ttu-id="17222-118">**型**</span><span class="sxs-lookup"><span data-stu-id="17222-118">**Type**</span></span>|<span data-ttu-id="17222-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="17222-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17222-120">問題</span><span class="sxs-lookup"><span data-stu-id="17222-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17222-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="17222-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17222-122">ドキュメントのすべての**問題**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="17222-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17222-123">子要素</span><span class="sxs-lookup"><span data-stu-id="17222-123">Child elements</span></span>

|<span data-ttu-id="17222-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="17222-124">**Element**</span></span>|<span data-ttu-id="17222-125">**型**</span><span class="sxs-lookup"><span data-stu-id="17222-125">**Type**</span></span>|<span data-ttu-id="17222-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="17222-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17222-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="17222-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17222-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="17222-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17222-129">親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。</span><span class="sxs-lookup"><span data-stu-id="17222-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="17222-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="17222-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17222-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="17222-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17222-132">親の検証の問題に関連する入力規則に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="17222-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="17222-133">属性</span><span class="sxs-lookup"><span data-stu-id="17222-133">Attributes</span></span>

|<span data-ttu-id="17222-134">**属性**</span><span class="sxs-lookup"><span data-stu-id="17222-134">**Attribute**</span></span>|<span data-ttu-id="17222-135">**型**</span><span class="sxs-lookup"><span data-stu-id="17222-135">**Type**</span></span>|<span data-ttu-id="17222-136">**必須**</span><span class="sxs-lookup"><span data-stu-id="17222-136">**Required**</span></span>|<span data-ttu-id="17222-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="17222-137">**Description**</span></span>|<span data-ttu-id="17222-138">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="17222-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17222-139">ID</span><span class="sxs-lookup"><span data-stu-id="17222-139">ID</span></span>  <br/> |<span data-ttu-id="17222-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="17222-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="17222-141">必須</span><span class="sxs-lookup"><span data-stu-id="17222-141">required</span></span>  <br/> |<span data-ttu-id="17222-142">検証の問題の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="17222-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="17222-143">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="17222-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="17222-144">無視</span><span class="sxs-lookup"><span data-stu-id="17222-144">Ignored</span></span>  <br/> |<span data-ttu-id="17222-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="17222-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="17222-146">省略可能</span><span class="sxs-lookup"><span data-stu-id="17222-146">optional</span></span>  <br/> |<span data-ttu-id="17222-147">親の検証の問題に関連する入力規則に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="17222-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="17222-148">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="17222-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

