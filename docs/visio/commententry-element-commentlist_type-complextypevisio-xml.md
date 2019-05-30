---
title: コメント Entry 要素 (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するために使用するプロパティを指定します。
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540113"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="dff09-103">コメント Entry 要素 (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dff09-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="dff09-104">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="dff09-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dff09-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="dff09-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dff09-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="dff09-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dff09-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="dff09-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dff09-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dff09-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dff09-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dff09-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dff09-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="dff09-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dff09-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="dff09-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dff09-112">comments</span><span class="sxs-lookup"><span data-stu-id="dff09-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dff09-113">定義</span><span class="sxs-lookup"><span data-stu-id="dff09-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dff09-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dff09-114">Elements and attributes</span></span>

<span data-ttu-id="dff09-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dff09-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dff09-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dff09-116">Parent elements</span></span>

|<span data-ttu-id="dff09-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dff09-117">**Element**</span></span>|<span data-ttu-id="dff09-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dff09-118">**Type**</span></span>|<span data-ttu-id="dff09-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dff09-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dff09-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="dff09-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dff09-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="dff09-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dff09-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="dff09-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dff09-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dff09-123">Child elements</span></span>

<span data-ttu-id="dff09-124">なし。</span><span class="sxs-lookup"><span data-stu-id="dff09-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dff09-125">属性</span><span class="sxs-lookup"><span data-stu-id="dff09-125">Attributes</span></span>

|<span data-ttu-id="dff09-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="dff09-126">**Attribute**</span></span>|<span data-ttu-id="dff09-127">**型**</span><span class="sxs-lookup"><span data-stu-id="dff09-127">**Type**</span></span>|<span data-ttu-id="dff09-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="dff09-128">**Required**</span></span>|<span data-ttu-id="dff09-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="dff09-129">**Description**</span></span>|<span data-ttu-id="dff09-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="dff09-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dff09-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="dff09-131">AuthorID</span></span>  <br/> |<span data-ttu-id="dff09-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="dff09-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dff09-133">必須</span><span class="sxs-lookup"><span data-stu-id="dff09-133">required</span></span>  <br/> |<span data-ttu-id="dff09-134">作成者を識別する1から始まる値。</span><span class="sxs-lookup"><span data-stu-id="dff09-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="dff09-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dff09-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="dff09-136">CommentID</span></span>  <br/> |<span data-ttu-id="dff09-137">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="dff09-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dff09-138">必須</span><span class="sxs-lookup"><span data-stu-id="dff09-138">required</span></span>  <br/> |<span data-ttu-id="dff09-139">図面ページのコメントを識別する一意の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="dff09-140">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dff09-141">日付</span><span class="sxs-lookup"><span data-stu-id="dff09-141">Date</span></span>  <br/> |<span data-ttu-id="dff09-142">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="dff09-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="dff09-143">必須</span><span class="sxs-lookup"><span data-stu-id="dff09-143">required</span></span>  <br/> |<span data-ttu-id="dff09-144">コメントが作成された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="dff09-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="dff09-145">Xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="dff09-146">完了</span><span class="sxs-lookup"><span data-stu-id="dff09-146">Done</span></span>  <br/> |<span data-ttu-id="dff09-147">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="dff09-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="dff09-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="dff09-148">optional</span></span>  <br/> |<span data-ttu-id="dff09-149">コメントの現在の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="dff09-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="dff09-150">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="dff09-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="dff09-151">EditDate</span></span>  <br/> |<span data-ttu-id="dff09-152">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="dff09-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="dff09-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="dff09-153">optional</span></span>  <br/> |<span data-ttu-id="dff09-154">コメントが最後に変更された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="dff09-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="dff09-155">Xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="dff09-156">PageID</span><span class="sxs-lookup"><span data-stu-id="dff09-156">PageID</span></span>  <br/> |<span data-ttu-id="dff09-157">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="dff09-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dff09-158">必須</span><span class="sxs-lookup"><span data-stu-id="dff09-158">required</span></span>  <br/> |<span data-ttu-id="dff09-159">コメントがある図面ページを識別する値。</span><span class="sxs-lookup"><span data-stu-id="dff09-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="dff09-160">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dff09-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="dff09-161">ShapeID</span></span>  <br/> |<span data-ttu-id="dff09-162">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="dff09-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dff09-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="dff09-163">optional</span></span>  <br/> |<span data-ttu-id="dff09-164">コメントがある図形を識別する値。</span><span class="sxs-lookup"><span data-stu-id="dff09-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="dff09-165">ShapeID が指定されていない場合、コメントは図面ページを参照します。</span><span class="sxs-lookup"><span data-stu-id="dff09-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="dff09-166">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="dff09-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

