---
title: ColorEntry 要素 (Colors_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: カラー テーブル エントリが含まれます。
ms.openlocfilehash: f2221d8d32823e5eec4a100eaf4e8f62b914df28
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540183"
---
# <a name="colorentry-element-colors_type-complextype-visio-xml"></a><span data-ttu-id="2cf64-103">ColorEntry 要素 (Colors_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2cf64-103">ColorEntry element (Colors_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="2cf64-104">カラー テーブル エントリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2cf64-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2cf64-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="2cf64-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cf64-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="2cf64-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2cf64-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2cf64-107">ColorEntry_Type complexType</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2cf64-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2cf64-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2cf64-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2cf64-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2cf64-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2cf64-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2cf64-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="2cf64-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="2cf64-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="2cf64-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2cf64-113">定義</span><span class="sxs-lookup"><span data-stu-id="2cf64-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2cf64-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2cf64-114">Elements and attributes</span></span>

<span data-ttu-id="2cf64-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cf64-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2cf64-116">親要素</span><span class="sxs-lookup"><span data-stu-id="2cf64-116">Parent elements</span></span>

|<span data-ttu-id="2cf64-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="2cf64-117">**Element**</span></span>|<span data-ttu-id="2cf64-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2cf64-118">**Type**</span></span>|<span data-ttu-id="2cf64-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="2cf64-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2cf64-120">色</span><span class="sxs-lookup"><span data-stu-id="2cf64-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2cf64-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="2cf64-121">Colors_Type complexType</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2cf64-122">ドキュメントのカラーテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2cf64-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2cf64-123">子要素</span><span class="sxs-lookup"><span data-stu-id="2cf64-123">Child elements</span></span>

<span data-ttu-id="2cf64-124">なし。</span><span class="sxs-lookup"><span data-stu-id="2cf64-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2cf64-125">属性</span><span class="sxs-lookup"><span data-stu-id="2cf64-125">Attributes</span></span>

|<span data-ttu-id="2cf64-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="2cf64-126">**Attribute**</span></span>|<span data-ttu-id="2cf64-127">**型**</span><span class="sxs-lookup"><span data-stu-id="2cf64-127">**Type**</span></span>|<span data-ttu-id="2cf64-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="2cf64-128">**Required**</span></span>|<span data-ttu-id="2cf64-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="2cf64-129">**Description**</span></span>|<span data-ttu-id="2cf64-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="2cf64-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2cf64-131">IX</span><span class="sxs-lookup"><span data-stu-id="2cf64-131">IX</span></span>  <br/> |<span data-ttu-id="2cf64-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2cf64-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2cf64-133">必須</span><span class="sxs-lookup"><span data-stu-id="2cf64-133">required</span></span>  <br/> |<span data-ttu-id="2cf64-134">親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="2cf64-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="2cf64-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="2cf64-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2cf64-136">RGB</span><span class="sxs-lookup"><span data-stu-id="2cf64-136">RGB</span></span>  <br/> |<span data-ttu-id="2cf64-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="2cf64-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2cf64-138">必須</span><span class="sxs-lookup"><span data-stu-id="2cf64-138">required</span></span>  <br/> |<span data-ttu-id="2cf64-139">カラー テーブル エントリの 16 進値。</span><span class="sxs-lookup"><span data-stu-id="2cf64-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="2cf64-140">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="2cf64-140">Values of the xsd:string type.</span></span>  <br/> |
   

