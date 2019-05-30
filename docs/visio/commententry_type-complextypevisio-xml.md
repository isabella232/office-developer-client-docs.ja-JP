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
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="28c50-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="28c50-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="28c50-103">型情報</span><span class="sxs-lookup"><span data-stu-id="28c50-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28c50-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="28c50-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28c50-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="28c50-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28c50-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="28c50-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28c50-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="28c50-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28c50-108">xsd: string</span><span class="sxs-lookup"><span data-stu-id="28c50-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28c50-109">定義</span><span class="sxs-lookup"><span data-stu-id="28c50-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="28c50-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="28c50-110">Elements and attributes</span></span>

<span data-ttu-id="28c50-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="28c50-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28c50-112">子要素</span><span class="sxs-lookup"><span data-stu-id="28c50-112">Child elements</span></span>

<span data-ttu-id="28c50-113">なし。</span><span class="sxs-lookup"><span data-stu-id="28c50-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28c50-114">属性</span><span class="sxs-lookup"><span data-stu-id="28c50-114">Attributes</span></span>

|<span data-ttu-id="28c50-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="28c50-115">**Attribute**</span></span>|<span data-ttu-id="28c50-116">**型**</span><span class="sxs-lookup"><span data-stu-id="28c50-116">**Type**</span></span>|<span data-ttu-id="28c50-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="28c50-117">**Required**</span></span>|<span data-ttu-id="28c50-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="28c50-118">**Description**</span></span>|<span data-ttu-id="28c50-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="28c50-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="28c50-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="28c50-120">AuthorID</span></span>  <br/> |<span data-ttu-id="28c50-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="28c50-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28c50-122">必須</span><span class="sxs-lookup"><span data-stu-id="28c50-122">required</span></span>  <br/> ||<span data-ttu-id="28c50-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28c50-124">Autoコメントの種類</span><span class="sxs-lookup"><span data-stu-id="28c50-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="28c50-125">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="28c50-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28c50-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="28c50-126">optional</span></span>  <br/> ||<span data-ttu-id="28c50-127">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28c50-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="28c50-128">CommentID</span></span>  <br/> |<span data-ttu-id="28c50-129">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="28c50-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28c50-130">必須</span><span class="sxs-lookup"><span data-stu-id="28c50-130">required</span></span>  <br/> ||<span data-ttu-id="28c50-131">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28c50-132">日付</span><span class="sxs-lookup"><span data-stu-id="28c50-132">Date</span></span>  <br/> |<span data-ttu-id="28c50-133">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="28c50-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="28c50-134">必須</span><span class="sxs-lookup"><span data-stu-id="28c50-134">required</span></span>  <br/> ||<span data-ttu-id="28c50-135">Xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="28c50-136">完了</span><span class="sxs-lookup"><span data-stu-id="28c50-136">Done</span></span>  <br/> |<span data-ttu-id="28c50-137">xsd: boolean</span><span class="sxs-lookup"><span data-stu-id="28c50-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28c50-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="28c50-138">optional</span></span>  <br/> ||<span data-ttu-id="28c50-139">Xsd: boolean 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28c50-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="28c50-140">EditDate</span></span>  <br/> |<span data-ttu-id="28c50-141">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="28c50-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="28c50-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="28c50-142">optional</span></span>  <br/> ||<span data-ttu-id="28c50-143">Xsd: dateTime 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="28c50-144">PageID</span><span class="sxs-lookup"><span data-stu-id="28c50-144">PageID</span></span>  <br/> |<span data-ttu-id="28c50-145">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="28c50-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28c50-146">必須</span><span class="sxs-lookup"><span data-stu-id="28c50-146">required</span></span>  <br/> ||<span data-ttu-id="28c50-147">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28c50-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="28c50-148">ShapeID</span></span>  <br/> |<span data-ttu-id="28c50-149">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="28c50-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28c50-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="28c50-150">optional</span></span>  <br/> ||<span data-ttu-id="28c50-151">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="28c50-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

