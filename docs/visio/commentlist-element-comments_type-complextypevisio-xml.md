---
title: CommentList 要素 (Comments_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: 図面内のコメントを指定します。
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805048"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="804db-103">CommentList 要素 (Comments_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="804db-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="804db-104">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="804db-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="804db-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="804db-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="804db-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="804db-106">**Element type**</span></span> <br/> |[<span data-ttu-id="804db-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="804db-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="804db-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="804db-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="804db-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="804db-109">**Schema file**</span></span> <br/> |<span data-ttu-id="804db-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="804db-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="804db-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="804db-111">**Document parts**</span></span> <br/> |<span data-ttu-id="804db-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="804db-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="804db-113">定義</span><span class="sxs-lookup"><span data-stu-id="804db-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="804db-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="804db-114">Elements and attributes</span></span>

<span data-ttu-id="804db-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="804db-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="804db-116">親要素</span><span class="sxs-lookup"><span data-stu-id="804db-116">Parent elements</span></span>

|<span data-ttu-id="804db-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="804db-117">**Element**</span></span>|<span data-ttu-id="804db-118">**型**</span><span class="sxs-lookup"><span data-stu-id="804db-118">**Type**</span></span>|<span data-ttu-id="804db-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="804db-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="804db-120">Comments</span><span class="sxs-lookup"><span data-stu-id="804db-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="804db-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="804db-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="804db-122">図面内のコメント、作成者を識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="804db-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="804db-123">子要素</span><span class="sxs-lookup"><span data-stu-id="804db-123">Child elements</span></span>

|<span data-ttu-id="804db-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="804db-124">**Element**</span></span>|<span data-ttu-id="804db-125">**型**</span><span class="sxs-lookup"><span data-stu-id="804db-125">**Type**</span></span>|<span data-ttu-id="804db-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="804db-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="804db-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="804db-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="804db-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="804db-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="804db-129">図面内のコメントを識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="804db-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="804db-130">属性</span><span class="sxs-lookup"><span data-stu-id="804db-130">Attributes</span></span>

<span data-ttu-id="804db-131">なし。</span><span class="sxs-lookup"><span data-stu-id="804db-131">None.</span></span>
  

