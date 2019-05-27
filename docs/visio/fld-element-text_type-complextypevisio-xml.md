---
title: fld 要素 (Text_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: 対応するフィールド要素のテキストフィールドの挿入ポイントを示します。
ms.openlocfilehash: a7303697a9471dab68f5b1cf851f60d51650a84e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346215"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="dd1f9-103">fld 要素 (Text_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="dd1f9-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dd1f9-104">対応する**Field** 要素のテキストフィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="dd1f9-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="dd1f9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd1f9-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dd1f9-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="dd1f9-107">fld_Type complexType</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dd1f9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dd1f9-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dd1f9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dd1f9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dd1f9-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="dd1f9-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="dd1f9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dd1f9-113">定義</span><span class="sxs-lookup"><span data-stu-id="dd1f9-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dd1f9-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dd1f9-114">Elements and attributes</span></span>

<span data-ttu-id="dd1f9-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dd1f9-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dd1f9-116">Parent elements</span></span>

|<span data-ttu-id="dd1f9-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-117">**Element**</span></span>|<span data-ttu-id="dd1f9-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-118">**Type**</span></span>|<span data-ttu-id="dd1f9-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dd1f9-120">Text</span><span class="sxs-lookup"><span data-stu-id="dd1f9-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dd1f9-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="dd1f9-121">textType</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dd1f9-122">図形のテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dd1f9-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dd1f9-123">Child elements</span></span>

<span data-ttu-id="dd1f9-124">なし。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd1f9-125">属性</span><span class="sxs-lookup"><span data-stu-id="dd1f9-125">Attributes</span></span>

|<span data-ttu-id="dd1f9-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-126">**Attribute**</span></span>|<span data-ttu-id="dd1f9-127">**型**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-127">**Type**</span></span>|<span data-ttu-id="dd1f9-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-128">**Required**</span></span>|<span data-ttu-id="dd1f9-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-129">**Description**</span></span>|<span data-ttu-id="dd1f9-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="dd1f9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dd1f9-131">IX</span><span class="sxs-lookup"><span data-stu-id="dd1f9-131">IX</span></span>  <br/> |<span data-ttu-id="dd1f9-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dd1f9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dd1f9-133">必須</span><span class="sxs-lookup"><span data-stu-id="dd1f9-133">required</span></span>  <br/> |<span data-ttu-id="dd1f9-134">親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="dd1f9-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="dd1f9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

