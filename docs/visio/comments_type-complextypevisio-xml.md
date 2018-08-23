---
title: Comments_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: 4d7a1d75387ddc84bec8eb1370cfb7d641c8a9ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805050"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="f3757-102">Comments_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="f3757-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f3757-103">型情報</span><span class="sxs-lookup"><span data-stu-id="f3757-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3757-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="f3757-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f3757-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f3757-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f3757-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f3757-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f3757-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="f3757-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f3757-108">なし</span><span class="sxs-lookup"><span data-stu-id="f3757-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3757-109">定義</span><span class="sxs-lookup"><span data-stu-id="f3757-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f3757-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f3757-110">Elements and attributes</span></span>

<span data-ttu-id="f3757-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3757-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f3757-112">子要素</span><span class="sxs-lookup"><span data-stu-id="f3757-112">Child elements</span></span>

|<span data-ttu-id="f3757-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="f3757-113">**Element**</span></span>|<span data-ttu-id="f3757-114">**型**</span><span class="sxs-lookup"><span data-stu-id="f3757-114">**Type**</span></span>|<span data-ttu-id="f3757-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="f3757-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3757-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="f3757-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3757-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="f3757-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f3757-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="f3757-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3757-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="f3757-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f3757-120">属性</span><span class="sxs-lookup"><span data-stu-id="f3757-120">Attributes</span></span>

|<span data-ttu-id="f3757-121">**属性**</span><span class="sxs-lookup"><span data-stu-id="f3757-121">**Attribute**</span></span>|<span data-ttu-id="f3757-122">**型**</span><span class="sxs-lookup"><span data-stu-id="f3757-122">**Type**</span></span>|<span data-ttu-id="f3757-123">**必須**</span><span class="sxs-lookup"><span data-stu-id="f3757-123">**Required**</span></span>|<span data-ttu-id="f3757-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="f3757-124">**Description**</span></span>|<span data-ttu-id="f3757-125">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="f3757-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3757-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="f3757-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="f3757-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="f3757-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f3757-128">省略可能</span><span class="sxs-lookup"><span data-stu-id="f3757-128">optional</span></span>  <br/> ||<span data-ttu-id="f3757-129">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3757-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

