---
title: CommentEntry 要素 (CommentList_Type complexType) (Visio XML)
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
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="76847-103">CommentEntry 要素 (CommentList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="76847-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="76847-104">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="76847-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76847-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="76847-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76847-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="76847-106">**Element type**</span></span> <br/> |[<span data-ttu-id="76847-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="76847-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="76847-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="76847-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="76847-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="76847-109">**Schema file**</span></span> <br/> |<span data-ttu-id="76847-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="76847-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="76847-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="76847-111">**Document parts**</span></span> <br/> |<span data-ttu-id="76847-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="76847-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76847-113">定義</span><span class="sxs-lookup"><span data-stu-id="76847-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="76847-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="76847-114">Elements and attributes</span></span>

<span data-ttu-id="76847-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76847-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="76847-116">親要素</span><span class="sxs-lookup"><span data-stu-id="76847-116">Parent elements</span></span>

|<span data-ttu-id="76847-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="76847-117">**Element**</span></span>|<span data-ttu-id="76847-118">**型**</span><span class="sxs-lookup"><span data-stu-id="76847-118">**Type**</span></span>|<span data-ttu-id="76847-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="76847-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="76847-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="76847-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="76847-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="76847-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="76847-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="76847-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="76847-123">子要素</span><span class="sxs-lookup"><span data-stu-id="76847-123">Child elements</span></span>

<span data-ttu-id="76847-124">なし。</span><span class="sxs-lookup"><span data-stu-id="76847-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76847-125">属性</span><span class="sxs-lookup"><span data-stu-id="76847-125">Attributes</span></span>

|<span data-ttu-id="76847-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="76847-126">**Attribute**</span></span>|<span data-ttu-id="76847-127">**型**</span><span class="sxs-lookup"><span data-stu-id="76847-127">**Type**</span></span>|<span data-ttu-id="76847-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="76847-128">**Required**</span></span>|<span data-ttu-id="76847-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="76847-129">**Description**</span></span>|<span data-ttu-id="76847-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="76847-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="76847-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="76847-131">AuthorID</span></span>  <br/> |<span data-ttu-id="76847-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76847-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76847-133">必須</span><span class="sxs-lookup"><span data-stu-id="76847-133">required</span></span>  <br/> |<span data-ttu-id="76847-134">作成者を識別する 1 ベースの値。</span><span class="sxs-lookup"><span data-stu-id="76847-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="76847-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76847-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="76847-136">CommentID</span></span>  <br/> |<span data-ttu-id="76847-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76847-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76847-138">必須</span><span class="sxs-lookup"><span data-stu-id="76847-138">required</span></span>  <br/> |<span data-ttu-id="76847-139">図面ページのコメントを識別する一意の値。</span><span class="sxs-lookup"><span data-stu-id="76847-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="76847-140">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76847-141">日付</span><span class="sxs-lookup"><span data-stu-id="76847-141">Date</span></span>  <br/> |<span data-ttu-id="76847-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="76847-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="76847-143">必須</span><span class="sxs-lookup"><span data-stu-id="76847-143">required</span></span>  <br/> |<span data-ttu-id="76847-144">コメントが作成された時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="76847-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="76847-145">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="76847-146">完了</span><span class="sxs-lookup"><span data-stu-id="76847-146">Done</span></span>  <br/> |<span data-ttu-id="76847-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="76847-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="76847-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="76847-148">optional</span></span>  <br/> |<span data-ttu-id="76847-149">コメントの現在の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="76847-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="76847-150">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="76847-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="76847-151">EditDate</span></span>  <br/> |<span data-ttu-id="76847-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="76847-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="76847-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="76847-153">optional</span></span>  <br/> |<span data-ttu-id="76847-154">コメントが最後に変更された時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="76847-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="76847-155">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="76847-156">PageID</span><span class="sxs-lookup"><span data-stu-id="76847-156">PageID</span></span>  <br/> |<span data-ttu-id="76847-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76847-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76847-158">必須</span><span class="sxs-lookup"><span data-stu-id="76847-158">required</span></span>  <br/> |<span data-ttu-id="76847-159">コメントが表示されている図面ページを識別する値。</span><span class="sxs-lookup"><span data-stu-id="76847-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="76847-160">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="76847-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="76847-161">ShapeID</span></span>  <br/> |<span data-ttu-id="76847-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="76847-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="76847-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="76847-163">optional</span></span>  <br/> |<span data-ttu-id="76847-164">コメントがオンの図形を識別する値。</span><span class="sxs-lookup"><span data-stu-id="76847-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="76847-165">ShapeID が指定されていない場合、コメントは図面ページを参照します。</span><span class="sxs-lookup"><span data-stu-id="76847-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="76847-166">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="76847-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

