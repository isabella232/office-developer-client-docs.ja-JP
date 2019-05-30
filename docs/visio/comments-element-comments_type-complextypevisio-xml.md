---
title: Comments 要素 (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: 図面の作成者とコメントを識別するために使用するプロパティを指定します。
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539221"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="5721d-103">Comments 要素 (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5721d-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5721d-104">図面の作成者とコメントを識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="5721d-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5721d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5721d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5721d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5721d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5721d-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="5721d-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5721d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5721d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5721d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5721d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5721d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5721d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5721d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5721d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5721d-112">comments</span><span class="sxs-lookup"><span data-stu-id="5721d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5721d-113">定義</span><span class="sxs-lookup"><span data-stu-id="5721d-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5721d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5721d-114">Elements and attributes</span></span>

<span data-ttu-id="5721d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5721d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5721d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5721d-116">Parent elements</span></span>

<span data-ttu-id="5721d-117">なし。</span><span class="sxs-lookup"><span data-stu-id="5721d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5721d-118">子要素</span><span class="sxs-lookup"><span data-stu-id="5721d-118">Child elements</span></span>

|<span data-ttu-id="5721d-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="5721d-119">**Element**</span></span>|<span data-ttu-id="5721d-120">**型**</span><span class="sxs-lookup"><span data-stu-id="5721d-120">**Type**</span></span>|<span data-ttu-id="5721d-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="5721d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5721d-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="5721d-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5721d-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="5721d-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5721d-124">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="5721d-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="5721d-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="5721d-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5721d-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="5721d-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5721d-127">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="5721d-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5721d-128">属性</span><span class="sxs-lookup"><span data-stu-id="5721d-128">Attributes</span></span>

<span data-ttu-id="5721d-129">なし。</span><span class="sxs-lookup"><span data-stu-id="5721d-129">None.</span></span>
  

