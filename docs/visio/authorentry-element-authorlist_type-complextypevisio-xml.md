---
title: AuthorEntry 要素 (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するために使用するプロパティを指定します。
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537907"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="59d3b-103">AuthorEntry 要素 (AuthorList_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="59d3b-103">AuthorEntry element (AuthorList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="59d3b-104">図面内のコメントの作成者を識別するために使用するプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="59d3b-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59d3b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="59d3b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59d3b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="59d3b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59d3b-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="59d3b-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59d3b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="59d3b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59d3b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="59d3b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59d3b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="59d3b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59d3b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="59d3b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="59d3b-112">comments</span><span class="sxs-lookup"><span data-stu-id="59d3b-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59d3b-113">定義</span><span class="sxs-lookup"><span data-stu-id="59d3b-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59d3b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="59d3b-114">Elements and attributes</span></span>

<span data-ttu-id="59d3b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59d3b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59d3b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="59d3b-116">Parent elements</span></span>

|<span data-ttu-id="59d3b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="59d3b-117">**Element**</span></span>|<span data-ttu-id="59d3b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="59d3b-118">**Type**</span></span>|<span data-ttu-id="59d3b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="59d3b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59d3b-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="59d3b-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59d3b-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="59d3b-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59d3b-122">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="59d3b-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="59d3b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="59d3b-123">Child elements</span></span>

<span data-ttu-id="59d3b-124">なし。</span><span class="sxs-lookup"><span data-stu-id="59d3b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59d3b-125">属性</span><span class="sxs-lookup"><span data-stu-id="59d3b-125">Attributes</span></span>

|<span data-ttu-id="59d3b-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="59d3b-126">**Attribute**</span></span>|<span data-ttu-id="59d3b-127">**型**</span><span class="sxs-lookup"><span data-stu-id="59d3b-127">**Type**</span></span>|<span data-ttu-id="59d3b-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="59d3b-128">**Required**</span></span>|<span data-ttu-id="59d3b-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="59d3b-129">**Description**</span></span>|<span data-ttu-id="59d3b-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="59d3b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="59d3b-131">ID</span><span class="sxs-lookup"><span data-stu-id="59d3b-131">ID</span></span>  <br/> |<span data-ttu-id="59d3b-132">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="59d3b-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="59d3b-133">必須</span><span class="sxs-lookup"><span data-stu-id="59d3b-133">required</span></span>  <br/> |<span data-ttu-id="59d3b-134">作成者を識別する1から始まる値。</span><span class="sxs-lookup"><span data-stu-id="59d3b-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="59d3b-135">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="59d3b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="59d3b-136">イニシャル</span><span class="sxs-lookup"><span data-stu-id="59d3b-136">Initials</span></span>  <br/> |<span data-ttu-id="59d3b-137">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59d3b-137">xsd:string</span></span>  <br/> |<span data-ttu-id="59d3b-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="59d3b-138">optional</span></span>  <br/> |<span data-ttu-id="59d3b-139">作成者のイニシャル。</span><span class="sxs-lookup"><span data-stu-id="59d3b-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="59d3b-140">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59d3b-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59d3b-141">名前</span><span class="sxs-lookup"><span data-stu-id="59d3b-141">Name</span></span>  <br/> |<span data-ttu-id="59d3b-142">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59d3b-142">xsd:string</span></span>  <br/> |<span data-ttu-id="59d3b-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="59d3b-143">optional</span></span>  <br/> |<span data-ttu-id="59d3b-144">作成者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="59d3b-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="59d3b-145">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59d3b-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="59d3b-146">解決 Id</span><span class="sxs-lookup"><span data-stu-id="59d3b-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="59d3b-147">xsd: string</span><span class="sxs-lookup"><span data-stu-id="59d3b-147">xsd:string</span></span>  <br/> |<span data-ttu-id="59d3b-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="59d3b-148">optional</span></span>  <br/> |<span data-ttu-id="59d3b-149">作成者の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="59d3b-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="59d3b-150">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="59d3b-150">Values of the xsd:string type.</span></span>  <br/> |
   

