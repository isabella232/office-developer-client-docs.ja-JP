---
title: AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: 図面内のコメントの作成者を識別するためのプロパティを指定します。
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386333"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="10076-103">AuthorEntry 要素 (AuthorList_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="10076-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="10076-104">図面内のコメントの作成者を識別するためのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="10076-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10076-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="10076-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10076-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="10076-106">**Element type**</span></span> <br/> |[<span data-ttu-id="10076-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="10076-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="10076-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="10076-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="10076-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="10076-109">**Schema file**</span></span> <br/> |<span data-ttu-id="10076-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="10076-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="10076-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="10076-111">**Document parts**</span></span> <br/> |<span data-ttu-id="10076-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="10076-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10076-113">定義</span><span class="sxs-lookup"><span data-stu-id="10076-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10076-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="10076-114">Elements and attributes</span></span>

<span data-ttu-id="10076-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10076-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="10076-116">親要素</span><span class="sxs-lookup"><span data-stu-id="10076-116">Parent elements</span></span>

|<span data-ttu-id="10076-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="10076-117">**Element**</span></span>|<span data-ttu-id="10076-118">**型**</span><span class="sxs-lookup"><span data-stu-id="10076-118">**Type**</span></span>|<span data-ttu-id="10076-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="10076-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10076-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="10076-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10076-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="10076-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10076-122">図面の作成者を指定します。</span><span class="sxs-lookup"><span data-stu-id="10076-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="10076-123">子要素</span><span class="sxs-lookup"><span data-stu-id="10076-123">Child elements</span></span>

<span data-ttu-id="10076-124">なし。</span><span class="sxs-lookup"><span data-stu-id="10076-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10076-125">属性</span><span class="sxs-lookup"><span data-stu-id="10076-125">Attributes</span></span>

|<span data-ttu-id="10076-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="10076-126">**Attribute**</span></span>|<span data-ttu-id="10076-127">**型**</span><span class="sxs-lookup"><span data-stu-id="10076-127">**Type**</span></span>|<span data-ttu-id="10076-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="10076-128">**Required**</span></span>|<span data-ttu-id="10076-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="10076-129">**Description**</span></span>|<span data-ttu-id="10076-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="10076-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10076-131">ID</span><span class="sxs-lookup"><span data-stu-id="10076-131">ID</span></span>  <br/> |<span data-ttu-id="10076-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="10076-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10076-133">必須</span><span class="sxs-lookup"><span data-stu-id="10076-133">required</span></span>  <br/> |<span data-ttu-id="10076-134">作成者を識別する 1 から始まる値です。</span><span class="sxs-lookup"><span data-stu-id="10076-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="10076-135">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10076-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="10076-136">Initials</span><span class="sxs-lookup"><span data-stu-id="10076-136">Initials</span></span>  <br/> |<span data-ttu-id="10076-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="10076-137">xsd:string</span></span>  <br/> |<span data-ttu-id="10076-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="10076-138">optional</span></span>  <br/> |<span data-ttu-id="10076-139">作成者のイニシャルです。</span><span class="sxs-lookup"><span data-stu-id="10076-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="10076-140">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10076-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10076-141">名前</span><span class="sxs-lookup"><span data-stu-id="10076-141">Name</span></span>  <br/> |<span data-ttu-id="10076-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="10076-142">xsd:string</span></span>  <br/> |<span data-ttu-id="10076-143">省略可能</span><span class="sxs-lookup"><span data-stu-id="10076-143">optional</span></span>  <br/> |<span data-ttu-id="10076-144">作成者の名前。</span><span class="sxs-lookup"><span data-stu-id="10076-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="10076-145">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10076-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="10076-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="10076-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="10076-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="10076-147">xsd:string</span></span>  <br/> |<span data-ttu-id="10076-148">省略可能</span><span class="sxs-lookup"><span data-stu-id="10076-148">optional</span></span>  <br/> |<span data-ttu-id="10076-149">作成者の一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="10076-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="10076-150">Xsd:string の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10076-150">Values of the xsd:string type.</span></span>  <br/> |
   

