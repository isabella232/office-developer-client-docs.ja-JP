---
title: IssueTarget 要素 (Issue_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: 親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。 場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、IssueTarget を指定します。
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805650"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="564ef-104">IssueTarget 要素 (Issue_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="564ef-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="564ef-105">親のターゲットによっては、検証の問題は、ページ、またはページと両方親の検証の問題に関連付けられている図形を指定します。</span><span class="sxs-lookup"><span data-stu-id="564ef-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="564ef-106">場合は親の検証の問題の対象は、ドキュメント、ページと図形のどちらも、 **IssueTarget**を指定します。</span><span class="sxs-lookup"><span data-stu-id="564ef-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="564ef-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="564ef-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="564ef-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="564ef-108">**Element type**</span></span> <br/> |[<span data-ttu-id="564ef-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="564ef-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="564ef-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="564ef-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="564ef-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="564ef-111">**Schema file**</span></span> <br/> |<span data-ttu-id="564ef-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="564ef-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="564ef-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="564ef-113">**Document parts**</span></span> <br/> |<span data-ttu-id="564ef-114">validation.xml</span><span class="sxs-lookup"><span data-stu-id="564ef-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="564ef-115">定義</span><span class="sxs-lookup"><span data-stu-id="564ef-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="564ef-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="564ef-116">Elements and attributes</span></span>

<span data-ttu-id="564ef-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="564ef-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="564ef-118">親要素</span><span class="sxs-lookup"><span data-stu-id="564ef-118">Parent elements</span></span>

|<span data-ttu-id="564ef-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="564ef-119">**Element**</span></span>|<span data-ttu-id="564ef-120">**型**</span><span class="sxs-lookup"><span data-stu-id="564ef-120">**Type**</span></span>|<span data-ttu-id="564ef-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="564ef-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="564ef-122">問題</span><span class="sxs-lookup"><span data-stu-id="564ef-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="564ef-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="564ef-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="564ef-124">文書の 1 つの検証の問題を表します。</span><span class="sxs-lookup"><span data-stu-id="564ef-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="564ef-125">子要素</span><span class="sxs-lookup"><span data-stu-id="564ef-125">Child elements</span></span>

<span data-ttu-id="564ef-126">なし。</span><span class="sxs-lookup"><span data-stu-id="564ef-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="564ef-127">属性</span><span class="sxs-lookup"><span data-stu-id="564ef-127">Attributes</span></span>

|<span data-ttu-id="564ef-128">**属性**</span><span class="sxs-lookup"><span data-stu-id="564ef-128">**Attribute**</span></span>|<span data-ttu-id="564ef-129">**型**</span><span class="sxs-lookup"><span data-stu-id="564ef-129">**Type**</span></span>|<span data-ttu-id="564ef-130">**必須**</span><span class="sxs-lookup"><span data-stu-id="564ef-130">**Required**</span></span>|<span data-ttu-id="564ef-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="564ef-131">**Description**</span></span>|<span data-ttu-id="564ef-132">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="564ef-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="564ef-133">PageID</span><span class="sxs-lookup"><span data-stu-id="564ef-133">PageID</span></span>  <br/> |<span data-ttu-id="564ef-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="564ef-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="564ef-135">必須</span><span class="sxs-lookup"><span data-stu-id="564ef-135">required</span></span>  <br/> |<span data-ttu-id="564ef-136">親の検証の問題に関連付けられているページの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="564ef-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="564ef-137">ターゲットがドキュメントの場合は、PageID の値は 0 xffffffff にできます。</span><span class="sxs-lookup"><span data-stu-id="564ef-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="564ef-138">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="564ef-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="564ef-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="564ef-139">ShapeID</span></span>  <br/> |<span data-ttu-id="564ef-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="564ef-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="564ef-141">必須</span><span class="sxs-lookup"><span data-stu-id="564ef-141">required</span></span>  <br/> |<span data-ttu-id="564ef-142">親の検証の問題に関連付けられている図形の一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="564ef-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="564ef-143">ターゲットが、ドキュメントまたはページの場合は、ShapeID 値 0 xffffffff を使用できます。</span><span class="sxs-lookup"><span data-stu-id="564ef-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="564ef-144">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="564ef-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

