---
title: Text 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: 図形のテキストが含まれます。
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541926"
---
# <a name="text-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="0ce3e-103">Text 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0ce3e-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0ce3e-104">図形のテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ce3e-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="0ce3e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ce3e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0ce3e-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0ce3e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0ce3e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0ce3e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0ce3e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0ce3e-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0ce3e-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="0ce3e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ce3e-113">定義</span><span class="sxs-lookup"><span data-stu-id="0ce3e-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ce3e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0ce3e-114">Elements and attributes</span></span>

<span data-ttu-id="0ce3e-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0ce3e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0ce3e-116">Parent elements</span></span>

|<span data-ttu-id="0ce3e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-117">**Element**</span></span>|<span data-ttu-id="0ce3e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-118">**Type**</span></span>|<span data-ttu-id="0ce3e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ce3e-120">Shape</span><span class="sxs-lookup"><span data-stu-id="0ce3e-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce3e-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce3e-122">**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ce3e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="0ce3e-123">Child elements</span></span>

|<span data-ttu-id="0ce3e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-124">**Element**</span></span>|<span data-ttu-id="0ce3e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-125">**Type**</span></span>|<span data-ttu-id="0ce3e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="0ce3e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ce3e-127">cp</span><span class="sxs-lookup"><span data-stu-id="0ce3e-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce3e-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce3e-129">対応する Char 要素に従って書式設定された文字プロパティ実行の開始位置を示します。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="0ce3e-130">fld</span><span class="sxs-lookup"><span data-stu-id="0ce3e-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce3e-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce3e-132">対応するフィールド要素のテキスト フィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="0ce3e-133">pp</span><span class="sxs-lookup"><span data-stu-id="0ce3e-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce3e-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce3e-135">段落プロパティの実行の開始を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="0ce3e-136">tp</span><span class="sxs-lookup"><span data-stu-id="0ce3e-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ce3e-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="0ce3e-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ce3e-138">実行するタブ プロパティの先頭を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0ce3e-139">属性</span><span class="sxs-lookup"><span data-stu-id="0ce3e-139">Attributes</span></span>

<span data-ttu-id="0ce3e-140">なし。</span><span class="sxs-lookup"><span data-stu-id="0ce3e-140">None.</span></span>
  

