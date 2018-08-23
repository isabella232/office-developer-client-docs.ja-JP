---
title: CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するためのプロパティを指定します。
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805043"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="c3442-103">CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c3442-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c3442-104">図面内のコメントを識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="c3442-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3442-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c3442-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3442-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c3442-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c3442-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="c3442-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3442-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c3442-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3442-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c3442-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c3442-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c3442-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3442-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c3442-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c3442-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="c3442-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3442-113">定義</span><span class="sxs-lookup"><span data-stu-id="c3442-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3442-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c3442-114">Elements and attributes</span></span>

<span data-ttu-id="c3442-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3442-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3442-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c3442-116">Parent elements</span></span>

|<span data-ttu-id="c3442-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c3442-117">**Element**</span></span>|<span data-ttu-id="c3442-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c3442-118">**Type**</span></span>|<span data-ttu-id="c3442-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3442-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3442-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="c3442-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3442-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="c3442-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3442-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="c3442-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3442-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c3442-123">Child elements</span></span>

<span data-ttu-id="c3442-124">なし。</span><span class="sxs-lookup"><span data-stu-id="c3442-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3442-125">属性</span><span class="sxs-lookup"><span data-stu-id="c3442-125">Attributes</span></span>

|<span data-ttu-id="c3442-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="c3442-126">**Attribute**</span></span>|<span data-ttu-id="c3442-127">**型**</span><span class="sxs-lookup"><span data-stu-id="c3442-127">**Type**</span></span>|<span data-ttu-id="c3442-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="c3442-128">**Required**</span></span>|<span data-ttu-id="c3442-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3442-129">**Description**</span></span>|<span data-ttu-id="c3442-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="c3442-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3442-131">著者 Id</span><span class="sxs-lookup"><span data-stu-id="c3442-131">AuthorID</span></span>  <br/> |<span data-ttu-id="c3442-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3442-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3442-133">必須</span><span class="sxs-lookup"><span data-stu-id="c3442-133">required</span></span>  <br/> |<span data-ttu-id="c3442-134">作成者を識別する 1 から始まる値です。</span><span class="sxs-lookup"><span data-stu-id="c3442-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="c3442-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3442-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="c3442-136">CommentID</span></span>  <br/> |<span data-ttu-id="c3442-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3442-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3442-138">必須</span><span class="sxs-lookup"><span data-stu-id="c3442-138">required</span></span>  <br/> |<span data-ttu-id="c3442-139">図面ページにコメントを識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="c3442-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="c3442-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3442-141">日付</span><span class="sxs-lookup"><span data-stu-id="c3442-141">Date</span></span>  <br/> |<span data-ttu-id="c3442-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="c3442-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c3442-143">必須</span><span class="sxs-lookup"><span data-stu-id="c3442-143">required</span></span>  <br/> |<span data-ttu-id="c3442-144">コメントが作成された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3442-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="c3442-145">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="c3442-146">終了</span><span class="sxs-lookup"><span data-stu-id="c3442-146">Done</span></span>  <br/> |<span data-ttu-id="c3442-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c3442-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c3442-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="c3442-148">optional</span></span>  <br/> |<span data-ttu-id="c3442-149">コメントの現在の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3442-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="c3442-150">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c3442-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="c3442-151">EditDate</span></span>  <br/> |<span data-ttu-id="c3442-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="c3442-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c3442-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="c3442-153">optional</span></span>  <br/> |<span data-ttu-id="c3442-154">コメントが最後に変更された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3442-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="c3442-155">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="c3442-156">PageID</span><span class="sxs-lookup"><span data-stu-id="c3442-156">PageID</span></span>  <br/> |<span data-ttu-id="c3442-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3442-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3442-158">必須</span><span class="sxs-lookup"><span data-stu-id="c3442-158">required</span></span>  <br/> |<span data-ttu-id="c3442-159">コメントするには図面のページを識別する値です。</span><span class="sxs-lookup"><span data-stu-id="c3442-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="c3442-160">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3442-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="c3442-161">ShapeID</span></span>  <br/> |<span data-ttu-id="c3442-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c3442-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3442-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="c3442-163">optional</span></span>  <br/> |<span data-ttu-id="c3442-164">コメントするには図形を識別する値です。</span><span class="sxs-lookup"><span data-stu-id="c3442-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="c3442-165">ShapeID が指定されていない場合、コメントは、図面のページを参照します。</span><span class="sxs-lookup"><span data-stu-id="c3442-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="c3442-166">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3442-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

