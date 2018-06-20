---
title: テキスト要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: 図形のテキストが含まれています。
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806613"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="10ae8-103">テキスト要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="10ae8-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="10ae8-104">図形のテキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="10ae8-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10ae8-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="10ae8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10ae8-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="10ae8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="10ae8-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="10ae8-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="10ae8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="10ae8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="10ae8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="10ae8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="10ae8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="10ae8-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="10ae8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="10ae8-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="10ae8-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10ae8-113">定義</span><span class="sxs-lookup"><span data-stu-id="10ae8-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10ae8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="10ae8-114">Elements and attributes</span></span>

<span data-ttu-id="10ae8-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10ae8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="10ae8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="10ae8-116">Parent elements</span></span>

|<span data-ttu-id="10ae8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="10ae8-117">**Element**</span></span>|<span data-ttu-id="10ae8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="10ae8-118">**Type**</span></span>|<span data-ttu-id="10ae8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="10ae8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10ae8-120">Shape</span><span class="sxs-lookup"><span data-stu-id="10ae8-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10ae8-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10ae8-122">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="10ae8-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="10ae8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="10ae8-123">Child elements</span></span>

|<span data-ttu-id="10ae8-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="10ae8-124">**Element**</span></span>|<span data-ttu-id="10ae8-125">**型**</span><span class="sxs-lookup"><span data-stu-id="10ae8-125">**Type**</span></span>|<span data-ttu-id="10ae8-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="10ae8-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10ae8-127">cp</span><span class="sxs-lookup"><span data-stu-id="10ae8-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10ae8-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10ae8-129">文字プロパティの最初の実行されているマークは、対応する Char 要素に従って書式設定されました。</span><span class="sxs-lookup"><span data-stu-id="10ae8-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="10ae8-130">フォルダー</span><span class="sxs-lookup"><span data-stu-id="10ae8-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10ae8-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10ae8-132">対応するフィールド要素のテキスト フィールドのテキスト挿入点を示します。</span><span class="sxs-lookup"><span data-stu-id="10ae8-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="10ae8-133">pp</span><span class="sxs-lookup"><span data-stu-id="10ae8-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10ae8-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10ae8-135">段落のプロパティの最初の実行を指定します。</span><span class="sxs-lookup"><span data-stu-id="10ae8-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="10ae8-136">tp</span><span class="sxs-lookup"><span data-stu-id="10ae8-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10ae8-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="10ae8-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10ae8-138">実行タブのプロパティの先頭を指定します。</span><span class="sxs-lookup"><span data-stu-id="10ae8-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="10ae8-139">属性</span><span class="sxs-lookup"><span data-stu-id="10ae8-139">Attributes</span></span>

<span data-ttu-id="10ae8-140">なし。</span><span class="sxs-lookup"><span data-stu-id="10ae8-140">None.</span></span>
  

