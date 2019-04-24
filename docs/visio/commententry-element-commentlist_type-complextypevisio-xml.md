---
title: コメント entry 要素 (CommentList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するために使用するプロパティを指定します。
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329541"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="470ec-103">コメント entry 要素 (CommentList_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="470ec-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="470ec-104">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="470ec-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="470ec-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="470ec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="470ec-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="470ec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="470ec-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="470ec-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="470ec-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="470ec-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="470ec-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="470ec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="470ec-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="470ec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="470ec-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="470ec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="470ec-112">comments</span><span class="sxs-lookup"><span data-stu-id="470ec-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="470ec-113">定義</span><span class="sxs-lookup"><span data-stu-id="470ec-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="470ec-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="470ec-114">Elements and attributes</span></span>

<span data-ttu-id="470ec-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="470ec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="470ec-116">親要素</span><span class="sxs-lookup"><span data-stu-id="470ec-116">Parent elements</span></span>

|<span data-ttu-id="470ec-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="470ec-117">**Element**</span></span>|<span data-ttu-id="470ec-118">**型**</span><span class="sxs-lookup"><span data-stu-id="470ec-118">**Type**</span></span>|<span data-ttu-id="470ec-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="470ec-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="470ec-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="470ec-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="470ec-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="470ec-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="470ec-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="470ec-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="470ec-123">子要素</span><span class="sxs-lookup"><span data-stu-id="470ec-123">Child elements</span></span>

<span data-ttu-id="470ec-124">なし。</span><span class="sxs-lookup"><span data-stu-id="470ec-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="470ec-125">属性</span><span class="sxs-lookup"><span data-stu-id="470ec-125">Attributes</span></span>

|<span data-ttu-id="470ec-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="470ec-126">**Attribute**</span></span>|<span data-ttu-id="470ec-127">**型**</span><span class="sxs-lookup"><span data-stu-id="470ec-127">**Type**</span></span>|<span data-ttu-id="470ec-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="470ec-128">**Required**</span></span>|<span data-ttu-id="470ec-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="470ec-129">**Description**</span></span>|<span data-ttu-id="470ec-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="470ec-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="470ec-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="470ec-131">AuthorID</span></span>  <br/> |<span data-ttu-id="470ec-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="470ec-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ec-133">必須</span><span class="sxs-lookup"><span data-stu-id="470ec-133">required</span></span>  <br/> |<span data-ttu-id="470ec-134">作成者を識別する1から始まる値。</span><span class="sxs-lookup"><span data-stu-id="470ec-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="470ec-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ec-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="470ec-136">CommentID</span></span>  <br/> |<span data-ttu-id="470ec-137">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="470ec-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ec-138">必須</span><span class="sxs-lookup"><span data-stu-id="470ec-138">required</span></span>  <br/> |<span data-ttu-id="470ec-139">図面ページのコメントを識別する一意の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="470ec-140">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ec-141">日付</span><span class="sxs-lookup"><span data-stu-id="470ec-141">Date</span></span>  <br/> |<span data-ttu-id="470ec-142">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="470ec-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="470ec-143">必須</span><span class="sxs-lookup"><span data-stu-id="470ec-143">required</span></span>  <br/> |<span data-ttu-id="470ec-144">コメントが作成された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="470ec-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="470ec-145">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="470ec-146">完了</span><span class="sxs-lookup"><span data-stu-id="470ec-146">Done</span></span>  <br/> |<span data-ttu-id="470ec-147">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="470ec-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="470ec-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="470ec-148">optional</span></span>  <br/> |<span data-ttu-id="470ec-149">コメントの現在の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="470ec-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="470ec-150">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="470ec-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="470ec-151">EditDate</span></span>  <br/> |<span data-ttu-id="470ec-152">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="470ec-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="470ec-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="470ec-153">optional</span></span>  <br/> |<span data-ttu-id="470ec-154">コメントが最後に変更された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="470ec-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="470ec-155">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="470ec-156">PageID</span><span class="sxs-lookup"><span data-stu-id="470ec-156">PageID</span></span>  <br/> |<span data-ttu-id="470ec-157">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="470ec-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ec-158">必須</span><span class="sxs-lookup"><span data-stu-id="470ec-158">required</span></span>  <br/> |<span data-ttu-id="470ec-159">コメントがある図面ページを識別する値。</span><span class="sxs-lookup"><span data-stu-id="470ec-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="470ec-160">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="470ec-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="470ec-161">ShapeID</span></span>  <br/> |<span data-ttu-id="470ec-162">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="470ec-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="470ec-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="470ec-163">optional</span></span>  <br/> |<span data-ttu-id="470ec-164">コメントがある図形を識別する値。</span><span class="sxs-lookup"><span data-stu-id="470ec-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="470ec-165">ShapeID が指定されていない場合、コメントは図面ページを参照します。</span><span class="sxs-lookup"><span data-stu-id="470ec-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="470ec-166">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="470ec-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

