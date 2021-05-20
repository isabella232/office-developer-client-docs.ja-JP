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
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="1ffba-103">AuthorList 要素 (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1ffba-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1ffba-104">図面内のコメントの作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="1ffba-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ffba-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="1ffba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ffba-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1ffba-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1ffba-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="1ffba-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ffba-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ffba-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ffba-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1ffba-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1ffba-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1ffba-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ffba-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="1ffba-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1ffba-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="1ffba-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ffba-113">定義</span><span class="sxs-lookup"><span data-stu-id="1ffba-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ffba-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1ffba-114">Elements and attributes</span></span>

<span data-ttu-id="1ffba-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ffba-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ffba-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1ffba-116">Parent elements</span></span>

|<span data-ttu-id="1ffba-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1ffba-117">**Element**</span></span>|<span data-ttu-id="1ffba-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1ffba-118">**Type**</span></span>|<span data-ttu-id="1ffba-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1ffba-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ffba-120">コメント</span><span class="sxs-lookup"><span data-stu-id="1ffba-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ffba-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="1ffba-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ffba-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="1ffba-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ffba-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1ffba-123">Child elements</span></span>

|<span data-ttu-id="1ffba-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ffba-124">**Element**</span></span>|<span data-ttu-id="1ffba-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1ffba-125">**Type**</span></span>|<span data-ttu-id="1ffba-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1ffba-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ffba-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="1ffba-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ffba-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1ffba-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ffba-129">図面内のコメントの作成者を識別するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="1ffba-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1ffba-130">属性</span><span class="sxs-lookup"><span data-stu-id="1ffba-130">Attributes</span></span>

<span data-ttu-id="1ffba-131">なし。</span><span class="sxs-lookup"><span data-stu-id="1ffba-131">None.</span></span>
  

