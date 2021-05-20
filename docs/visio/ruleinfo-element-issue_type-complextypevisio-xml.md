---
title: RuleInfo 要素 (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: 親検証の問題に関連する検証ルールに関する情報を指定します。
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541688"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="a2684-103">RuleInfo 要素 (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a2684-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a2684-104">親検証の問題に関連する検証ルールに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2684-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2684-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a2684-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2684-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a2684-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a2684-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="a2684-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a2684-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a2684-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a2684-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a2684-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a2684-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a2684-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a2684-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a2684-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a2684-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="a2684-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2684-113">定義</span><span class="sxs-lookup"><span data-stu-id="a2684-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a2684-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a2684-114">Elements and attributes</span></span>

<span data-ttu-id="a2684-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2684-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a2684-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a2684-116">Parent elements</span></span>

|<span data-ttu-id="a2684-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a2684-117">**Element**</span></span>|<span data-ttu-id="a2684-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a2684-118">**Type**</span></span>|<span data-ttu-id="a2684-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2684-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a2684-120">Issue</span><span class="sxs-lookup"><span data-stu-id="a2684-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a2684-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="a2684-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a2684-122">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="a2684-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a2684-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a2684-123">Child elements</span></span>

<span data-ttu-id="a2684-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a2684-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2684-125">属性</span><span class="sxs-lookup"><span data-stu-id="a2684-125">Attributes</span></span>

|<span data-ttu-id="a2684-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="a2684-126">**Attribute**</span></span>|<span data-ttu-id="a2684-127">**型**</span><span class="sxs-lookup"><span data-stu-id="a2684-127">**Type**</span></span>|<span data-ttu-id="a2684-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="a2684-128">**Required**</span></span>|<span data-ttu-id="a2684-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2684-129">**Description**</span></span>|<span data-ttu-id="a2684-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a2684-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2684-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="a2684-131">RuleID</span></span>  <br/> |<span data-ttu-id="a2684-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2684-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2684-133">必須</span><span class="sxs-lookup"><span data-stu-id="a2684-133">required</span></span>  <br/> |<span data-ttu-id="a2684-134">親の問題に関連する検証ルールの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2684-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="a2684-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a2684-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a2684-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="a2684-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="a2684-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a2684-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a2684-138">必須</span><span class="sxs-lookup"><span data-stu-id="a2684-138">required</span></span>  <br/> |<span data-ttu-id="a2684-139">親の問題に関連する検証ルール セットの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="a2684-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="a2684-140">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="a2684-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

