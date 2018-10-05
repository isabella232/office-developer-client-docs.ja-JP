---
title: IssueTarget 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。 場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、IssueTarget を指定します。
ms.openlocfilehash: 74005bfb6035e32b7b34fdd5a8a5737813a562a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385362"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="54ea1-104">IssueTarget 要素 (Issue_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="54ea1-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="54ea1-105">親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="54ea1-106">場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、 **IssueTarget**を指定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="54ea1-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="54ea1-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54ea1-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="54ea1-108">**Element type**</span></span> <br/> |[<span data-ttu-id="54ea1-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="54ea1-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54ea1-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="54ea1-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54ea1-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="54ea1-111">**Schema file**</span></span> <br/> |<span data-ttu-id="54ea1-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="54ea1-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54ea1-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="54ea1-113">**Document parts**</span></span> <br/> |<span data-ttu-id="54ea1-114">validation.xml</span><span class="sxs-lookup"><span data-stu-id="54ea1-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54ea1-115">定義</span><span class="sxs-lookup"><span data-stu-id="54ea1-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54ea1-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="54ea1-116">Elements and attributes</span></span>

<span data-ttu-id="54ea1-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="54ea1-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54ea1-118">親要素</span><span class="sxs-lookup"><span data-stu-id="54ea1-118">Parent elements</span></span>

|<span data-ttu-id="54ea1-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="54ea1-119">**Element**</span></span>|<span data-ttu-id="54ea1-120">**型**</span><span class="sxs-lookup"><span data-stu-id="54ea1-120">**Type**</span></span>|<span data-ttu-id="54ea1-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="54ea1-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54ea1-122">問題</span><span class="sxs-lookup"><span data-stu-id="54ea1-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54ea1-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="54ea1-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54ea1-124">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54ea1-125">子要素</span><span class="sxs-lookup"><span data-stu-id="54ea1-125">Child elements</span></span>

<span data-ttu-id="54ea1-126">なし。</span><span class="sxs-lookup"><span data-stu-id="54ea1-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54ea1-127">属性</span><span class="sxs-lookup"><span data-stu-id="54ea1-127">Attributes</span></span>

|<span data-ttu-id="54ea1-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="54ea1-128">**Attribute**</span></span>|<span data-ttu-id="54ea1-129">**型**</span><span class="sxs-lookup"><span data-stu-id="54ea1-129">**Type**</span></span>|<span data-ttu-id="54ea1-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="54ea1-130">**Required**</span></span>|<span data-ttu-id="54ea1-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="54ea1-131">**Description**</span></span>|<span data-ttu-id="54ea1-132">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="54ea1-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="54ea1-133">PageID</span><span class="sxs-lookup"><span data-stu-id="54ea1-133">PageID</span></span>  <br/> |<span data-ttu-id="54ea1-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54ea1-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54ea1-135">必須</span><span class="sxs-lookup"><span data-stu-id="54ea1-135">required</span></span>  <br/> |<span data-ttu-id="54ea1-136">親の検証の問題に関連付けられているページの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="54ea1-137">ターゲットがドキュメントの場合は、PageID の値は 0 xffffffff にできます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="54ea1-138">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="54ea1-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="54ea1-139">ShapeID</span></span>  <br/> |<span data-ttu-id="54ea1-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="54ea1-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="54ea1-141">必須</span><span class="sxs-lookup"><span data-stu-id="54ea1-141">required</span></span>  <br/> |<span data-ttu-id="54ea1-142">親の検証の問題に関連付けられている図形の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="54ea1-143">ターゲットが、ドキュメントまたはページの場合は、ShapeID 値 0 xffffffff を使用できます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="54ea1-144">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

