---
title: AuthorList 要素 (Comments_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: 図面内のコメントの作成者を指定します。
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387742"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="38e3c-103">AuthorList 要素 (Comments_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="38e3c-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="38e3c-104">図面内のコメントの作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="38e3c-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38e3c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="38e3c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38e3c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="38e3c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="38e3c-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="38e3c-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="38e3c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="38e3c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="38e3c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="38e3c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="38e3c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="38e3c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="38e3c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="38e3c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="38e3c-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="38e3c-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38e3c-113">定義</span><span class="sxs-lookup"><span data-stu-id="38e3c-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="38e3c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="38e3c-114">Elements and attributes</span></span>

<span data-ttu-id="38e3c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="38e3c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="38e3c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="38e3c-116">Parent elements</span></span>

|<span data-ttu-id="38e3c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="38e3c-117">**Element**</span></span>|<span data-ttu-id="38e3c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="38e3c-118">**Type**</span></span>|<span data-ttu-id="38e3c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="38e3c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38e3c-120">Comments</span><span class="sxs-lookup"><span data-stu-id="38e3c-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="38e3c-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="38e3c-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="38e3c-122">図面内のコメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="38e3c-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38e3c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="38e3c-123">Child elements</span></span>

|<span data-ttu-id="38e3c-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="38e3c-124">**Element**</span></span>|<span data-ttu-id="38e3c-125">**型**</span><span class="sxs-lookup"><span data-stu-id="38e3c-125">**Type**</span></span>|<span data-ttu-id="38e3c-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="38e3c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38e3c-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="38e3c-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="38e3c-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="38e3c-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="38e3c-129">図面内のコメントの作成者を識別するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="38e3c-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="38e3c-130">属性</span><span class="sxs-lookup"><span data-stu-id="38e3c-130">Attributes</span></span>

<span data-ttu-id="38e3c-131">なし。</span><span class="sxs-lookup"><span data-stu-id="38e3c-131">None.</span></span>
  

