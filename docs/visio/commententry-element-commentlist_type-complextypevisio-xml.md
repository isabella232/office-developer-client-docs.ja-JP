---
title: CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: 図面内のコメントを識別するためのプロパティを指定します。
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397045"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="02318-103">CommentEntry 要素 (CommentList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="02318-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="02318-104">図面内のコメントを識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="02318-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02318-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="02318-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02318-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="02318-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02318-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="02318-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02318-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="02318-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02318-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="02318-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02318-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="02318-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02318-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="02318-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02318-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="02318-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02318-113">定義</span><span class="sxs-lookup"><span data-stu-id="02318-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02318-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="02318-114">Elements and attributes</span></span>

<span data-ttu-id="02318-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="02318-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02318-116">親要素</span><span class="sxs-lookup"><span data-stu-id="02318-116">Parent elements</span></span>

|<span data-ttu-id="02318-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="02318-117">**Element**</span></span>|<span data-ttu-id="02318-118">**型**</span><span class="sxs-lookup"><span data-stu-id="02318-118">**Type**</span></span>|<span data-ttu-id="02318-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="02318-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02318-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="02318-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02318-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="02318-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02318-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="02318-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02318-123">子要素</span><span class="sxs-lookup"><span data-stu-id="02318-123">Child elements</span></span>

<span data-ttu-id="02318-124">なし。</span><span class="sxs-lookup"><span data-stu-id="02318-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02318-125">属性</span><span class="sxs-lookup"><span data-stu-id="02318-125">Attributes</span></span>

|<span data-ttu-id="02318-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="02318-126">**Attribute**</span></span>|<span data-ttu-id="02318-127">**型**</span><span class="sxs-lookup"><span data-stu-id="02318-127">**Type**</span></span>|<span data-ttu-id="02318-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="02318-128">**Required**</span></span>|<span data-ttu-id="02318-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="02318-129">**Description**</span></span>|<span data-ttu-id="02318-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="02318-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02318-131">著者 Id</span><span class="sxs-lookup"><span data-stu-id="02318-131">AuthorID</span></span>  <br/> |<span data-ttu-id="02318-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02318-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02318-133">必須</span><span class="sxs-lookup"><span data-stu-id="02318-133">required</span></span>  <br/> |<span data-ttu-id="02318-134">作成者を識別する 1 から始まる値です。</span><span class="sxs-lookup"><span data-stu-id="02318-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="02318-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02318-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="02318-136">CommentID</span></span>  <br/> |<span data-ttu-id="02318-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02318-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02318-138">必須</span><span class="sxs-lookup"><span data-stu-id="02318-138">required</span></span>  <br/> |<span data-ttu-id="02318-139">図面ページにコメントを識別する一意の値です。</span><span class="sxs-lookup"><span data-stu-id="02318-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="02318-140">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02318-141">日付</span><span class="sxs-lookup"><span data-stu-id="02318-141">Date</span></span>  <br/> |<span data-ttu-id="02318-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="02318-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="02318-143">必須</span><span class="sxs-lookup"><span data-stu-id="02318-143">required</span></span>  <br/> |<span data-ttu-id="02318-144">コメントが作成された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="02318-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="02318-145">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="02318-146">終了</span><span class="sxs-lookup"><span data-stu-id="02318-146">Done</span></span>  <br/> |<span data-ttu-id="02318-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="02318-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="02318-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="02318-148">optional</span></span>  <br/> |<span data-ttu-id="02318-149">コメントの現在の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="02318-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="02318-150">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="02318-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="02318-151">EditDate</span></span>  <br/> |<span data-ttu-id="02318-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="02318-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="02318-153">省略可能</span><span class="sxs-lookup"><span data-stu-id="02318-153">optional</span></span>  <br/> |<span data-ttu-id="02318-154">コメントが最後に変更された日時を指定します。</span><span class="sxs-lookup"><span data-stu-id="02318-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="02318-155">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="02318-156">PageID</span><span class="sxs-lookup"><span data-stu-id="02318-156">PageID</span></span>  <br/> |<span data-ttu-id="02318-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02318-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02318-158">必須</span><span class="sxs-lookup"><span data-stu-id="02318-158">required</span></span>  <br/> |<span data-ttu-id="02318-159">コメントするには図面のページを識別する値です。</span><span class="sxs-lookup"><span data-stu-id="02318-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="02318-160">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02318-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="02318-161">ShapeID</span></span>  <br/> |<span data-ttu-id="02318-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02318-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02318-163">省略可能</span><span class="sxs-lookup"><span data-stu-id="02318-163">optional</span></span>  <br/> |<span data-ttu-id="02318-164">コメントするには図形を識別する値です。</span><span class="sxs-lookup"><span data-stu-id="02318-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="02318-165">ShapeID が指定されていない場合、コメントは、図面のページを参照します。</span><span class="sxs-lookup"><span data-stu-id="02318-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="02318-166">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02318-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

