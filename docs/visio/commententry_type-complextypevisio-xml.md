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
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="6018e-102">CommentEntry_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="6018e-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6018e-103">型情報</span><span class="sxs-lookup"><span data-stu-id="6018e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6018e-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6018e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6018e-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6018e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6018e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6018e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6018e-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="6018e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6018e-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6018e-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6018e-109">定義</span><span class="sxs-lookup"><span data-stu-id="6018e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6018e-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6018e-110">Elements and attributes</span></span>

<span data-ttu-id="6018e-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6018e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6018e-112">子要素</span><span class="sxs-lookup"><span data-stu-id="6018e-112">Child elements</span></span>

<span data-ttu-id="6018e-113">なし。</span><span class="sxs-lookup"><span data-stu-id="6018e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6018e-114">属性</span><span class="sxs-lookup"><span data-stu-id="6018e-114">Attributes</span></span>

|<span data-ttu-id="6018e-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="6018e-115">**Attribute**</span></span>|<span data-ttu-id="6018e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6018e-116">**Type**</span></span>|<span data-ttu-id="6018e-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="6018e-117">**Required**</span></span>|<span data-ttu-id="6018e-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="6018e-118">**Description**</span></span>|<span data-ttu-id="6018e-119">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6018e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6018e-120">著者 Id</span><span class="sxs-lookup"><span data-stu-id="6018e-120">AuthorID</span></span>  <br/> |<span data-ttu-id="6018e-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6018e-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6018e-122">必須</span><span class="sxs-lookup"><span data-stu-id="6018e-122">required</span></span>  <br/> ||<span data-ttu-id="6018e-123">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6018e-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="6018e-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="6018e-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6018e-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6018e-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="6018e-126">optional</span></span>  <br/> ||<span data-ttu-id="6018e-127">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6018e-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="6018e-128">CommentID</span></span>  <br/> |<span data-ttu-id="6018e-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6018e-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6018e-130">必須</span><span class="sxs-lookup"><span data-stu-id="6018e-130">required</span></span>  <br/> ||<span data-ttu-id="6018e-131">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6018e-132">Date</span><span class="sxs-lookup"><span data-stu-id="6018e-132">Date</span></span>  <br/> |<span data-ttu-id="6018e-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="6018e-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="6018e-134">必須</span><span class="sxs-lookup"><span data-stu-id="6018e-134">required</span></span>  <br/> ||<span data-ttu-id="6018e-135">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="6018e-136">終了</span><span class="sxs-lookup"><span data-stu-id="6018e-136">Done</span></span>  <br/> |<span data-ttu-id="6018e-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6018e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6018e-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="6018e-138">optional</span></span>  <br/> ||<span data-ttu-id="6018e-139">Xsd:boolean の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6018e-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="6018e-140">EditDate</span></span>  <br/> |<span data-ttu-id="6018e-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="6018e-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="6018e-142">省略可能</span><span class="sxs-lookup"><span data-stu-id="6018e-142">optional</span></span>  <br/> ||<span data-ttu-id="6018e-143">Xsd:dateTime の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="6018e-144">PageID</span><span class="sxs-lookup"><span data-stu-id="6018e-144">PageID</span></span>  <br/> |<span data-ttu-id="6018e-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6018e-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6018e-146">必須</span><span class="sxs-lookup"><span data-stu-id="6018e-146">required</span></span>  <br/> ||<span data-ttu-id="6018e-147">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6018e-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="6018e-148">ShapeID</span></span>  <br/> |<span data-ttu-id="6018e-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6018e-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6018e-150">省略可能</span><span class="sxs-lookup"><span data-stu-id="6018e-150">optional</span></span>  <br/> ||<span data-ttu-id="6018e-151">Xsd:unsignedInt の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6018e-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

