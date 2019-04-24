---
title: ruleinfo 要素 (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親の検証問題に関連する検証ルールについての情報を指定します。
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356988"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="8761d-103">ruleinfo 要素 (Issue_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="8761d-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8761d-104">親の検証問題に関連する検証ルールについての情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8761d-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8761d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="8761d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8761d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8761d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8761d-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="8761d-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8761d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8761d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8761d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8761d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8761d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="8761d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8761d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="8761d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8761d-112">検証 xml</span><span class="sxs-lookup"><span data-stu-id="8761d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8761d-113">定義</span><span class="sxs-lookup"><span data-stu-id="8761d-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8761d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8761d-114">Elements and attributes</span></span>

<span data-ttu-id="8761d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8761d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8761d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8761d-116">Parent elements</span></span>

|<span data-ttu-id="8761d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8761d-117">**Element**</span></span>|<span data-ttu-id="8761d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8761d-118">**Type**</span></span>|<span data-ttu-id="8761d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8761d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8761d-120">問題</span><span class="sxs-lookup"><span data-stu-id="8761d-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8761d-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="8761d-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8761d-122">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="8761d-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8761d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8761d-123">Child elements</span></span>

<span data-ttu-id="8761d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="8761d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8761d-125">属性</span><span class="sxs-lookup"><span data-stu-id="8761d-125">Attributes</span></span>

|<span data-ttu-id="8761d-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="8761d-126">**Attribute**</span></span>|<span data-ttu-id="8761d-127">**型**</span><span class="sxs-lookup"><span data-stu-id="8761d-127">**Type**</span></span>|<span data-ttu-id="8761d-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="8761d-128">**Required**</span></span>|<span data-ttu-id="8761d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="8761d-129">**Description**</span></span>|<span data-ttu-id="8761d-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8761d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8761d-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="8761d-131">RuleID</span></span>  <br/> |<span data-ttu-id="8761d-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="8761d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8761d-133">必須</span><span class="sxs-lookup"><span data-stu-id="8761d-133">required</span></span>  <br/> |<span data-ttu-id="8761d-134">親の問題に関連する検証ルールの一意識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8761d-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="8761d-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="8761d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8761d-136">rulesetid</span><span class="sxs-lookup"><span data-stu-id="8761d-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="8761d-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="8761d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8761d-138">必須</span><span class="sxs-lookup"><span data-stu-id="8761d-138">required</span></span>  <br/> |<span data-ttu-id="8761d-139">親の問題に関連する入力規則セットの一意識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="8761d-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="8761d-140">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="8761d-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

