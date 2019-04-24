---
title: authorentry 要素 (AuthorList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するために使用するプロパティを指定します。
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338627"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="78b30-103">authorentry 要素 (AuthorList_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="78b30-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="78b30-104">図面内のコメントの作成者を識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="78b30-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78b30-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="78b30-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78b30-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="78b30-106">**Element type**</span></span> <br/> |[<span data-ttu-id="78b30-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="78b30-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="78b30-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="78b30-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="78b30-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="78b30-109">**Schema file**</span></span> <br/> |<span data-ttu-id="78b30-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="78b30-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="78b30-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="78b30-111">**Document parts**</span></span> <br/> |<span data-ttu-id="78b30-112">comments</span><span class="sxs-lookup"><span data-stu-id="78b30-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="78b30-113">定義</span><span class="sxs-lookup"><span data-stu-id="78b30-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="78b30-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="78b30-114">Elements and attributes</span></span>

<span data-ttu-id="78b30-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="78b30-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="78b30-116">親要素</span><span class="sxs-lookup"><span data-stu-id="78b30-116">Parent elements</span></span>

|<span data-ttu-id="78b30-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="78b30-117">**Element**</span></span>|<span data-ttu-id="78b30-118">**型**</span><span class="sxs-lookup"><span data-stu-id="78b30-118">**Type**</span></span>|<span data-ttu-id="78b30-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="78b30-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="78b30-120">authorlist</span><span class="sxs-lookup"><span data-stu-id="78b30-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="78b30-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="78b30-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="78b30-122">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="78b30-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="78b30-123">子要素</span><span class="sxs-lookup"><span data-stu-id="78b30-123">Child elements</span></span>

<span data-ttu-id="78b30-124">なし。</span><span class="sxs-lookup"><span data-stu-id="78b30-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78b30-125">属性</span><span class="sxs-lookup"><span data-stu-id="78b30-125">Attributes</span></span>

|<span data-ttu-id="78b30-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="78b30-126">**Attribute**</span></span>|<span data-ttu-id="78b30-127">**型**</span><span class="sxs-lookup"><span data-stu-id="78b30-127">**Type**</span></span>|<span data-ttu-id="78b30-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="78b30-128">**Required**</span></span>|<span data-ttu-id="78b30-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="78b30-129">**Description**</span></span>|<span data-ttu-id="78b30-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="78b30-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="78b30-131">ID</span><span class="sxs-lookup"><span data-stu-id="78b30-131">ID</span></span>  <br/> |<span data-ttu-id="78b30-132">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="78b30-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="78b30-133">必須</span><span class="sxs-lookup"><span data-stu-id="78b30-133">required</span></span>  <br/> |<span data-ttu-id="78b30-134">作成者を識別する1から始まる値。</span><span class="sxs-lookup"><span data-stu-id="78b30-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="78b30-135">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="78b30-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="78b30-136">イニシャル</span><span class="sxs-lookup"><span data-stu-id="78b30-136">Initials</span></span>  <br/> |<span data-ttu-id="78b30-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="78b30-137">xsd:string</span></span>  <br/> |<span data-ttu-id="78b30-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="78b30-138">optional</span></span>  <br/> |<span data-ttu-id="78b30-139">作成者のイニシャル。</span><span class="sxs-lookup"><span data-stu-id="78b30-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="78b30-140">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="78b30-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="78b30-141">名前</span><span class="sxs-lookup"><span data-stu-id="78b30-141">Name</span></span>  <br/> |<span data-ttu-id="78b30-142">xsd: string</span><span class="sxs-lookup"><span data-stu-id="78b30-142">xsd:string</span></span>  <br/> |<span data-ttu-id="78b30-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="78b30-143">optional</span></span>  <br/> |<span data-ttu-id="78b30-144">作成者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="78b30-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="78b30-145">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="78b30-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="78b30-146">解決 id</span><span class="sxs-lookup"><span data-stu-id="78b30-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="78b30-147">xsd: string</span><span class="sxs-lookup"><span data-stu-id="78b30-147">xsd:string</span></span>  <br/> |<span data-ttu-id="78b30-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="78b30-148">optional</span></span>  <br/> |<span data-ttu-id="78b30-149">作成者の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="78b30-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="78b30-150">xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="78b30-150">Values of the xsd:string type.</span></span>  <br/> |
   

