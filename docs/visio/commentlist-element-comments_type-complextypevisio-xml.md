---
title: コメント list 要素 (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: 図面内のコメントを指定します。
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359431"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="833da-103">コメント list 要素 (Comments_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="833da-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="833da-104">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="833da-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="833da-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="833da-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="833da-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="833da-106">**Element type**</span></span> <br/> |[<span data-ttu-id="833da-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="833da-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="833da-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="833da-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="833da-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="833da-109">**Schema file**</span></span> <br/> |<span data-ttu-id="833da-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="833da-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="833da-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="833da-111">**Document parts**</span></span> <br/> |<span data-ttu-id="833da-112">comments</span><span class="sxs-lookup"><span data-stu-id="833da-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="833da-113">定義</span><span class="sxs-lookup"><span data-stu-id="833da-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="833da-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="833da-114">Elements and attributes</span></span>

<span data-ttu-id="833da-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="833da-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="833da-116">親要素</span><span class="sxs-lookup"><span data-stu-id="833da-116">Parent elements</span></span>

|<span data-ttu-id="833da-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="833da-117">**Element**</span></span>|<span data-ttu-id="833da-118">**型**</span><span class="sxs-lookup"><span data-stu-id="833da-118">**Type**</span></span>|<span data-ttu-id="833da-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="833da-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="833da-120">コメント</span><span class="sxs-lookup"><span data-stu-id="833da-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="833da-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="833da-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="833da-122">図面の作成者とコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="833da-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="833da-123">子要素</span><span class="sxs-lookup"><span data-stu-id="833da-123">Child elements</span></span>

|<span data-ttu-id="833da-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="833da-124">**Element**</span></span>|<span data-ttu-id="833da-125">**型**</span><span class="sxs-lookup"><span data-stu-id="833da-125">**Type**</span></span>|<span data-ttu-id="833da-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="833da-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="833da-127">コメントエントリ</span><span class="sxs-lookup"><span data-stu-id="833da-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="833da-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="833da-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="833da-129">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="833da-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="833da-130">属性</span><span class="sxs-lookup"><span data-stu-id="833da-130">Attributes</span></span>

<span data-ttu-id="833da-131">なし。</span><span class="sxs-lookup"><span data-stu-id="833da-131">None.</span></span>
  

