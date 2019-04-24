---
title: authorlist 要素 (Comments_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: 図面内のコメントの作成者を指定します。
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338417"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="d8a00-103">authorlist 要素 (Comments_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d8a00-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d8a00-104">図面内のコメントの作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8a00-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d8a00-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8a00-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d8a00-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d8a00-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="d8a00-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d8a00-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8a00-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d8a00-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d8a00-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d8a00-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d8a00-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d8a00-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d8a00-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d8a00-112">comments</span><span class="sxs-lookup"><span data-stu-id="d8a00-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8a00-113">定義</span><span class="sxs-lookup"><span data-stu-id="d8a00-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d8a00-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d8a00-114">Elements and attributes</span></span>

<span data-ttu-id="d8a00-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8a00-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d8a00-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d8a00-116">Parent elements</span></span>

|<span data-ttu-id="d8a00-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="d8a00-117">**Element**</span></span>|<span data-ttu-id="d8a00-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d8a00-118">**Type**</span></span>|<span data-ttu-id="d8a00-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8a00-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8a00-120">コメント</span><span class="sxs-lookup"><span data-stu-id="d8a00-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8a00-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="d8a00-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8a00-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d8a00-123">子要素</span><span class="sxs-lookup"><span data-stu-id="d8a00-123">Child elements</span></span>

|<span data-ttu-id="d8a00-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8a00-124">**Element**</span></span>|<span data-ttu-id="d8a00-125">**型**</span><span class="sxs-lookup"><span data-stu-id="d8a00-125">**Type**</span></span>|<span data-ttu-id="d8a00-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8a00-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8a00-127">authorentry</span><span class="sxs-lookup"><span data-stu-id="d8a00-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8a00-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d8a00-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d8a00-129">図面内のコメントの作成者を識別するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8a00-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d8a00-130">属性</span><span class="sxs-lookup"><span data-stu-id="d8a00-130">Attributes</span></span>

<span data-ttu-id="d8a00-131">なし。</span><span class="sxs-lookup"><span data-stu-id="d8a00-131">None.</span></span>
  

