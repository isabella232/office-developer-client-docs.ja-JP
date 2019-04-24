---
title: /出力先要素 (Issue_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親の検証問題のターゲットに応じて、親の検証の問題に関連付けられているページまたはページと図形の両方を指定します。 親の検証問題のターゲットがドキュメントの場合は、ページまたは図形のどちらも対象外になります。
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332523"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="5857c-104">/出力先要素 (Issue_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="5857c-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5857c-105">親の検証問題のターゲットに応じて、親の検証の問題に関連付けられているページまたはページと図形の両方を指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="5857c-106">親の検証問題のターゲットがドキュメントの場合は、ページまたは図形のどちらも**対象**外になります。</span><span class="sxs-lookup"><span data-stu-id="5857c-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5857c-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="5857c-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5857c-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5857c-108">**Element type**</span></span> <br/> |[<span data-ttu-id="5857c-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="5857c-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5857c-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5857c-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5857c-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5857c-111">**Schema file**</span></span> <br/> |<span data-ttu-id="5857c-112">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5857c-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5857c-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5857c-113">**Document parts**</span></span> <br/> |<span data-ttu-id="5857c-114">検証 xml</span><span class="sxs-lookup"><span data-stu-id="5857c-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5857c-115">定義</span><span class="sxs-lookup"><span data-stu-id="5857c-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5857c-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5857c-116">Elements and attributes</span></span>

<span data-ttu-id="5857c-117">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5857c-118">親要素</span><span class="sxs-lookup"><span data-stu-id="5857c-118">Parent elements</span></span>

|<span data-ttu-id="5857c-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="5857c-119">**Element**</span></span>|<span data-ttu-id="5857c-120">**型**</span><span class="sxs-lookup"><span data-stu-id="5857c-120">**Type**</span></span>|<span data-ttu-id="5857c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="5857c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5857c-122">問題</span><span class="sxs-lookup"><span data-stu-id="5857c-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5857c-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="5857c-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5857c-124">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="5857c-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5857c-125">子要素</span><span class="sxs-lookup"><span data-stu-id="5857c-125">Child elements</span></span>

<span data-ttu-id="5857c-126">なし。</span><span class="sxs-lookup"><span data-stu-id="5857c-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5857c-127">属性</span><span class="sxs-lookup"><span data-stu-id="5857c-127">Attributes</span></span>

|<span data-ttu-id="5857c-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="5857c-128">**Attribute**</span></span>|<span data-ttu-id="5857c-129">**型**</span><span class="sxs-lookup"><span data-stu-id="5857c-129">**Type**</span></span>|<span data-ttu-id="5857c-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="5857c-130">**Required**</span></span>|<span data-ttu-id="5857c-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="5857c-131">**Description**</span></span>|<span data-ttu-id="5857c-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="5857c-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5857c-133">PageID</span><span class="sxs-lookup"><span data-stu-id="5857c-133">PageID</span></span>  <br/> |<span data-ttu-id="5857c-134">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="5857c-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5857c-135">必須</span><span class="sxs-lookup"><span data-stu-id="5857c-135">required</span></span>  <br/> |<span data-ttu-id="5857c-136">親の検証問題に関連付けられているページの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="5857c-137">ターゲットがドキュメントの場合、PageID の値は0xffffffff になります。</span><span class="sxs-lookup"><span data-stu-id="5857c-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="5857c-138">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="5857c-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5857c-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="5857c-139">ShapeID</span></span>  <br/> |<span data-ttu-id="5857c-140">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="5857c-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5857c-141">必須</span><span class="sxs-lookup"><span data-stu-id="5857c-141">required</span></span>  <br/> |<span data-ttu-id="5857c-142">親の検証問題に関連付けられている図形の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="5857c-143">ターゲットがドキュメントまたはページである場合、ShapeID の値は0xffffffff にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5857c-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="5857c-144">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="5857c-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

