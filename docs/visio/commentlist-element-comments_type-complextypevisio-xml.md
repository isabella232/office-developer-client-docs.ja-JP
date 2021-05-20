---
title: CommentList 要素 (Comments_Type complexType) (Visio XML)
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
# <a name="commentlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="e69be-103">CommentList 要素 (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e69be-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e69be-104">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="e69be-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e69be-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="e69be-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e69be-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e69be-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e69be-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="e69be-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e69be-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e69be-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e69be-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e69be-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e69be-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e69be-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e69be-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="e69be-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e69be-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="e69be-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e69be-113">定義</span><span class="sxs-lookup"><span data-stu-id="e69be-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e69be-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e69be-114">Elements and attributes</span></span>

<span data-ttu-id="e69be-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e69be-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e69be-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e69be-116">Parent elements</span></span>

|<span data-ttu-id="e69be-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e69be-117">**Element**</span></span>|<span data-ttu-id="e69be-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e69be-118">**Type**</span></span>|<span data-ttu-id="e69be-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e69be-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e69be-120">コメント</span><span class="sxs-lookup"><span data-stu-id="e69be-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e69be-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="e69be-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e69be-122">図面内の作成者とコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e69be-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e69be-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e69be-123">Child elements</span></span>

|<span data-ttu-id="e69be-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e69be-124">**Element**</span></span>|<span data-ttu-id="e69be-125">**型**</span><span class="sxs-lookup"><span data-stu-id="e69be-125">**Type**</span></span>|<span data-ttu-id="e69be-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="e69be-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e69be-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="e69be-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e69be-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="e69be-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e69be-129">図面内のコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="e69be-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e69be-130">属性</span><span class="sxs-lookup"><span data-stu-id="e69be-130">Attributes</span></span>

<span data-ttu-id="e69be-131">なし。</span><span class="sxs-lookup"><span data-stu-id="e69be-131">None.</span></span>
  

