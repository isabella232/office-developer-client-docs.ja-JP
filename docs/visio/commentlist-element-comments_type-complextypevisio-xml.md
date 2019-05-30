---
title: コメント List 要素 (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: 図面内のコメントを指定します。
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539249"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="02d02-103">コメント List 要素 (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02d02-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="02d02-104">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="02d02-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02d02-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="02d02-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02d02-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="02d02-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02d02-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="02d02-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02d02-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="02d02-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02d02-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="02d02-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02d02-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="02d02-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02d02-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="02d02-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02d02-112">comments</span><span class="sxs-lookup"><span data-stu-id="02d02-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02d02-113">定義</span><span class="sxs-lookup"><span data-stu-id="02d02-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02d02-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="02d02-114">Elements and attributes</span></span>

<span data-ttu-id="02d02-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="02d02-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02d02-116">親要素</span><span class="sxs-lookup"><span data-stu-id="02d02-116">Parent elements</span></span>

|<span data-ttu-id="02d02-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="02d02-117">**Element**</span></span>|<span data-ttu-id="02d02-118">**型**</span><span class="sxs-lookup"><span data-stu-id="02d02-118">**Type**</span></span>|<span data-ttu-id="02d02-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="02d02-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02d02-120">コメント</span><span class="sxs-lookup"><span data-stu-id="02d02-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02d02-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="02d02-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02d02-122">図面の作成者とコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="02d02-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02d02-123">子要素</span><span class="sxs-lookup"><span data-stu-id="02d02-123">Child elements</span></span>

|<span data-ttu-id="02d02-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="02d02-124">**Element**</span></span>|<span data-ttu-id="02d02-125">**型**</span><span class="sxs-lookup"><span data-stu-id="02d02-125">**Type**</span></span>|<span data-ttu-id="02d02-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="02d02-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02d02-127">コメントエントリ</span><span class="sxs-lookup"><span data-stu-id="02d02-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02d02-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="02d02-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02d02-129">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="02d02-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="02d02-130">属性</span><span class="sxs-lookup"><span data-stu-id="02d02-130">Attributes</span></span>

<span data-ttu-id="02d02-131">なし。</span><span class="sxs-lookup"><span data-stu-id="02d02-131">None.</span></span>
  

