---
title: fld 要素 (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: 対応するフィールド要素のテキスト フィールドの挿入ポイントを示します。
ms.openlocfilehash: efacb7ed11968dec5d5c2f62b0ca3e3bcd8580c0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539615"
---
# <a name="fld-element-text_type-complextype-visio-xml"></a><span data-ttu-id="98e29-103">fld 要素 (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="98e29-103">fld element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="98e29-104">対応する**フィールド** 要素のテキスト フィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="98e29-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="98e29-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="98e29-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98e29-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="98e29-106">**Element type**</span></span> <br/> |[<span data-ttu-id="98e29-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="98e29-107">fld_Type complexType</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="98e29-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="98e29-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="98e29-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="98e29-109">**Schema file**</span></span> <br/> |<span data-ttu-id="98e29-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="98e29-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="98e29-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="98e29-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="98e29-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="98e29-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98e29-113">定義</span><span class="sxs-lookup"><span data-stu-id="98e29-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="98e29-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="98e29-114">Elements and attributes</span></span>

<span data-ttu-id="98e29-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98e29-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="98e29-116">親要素</span><span class="sxs-lookup"><span data-stu-id="98e29-116">Parent elements</span></span>

|<span data-ttu-id="98e29-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="98e29-117">**Element**</span></span>|<span data-ttu-id="98e29-118">**型**</span><span class="sxs-lookup"><span data-stu-id="98e29-118">**Type**</span></span>|<span data-ttu-id="98e29-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="98e29-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98e29-120">Text</span><span class="sxs-lookup"><span data-stu-id="98e29-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="98e29-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="98e29-121">textType</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="98e29-122">図形のテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="98e29-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98e29-123">子要素</span><span class="sxs-lookup"><span data-stu-id="98e29-123">Child elements</span></span>

<span data-ttu-id="98e29-124">なし。</span><span class="sxs-lookup"><span data-stu-id="98e29-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98e29-125">属性</span><span class="sxs-lookup"><span data-stu-id="98e29-125">Attributes</span></span>

|<span data-ttu-id="98e29-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="98e29-126">**Attribute**</span></span>|<span data-ttu-id="98e29-127">**型**</span><span class="sxs-lookup"><span data-stu-id="98e29-127">**Type**</span></span>|<span data-ttu-id="98e29-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="98e29-128">**Required**</span></span>|<span data-ttu-id="98e29-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="98e29-129">**Description**</span></span>|<span data-ttu-id="98e29-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="98e29-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98e29-131">IX</span><span class="sxs-lookup"><span data-stu-id="98e29-131">IX</span></span>  <br/> |<span data-ttu-id="98e29-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="98e29-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="98e29-133">必須</span><span class="sxs-lookup"><span data-stu-id="98e29-133">required</span></span>  <br/> |<span data-ttu-id="98e29-134">親要素内の要素の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="98e29-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="98e29-135">xsd:unsignedInt 型の値。</span><span class="sxs-lookup"><span data-stu-id="98e29-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

