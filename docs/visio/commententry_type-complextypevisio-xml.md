---
title: CommentEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334945"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="77ed5-102">CommentEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="77ed5-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="77ed5-103">型情報</span><span class="sxs-lookup"><span data-stu-id="77ed5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77ed5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="77ed5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="77ed5-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="77ed5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="77ed5-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="77ed5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="77ed5-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="77ed5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="77ed5-108">xsd: string</span><span class="sxs-lookup"><span data-stu-id="77ed5-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77ed5-109">定義</span><span class="sxs-lookup"><span data-stu-id="77ed5-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="77ed5-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="77ed5-110">Elements and attributes</span></span>

<span data-ttu-id="77ed5-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77ed5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="77ed5-112">子要素</span><span class="sxs-lookup"><span data-stu-id="77ed5-112">Child elements</span></span>

<span data-ttu-id="77ed5-113">なし。</span><span class="sxs-lookup"><span data-stu-id="77ed5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77ed5-114">属性</span><span class="sxs-lookup"><span data-stu-id="77ed5-114">Attributes</span></span>

|<span data-ttu-id="77ed5-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="77ed5-115">**Attribute**</span></span>|<span data-ttu-id="77ed5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="77ed5-116">**Type**</span></span>|<span data-ttu-id="77ed5-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="77ed5-117">**Required**</span></span>|<span data-ttu-id="77ed5-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="77ed5-118">**Description**</span></span>|<span data-ttu-id="77ed5-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="77ed5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="77ed5-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="77ed5-120">AuthorID</span></span>  <br/> |<span data-ttu-id="77ed5-121">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="77ed5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77ed5-122">必須</span><span class="sxs-lookup"><span data-stu-id="77ed5-122">required</span></span>  <br/> ||<span data-ttu-id="77ed5-123">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-124">autoコメントの種類</span><span class="sxs-lookup"><span data-stu-id="77ed5-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="77ed5-125">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="77ed5-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77ed5-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="77ed5-126">optional</span></span>  <br/> ||<span data-ttu-id="77ed5-127">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="77ed5-128">CommentID</span></span>  <br/> |<span data-ttu-id="77ed5-129">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="77ed5-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77ed5-130">必須</span><span class="sxs-lookup"><span data-stu-id="77ed5-130">required</span></span>  <br/> ||<span data-ttu-id="77ed5-131">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-132">日付</span><span class="sxs-lookup"><span data-stu-id="77ed5-132">Date</span></span>  <br/> |<span data-ttu-id="77ed5-133">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="77ed5-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="77ed5-134">必須</span><span class="sxs-lookup"><span data-stu-id="77ed5-134">required</span></span>  <br/> ||<span data-ttu-id="77ed5-135">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-136">完了</span><span class="sxs-lookup"><span data-stu-id="77ed5-136">Done</span></span>  <br/> |<span data-ttu-id="77ed5-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="77ed5-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="77ed5-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="77ed5-138">optional</span></span>  <br/> ||<span data-ttu-id="77ed5-139">xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="77ed5-140">EditDate</span></span>  <br/> |<span data-ttu-id="77ed5-141">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="77ed5-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="77ed5-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="77ed5-142">optional</span></span>  <br/> ||<span data-ttu-id="77ed5-143">xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-144">PageID</span><span class="sxs-lookup"><span data-stu-id="77ed5-144">PageID</span></span>  <br/> |<span data-ttu-id="77ed5-145">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="77ed5-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77ed5-146">必須</span><span class="sxs-lookup"><span data-stu-id="77ed5-146">required</span></span>  <br/> ||<span data-ttu-id="77ed5-147">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="77ed5-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="77ed5-148">ShapeID</span></span>  <br/> |<span data-ttu-id="77ed5-149">xsd: アン signedint</span><span class="sxs-lookup"><span data-stu-id="77ed5-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="77ed5-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="77ed5-150">optional</span></span>  <br/> ||<span data-ttu-id="77ed5-151">xsd:/signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="77ed5-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

