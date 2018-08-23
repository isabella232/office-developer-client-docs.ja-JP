---
title: CommentEntry_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805036"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="a45f2-102">CommentEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a45f2-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a45f2-103">型情報</span><span class="sxs-lookup"><span data-stu-id="a45f2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a45f2-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a45f2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a45f2-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a45f2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a45f2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a45f2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a45f2-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a45f2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a45f2-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a45f2-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a45f2-109">定義</span><span class="sxs-lookup"><span data-stu-id="a45f2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a45f2-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a45f2-110">Elements and attributes</span></span>

<span data-ttu-id="a45f2-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a45f2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a45f2-112">子要素</span><span class="sxs-lookup"><span data-stu-id="a45f2-112">Child elements</span></span>

<span data-ttu-id="a45f2-113">なし。</span><span class="sxs-lookup"><span data-stu-id="a45f2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a45f2-114">属性</span><span class="sxs-lookup"><span data-stu-id="a45f2-114">Attributes</span></span>

|<span data-ttu-id="a45f2-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="a45f2-115">**Attribute**</span></span>|<span data-ttu-id="a45f2-116">**型**</span><span class="sxs-lookup"><span data-stu-id="a45f2-116">**Type**</span></span>|<span data-ttu-id="a45f2-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="a45f2-117">**Required**</span></span>|<span data-ttu-id="a45f2-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="a45f2-118">**Description**</span></span>|<span data-ttu-id="a45f2-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a45f2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a45f2-120">著者 Id</span><span class="sxs-lookup"><span data-stu-id="a45f2-120">AuthorID</span></span>  <br/> |<span data-ttu-id="a45f2-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a45f2-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a45f2-122">必須</span><span class="sxs-lookup"><span data-stu-id="a45f2-122">required</span></span>  <br/> ||<span data-ttu-id="a45f2-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="a45f2-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="a45f2-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a45f2-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a45f2-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a45f2-126">optional</span></span>  <br/> ||<span data-ttu-id="a45f2-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="a45f2-128">CommentID</span></span>  <br/> |<span data-ttu-id="a45f2-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a45f2-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a45f2-130">必須</span><span class="sxs-lookup"><span data-stu-id="a45f2-130">required</span></span>  <br/> ||<span data-ttu-id="a45f2-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-132">日付</span><span class="sxs-lookup"><span data-stu-id="a45f2-132">Date</span></span>  <br/> |<span data-ttu-id="a45f2-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="a45f2-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="a45f2-134">必須</span><span class="sxs-lookup"><span data-stu-id="a45f2-134">required</span></span>  <br/> ||<span data-ttu-id="a45f2-135">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-136">終了</span><span class="sxs-lookup"><span data-stu-id="a45f2-136">Done</span></span>  <br/> |<span data-ttu-id="a45f2-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="a45f2-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a45f2-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a45f2-138">optional</span></span>  <br/> ||<span data-ttu-id="a45f2-139">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="a45f2-140">EditDate</span></span>  <br/> |<span data-ttu-id="a45f2-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="a45f2-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="a45f2-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="a45f2-142">optional</span></span>  <br/> ||<span data-ttu-id="a45f2-143">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-144">PageID</span><span class="sxs-lookup"><span data-stu-id="a45f2-144">PageID</span></span>  <br/> |<span data-ttu-id="a45f2-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a45f2-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a45f2-146">必須</span><span class="sxs-lookup"><span data-stu-id="a45f2-146">required</span></span>  <br/> ||<span data-ttu-id="a45f2-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a45f2-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="a45f2-148">ShapeID</span></span>  <br/> |<span data-ttu-id="a45f2-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a45f2-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a45f2-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="a45f2-150">optional</span></span>  <br/> ||<span data-ttu-id="a45f2-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a45f2-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

