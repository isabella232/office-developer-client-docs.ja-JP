---
title: IssueTarget 要素 (Issue_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親の検証の問題の対象に応じて、親の検証の問題に関連付けられているページ、またはページと図形の両方を指定します。 親の検証の問題の対象がドキュメントの場合は、IssueTarget はページと図形のどちらも指定しません。
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542955"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="80d7d-104">IssueTarget 要素 (Issue_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="80d7d-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="80d7d-105">親の検証の問題の対象に応じて、親の検証の問題に関連付けられているページ、またはページと図形の両方を指定します。</span><span class="sxs-lookup"><span data-stu-id="80d7d-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="80d7d-106">親の検証の問題の対象がドキュメントの場合は、**IssueTarget** はページと図形のどちらも指定しません。</span><span class="sxs-lookup"><span data-stu-id="80d7d-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="80d7d-107">要素の情報</span><span class="sxs-lookup"><span data-stu-id="80d7d-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80d7d-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="80d7d-108">**Element type**</span></span> <br/> |[<span data-ttu-id="80d7d-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="80d7d-109">IssueTarget_Type complexType</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="80d7d-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="80d7d-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="80d7d-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="80d7d-111">**Schema file**</span></span> <br/> |<span data-ttu-id="80d7d-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="80d7d-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="80d7d-113">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="80d7d-113">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="80d7d-114">validation.xml</span><span class="sxs-lookup"><span data-stu-id="80d7d-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="80d7d-115">定義</span><span class="sxs-lookup"><span data-stu-id="80d7d-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="80d7d-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="80d7d-116">Elements and attributes</span></span>

<span data-ttu-id="80d7d-117">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="80d7d-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="80d7d-118">親要素</span><span class="sxs-lookup"><span data-stu-id="80d7d-118">Parent elements</span></span>

|<span data-ttu-id="80d7d-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="80d7d-119">**Element**</span></span>|<span data-ttu-id="80d7d-120">**型**</span><span class="sxs-lookup"><span data-stu-id="80d7d-120">**Type**</span></span>|<span data-ttu-id="80d7d-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="80d7d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="80d7d-122">Issue</span><span class="sxs-lookup"><span data-stu-id="80d7d-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="80d7d-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="80d7d-123">Issue_Type complexType</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="80d7d-124">文書内の1つの検証問題を表します。</span><span class="sxs-lookup"><span data-stu-id="80d7d-124">Represents a single validation issue in the ValidationIssues collection of  a document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="80d7d-125">子要素</span><span class="sxs-lookup"><span data-stu-id="80d7d-125">Child elements</span></span>

<span data-ttu-id="80d7d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="80d7d-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80d7d-127">属性</span><span class="sxs-lookup"><span data-stu-id="80d7d-127">Attributes</span></span>

|<span data-ttu-id="80d7d-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="80d7d-128">**Attribute**</span></span>|<span data-ttu-id="80d7d-129">**型**</span><span class="sxs-lookup"><span data-stu-id="80d7d-129">**Type**</span></span>|<span data-ttu-id="80d7d-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="80d7d-130">**Required**</span></span>|<span data-ttu-id="80d7d-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="80d7d-131">**Description**</span></span>|<span data-ttu-id="80d7d-132">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="80d7d-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80d7d-133">PageID</span><span class="sxs-lookup"><span data-stu-id="80d7d-133">PageID</span></span>  <br/> |<span data-ttu-id="80d7d-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80d7d-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80d7d-135">必須</span><span class="sxs-lookup"><span data-stu-id="80d7d-135">required</span></span>  <br/> |<span data-ttu-id="80d7d-136">親の検証の問題に関連付けられているページの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="80d7d-136">Returns the ID of the page that is associated with the validation issue.</span></span> <span data-ttu-id="80d7d-137">ターゲットがドキュメントの場合は、PageID 値を 0xFFFFFFFF にすることができます。</span><span class="sxs-lookup"><span data-stu-id="80d7d-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="80d7d-138">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="80d7d-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="80d7d-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="80d7d-139">shapeId</span></span>  <br/> |<span data-ttu-id="80d7d-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="80d7d-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="80d7d-141">必須</span><span class="sxs-lookup"><span data-stu-id="80d7d-141">required</span></span>  <br/> |<span data-ttu-id="80d7d-142">親の検証の問題に関連付けられている図形の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="80d7d-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="80d7d-143">ターゲットがドキュメントまたはページの場合は、ShapeID 値を 0xFFFFFFFF にすることができます。</span><span class="sxs-lookup"><span data-stu-id="80d7d-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="80d7d-144">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="80d7d-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

