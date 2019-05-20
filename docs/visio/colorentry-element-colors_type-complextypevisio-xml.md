---
title: ColorEntry 要素 (Colors_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: カラー テーブル エントリが含まれます。
ms.openlocfilehash: 14ef92069ce8d963ce4a0770324843321804c5cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358087"
---
# <a name="colorentry-element-colorstype-complextype-visio-xml"></a><span data-ttu-id="94f74-103">ColorEntry 要素 (Colors_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="94f74-103">ColorEntry element (Colors_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="94f74-104">カラー テーブル エントリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="94f74-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94f74-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="94f74-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94f74-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="94f74-106">**Element type**</span></span> <br/> |[<span data-ttu-id="94f74-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="94f74-107">ColorEntry_Type complexType</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="94f74-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="94f74-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="94f74-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="94f74-109">**Schema file**</span></span> <br/> |<span data-ttu-id="94f74-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="94f74-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="94f74-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="94f74-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="94f74-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="94f74-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="94f74-113">定義</span><span class="sxs-lookup"><span data-stu-id="94f74-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="94f74-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="94f74-114">Elements and attributes</span></span>

<span data-ttu-id="94f74-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="94f74-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="94f74-116">親要素</span><span class="sxs-lookup"><span data-stu-id="94f74-116">Parent elements</span></span>

|<span data-ttu-id="94f74-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="94f74-117">**Element**</span></span>|<span data-ttu-id="94f74-118">**型**</span><span class="sxs-lookup"><span data-stu-id="94f74-118">**Type**</span></span>|<span data-ttu-id="94f74-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="94f74-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="94f74-120">色</span><span class="sxs-lookup"><span data-stu-id="94f74-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="94f74-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="94f74-121">Colors_Type complexType</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="94f74-122">ドキュメントのカラーテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="94f74-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="94f74-123">子要素</span><span class="sxs-lookup"><span data-stu-id="94f74-123">Child elements</span></span>

<span data-ttu-id="94f74-124">なし。</span><span class="sxs-lookup"><span data-stu-id="94f74-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94f74-125">属性</span><span class="sxs-lookup"><span data-stu-id="94f74-125">Attributes</span></span>

|<span data-ttu-id="94f74-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="94f74-126">**Attribute**</span></span>|<span data-ttu-id="94f74-127">**型**</span><span class="sxs-lookup"><span data-stu-id="94f74-127">**Type**</span></span>|<span data-ttu-id="94f74-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="94f74-128">**Required**</span></span>|<span data-ttu-id="94f74-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="94f74-129">**Description**</span></span>|<span data-ttu-id="94f74-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="94f74-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="94f74-131">IX</span><span class="sxs-lookup"><span data-stu-id="94f74-131">IX</span></span>  <br/> |<span data-ttu-id="94f74-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="94f74-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="94f74-133">必須</span><span class="sxs-lookup"><span data-stu-id="94f74-133">required</span></span>  <br/> |<span data-ttu-id="94f74-134">親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="94f74-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="94f74-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="94f74-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="94f74-136">RGB</span><span class="sxs-lookup"><span data-stu-id="94f74-136">RGB</span></span>  <br/> |<span data-ttu-id="94f74-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="94f74-137">xsd:string</span></span>  <br/> |<span data-ttu-id="94f74-138">必須</span><span class="sxs-lookup"><span data-stu-id="94f74-138">required</span></span>  <br/> |<span data-ttu-id="94f74-139">カラー テーブル エントリの 16 進値。</span><span class="sxs-lookup"><span data-stu-id="94f74-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="94f74-140">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="94f74-140">Values of the xsd:string type.</span></span>  <br/> |
   

