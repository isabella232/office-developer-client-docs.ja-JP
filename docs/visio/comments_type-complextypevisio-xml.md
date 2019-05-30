---
title: Comments_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542017"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="55232-102">Comments_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="55232-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="55232-103">型情報</span><span class="sxs-lookup"><span data-stu-id="55232-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55232-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="55232-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="55232-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="55232-105">**Schema file**</span></span> <br/> |<span data-ttu-id="55232-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="55232-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="55232-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="55232-107">**Extension base**</span></span> <br/> |<span data-ttu-id="55232-108">None</span><span class="sxs-lookup"><span data-stu-id="55232-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55232-109">定義</span><span class="sxs-lookup"><span data-stu-id="55232-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="55232-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="55232-110">Elements and attributes</span></span>

<span data-ttu-id="55232-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="55232-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="55232-112">子要素</span><span class="sxs-lookup"><span data-stu-id="55232-112">Child elements</span></span>

|<span data-ttu-id="55232-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="55232-113">**Element**</span></span>|<span data-ttu-id="55232-114">**型**</span><span class="sxs-lookup"><span data-stu-id="55232-114">**Type**</span></span>|<span data-ttu-id="55232-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="55232-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55232-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="55232-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55232-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="55232-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="55232-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="55232-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55232-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="55232-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="55232-120">属性</span><span class="sxs-lookup"><span data-stu-id="55232-120">Attributes</span></span>

|<span data-ttu-id="55232-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="55232-121">**Attribute**</span></span>|<span data-ttu-id="55232-122">**型**</span><span class="sxs-lookup"><span data-stu-id="55232-122">**Type**</span></span>|<span data-ttu-id="55232-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="55232-123">**Required**</span></span>|<span data-ttu-id="55232-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="55232-124">**Description**</span></span>|<span data-ttu-id="55232-125">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="55232-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="55232-126">Showコメントタグ</span><span class="sxs-lookup"><span data-stu-id="55232-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="55232-127">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="55232-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="55232-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="55232-128">optional</span></span>  <br/> ||<span data-ttu-id="55232-129">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="55232-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

