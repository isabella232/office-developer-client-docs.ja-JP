---
title: コメント要素 (Comments_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: 図面内のコメント、作成者を識別するためのプロパティを指定します。
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389646"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="1eb0c-103">コメント要素 (Comments_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1eb0c-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1eb0c-104">図面内のコメント、作成者を識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1eb0c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1eb0c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1eb0c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1eb0c-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="1eb0c-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1eb0c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1eb0c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1eb0c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1eb0c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1eb0c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1eb0c-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="1eb0c-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1eb0c-113">定義</span><span class="sxs-lookup"><span data-stu-id="1eb0c-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1eb0c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1eb0c-114">Elements and attributes</span></span>

<span data-ttu-id="1eb0c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1eb0c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1eb0c-116">Parent elements</span></span>

<span data-ttu-id="1eb0c-117">なし。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1eb0c-118">子要素</span><span class="sxs-lookup"><span data-stu-id="1eb0c-118">Child elements</span></span>

|<span data-ttu-id="1eb0c-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-119">**Element**</span></span>|<span data-ttu-id="1eb0c-120">**型**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-120">**Type**</span></span>|<span data-ttu-id="1eb0c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1eb0c-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="1eb0c-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1eb0c-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="1eb0c-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1eb0c-124">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="1eb0c-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="1eb0c-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1eb0c-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="1eb0c-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1eb0c-127">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1eb0c-128">属性</span><span class="sxs-lookup"><span data-stu-id="1eb0c-128">Attributes</span></span>

<span data-ttu-id="1eb0c-129">なし。</span><span class="sxs-lookup"><span data-stu-id="1eb0c-129">None.</span></span>
  

