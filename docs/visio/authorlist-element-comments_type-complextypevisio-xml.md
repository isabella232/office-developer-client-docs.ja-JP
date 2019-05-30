---
title: AuthorList 要素 (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: 図面内のコメントの作成者を指定します。
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537858"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="a767b-103">AuthorList 要素 (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a767b-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a767b-104">図面内のコメントの作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="a767b-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a767b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a767b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a767b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a767b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a767b-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="a767b-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a767b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a767b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a767b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a767b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a767b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="a767b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a767b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a767b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a767b-112">comments</span><span class="sxs-lookup"><span data-stu-id="a767b-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a767b-113">定義</span><span class="sxs-lookup"><span data-stu-id="a767b-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a767b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a767b-114">Elements and attributes</span></span>

<span data-ttu-id="a767b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a767b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a767b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a767b-116">Parent elements</span></span>

|<span data-ttu-id="a767b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a767b-117">**Element**</span></span>|<span data-ttu-id="a767b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a767b-118">**Type**</span></span>|<span data-ttu-id="a767b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a767b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a767b-120">コメント</span><span class="sxs-lookup"><span data-stu-id="a767b-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a767b-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="a767b-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a767b-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a767b-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a767b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a767b-123">Child elements</span></span>

|<span data-ttu-id="a767b-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a767b-124">**Element**</span></span>|<span data-ttu-id="a767b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a767b-125">**Type**</span></span>|<span data-ttu-id="a767b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a767b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a767b-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="a767b-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a767b-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="a767b-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a767b-129">図面内のコメントの作成者を識別するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a767b-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a767b-130">属性</span><span class="sxs-lookup"><span data-stu-id="a767b-130">Attributes</span></span>

<span data-ttu-id="a767b-131">なし。</span><span class="sxs-lookup"><span data-stu-id="a767b-131">None.</span></span>
  

