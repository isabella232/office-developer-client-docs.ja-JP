---
title: AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するためのプロパティを指定します。
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804789"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="3b071-103">AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="3b071-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3b071-104">図面内のコメントの作成者を識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3b071-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b071-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3b071-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b071-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="3b071-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3b071-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3b071-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3b071-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="3b071-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3b071-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3b071-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3b071-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3b071-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3b071-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3b071-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3b071-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="3b071-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b071-113">定義</span><span class="sxs-lookup"><span data-stu-id="3b071-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3b071-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3b071-114">Elements and attributes</span></span>

<span data-ttu-id="3b071-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b071-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3b071-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3b071-116">Parent elements</span></span>

|<span data-ttu-id="3b071-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3b071-117">**Element**</span></span>|<span data-ttu-id="3b071-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3b071-118">**Type**</span></span>|<span data-ttu-id="3b071-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b071-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b071-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="3b071-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b071-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="3b071-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b071-122">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b071-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3b071-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3b071-123">Child elements</span></span>

<span data-ttu-id="3b071-124">なし。</span><span class="sxs-lookup"><span data-stu-id="3b071-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b071-125">属性</span><span class="sxs-lookup"><span data-stu-id="3b071-125">Attributes</span></span>

|<span data-ttu-id="3b071-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="3b071-126">**Attribute**</span></span>|<span data-ttu-id="3b071-127">**型**</span><span class="sxs-lookup"><span data-stu-id="3b071-127">**Type**</span></span>|<span data-ttu-id="3b071-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="3b071-128">**Required**</span></span>|<span data-ttu-id="3b071-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b071-129">**Description**</span></span>|<span data-ttu-id="3b071-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="3b071-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b071-131">ID</span><span class="sxs-lookup"><span data-stu-id="3b071-131">ID</span></span>  <br/> |<span data-ttu-id="3b071-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3b071-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3b071-133">必須</span><span class="sxs-lookup"><span data-stu-id="3b071-133">required</span></span>  <br/> |<span data-ttu-id="3b071-134">作成者を識別する 1 から始まる値です。</span><span class="sxs-lookup"><span data-stu-id="3b071-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="3b071-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b071-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3b071-136">Initials</span><span class="sxs-lookup"><span data-stu-id="3b071-136">Initials</span></span>  <br/> |<span data-ttu-id="3b071-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3b071-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3b071-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="3b071-138">optional</span></span>  <br/> |<span data-ttu-id="3b071-139">作成者のイニシャルです。</span><span class="sxs-lookup"><span data-stu-id="3b071-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="3b071-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b071-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b071-141">名前</span><span class="sxs-lookup"><span data-stu-id="3b071-141">Name</span></span>  <br/> |<span data-ttu-id="3b071-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3b071-142">xsd:string</span></span>  <br/> |<span data-ttu-id="3b071-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="3b071-143">optional</span></span>  <br/> |<span data-ttu-id="3b071-144">作成者の名前。</span><span class="sxs-lookup"><span data-stu-id="3b071-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="3b071-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b071-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3b071-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="3b071-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="3b071-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3b071-147">xsd:string</span></span>  <br/> |<span data-ttu-id="3b071-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="3b071-148">optional</span></span>  <br/> |<span data-ttu-id="3b071-149">作成者の一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="3b071-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="3b071-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b071-150">Values of the xsd:string type.</span></span>  <br/> |
   

