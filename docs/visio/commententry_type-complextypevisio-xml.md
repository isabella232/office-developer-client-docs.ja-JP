---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540127"
---
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="65caa-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="65caa-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="65caa-103">型情報</span><span class="sxs-lookup"><span data-stu-id="65caa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65caa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65caa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65caa-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="65caa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65caa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65caa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65caa-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="65caa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65caa-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="65caa-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65caa-109">定義</span><span class="sxs-lookup"><span data-stu-id="65caa-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="65caa-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="65caa-110">Elements and attributes</span></span>

<span data-ttu-id="65caa-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65caa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65caa-112">子要素</span><span class="sxs-lookup"><span data-stu-id="65caa-112">Child elements</span></span>

<span data-ttu-id="65caa-113">なし。</span><span class="sxs-lookup"><span data-stu-id="65caa-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65caa-114">属性</span><span class="sxs-lookup"><span data-stu-id="65caa-114">Attributes</span></span>

|<span data-ttu-id="65caa-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="65caa-115">**Attribute**</span></span>|<span data-ttu-id="65caa-116">**型**</span><span class="sxs-lookup"><span data-stu-id="65caa-116">**Type**</span></span>|<span data-ttu-id="65caa-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="65caa-117">**Required**</span></span>|<span data-ttu-id="65caa-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="65caa-118">**Description**</span></span>|<span data-ttu-id="65caa-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="65caa-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65caa-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="65caa-120">AuthorID</span></span>  <br/> |<span data-ttu-id="65caa-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65caa-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65caa-122">必須</span><span class="sxs-lookup"><span data-stu-id="65caa-122">required</span></span>  <br/> ||<span data-ttu-id="65caa-123">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65caa-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="65caa-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="65caa-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65caa-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65caa-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="65caa-126">optional</span></span>  <br/> ||<span data-ttu-id="65caa-127">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65caa-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="65caa-128">CommentID</span></span>  <br/> |<span data-ttu-id="65caa-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65caa-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65caa-130">必須</span><span class="sxs-lookup"><span data-stu-id="65caa-130">required</span></span>  <br/> ||<span data-ttu-id="65caa-131">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65caa-132">日付</span><span class="sxs-lookup"><span data-stu-id="65caa-132">Date</span></span>  <br/> |<span data-ttu-id="65caa-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="65caa-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="65caa-134">必須</span><span class="sxs-lookup"><span data-stu-id="65caa-134">required</span></span>  <br/> ||<span data-ttu-id="65caa-135">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="65caa-136">完了</span><span class="sxs-lookup"><span data-stu-id="65caa-136">Done</span></span>  <br/> |<span data-ttu-id="65caa-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="65caa-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="65caa-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="65caa-138">optional</span></span>  <br/> ||<span data-ttu-id="65caa-139">xsd:boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="65caa-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="65caa-140">EditDate</span></span>  <br/> |<span data-ttu-id="65caa-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="65caa-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="65caa-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="65caa-142">optional</span></span>  <br/> ||<span data-ttu-id="65caa-143">xsd:dateTime type 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="65caa-144">PageID</span><span class="sxs-lookup"><span data-stu-id="65caa-144">PageID</span></span>  <br/> |<span data-ttu-id="65caa-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65caa-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65caa-146">必須</span><span class="sxs-lookup"><span data-stu-id="65caa-146">required</span></span>  <br/> ||<span data-ttu-id="65caa-147">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65caa-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="65caa-148">ShapeID</span></span>  <br/> |<span data-ttu-id="65caa-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65caa-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65caa-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="65caa-150">optional</span></span>  <br/> ||<span data-ttu-id="65caa-151">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="65caa-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

