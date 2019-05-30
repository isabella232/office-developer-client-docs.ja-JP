---
title: Text 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: 図形のテキストを格納します。
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541926"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="4937e-103">Text 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4937e-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4937e-104">図形のテキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="4937e-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4937e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4937e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4937e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4937e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4937e-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4937e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4937e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4937e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4937e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4937e-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4937e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4937e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4937e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4937e-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="4937e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4937e-113">定義</span><span class="sxs-lookup"><span data-stu-id="4937e-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4937e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4937e-114">Elements and attributes</span></span>

<span data-ttu-id="4937e-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4937e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4937e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4937e-116">Parent elements</span></span>

|<span data-ttu-id="4937e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4937e-117">**Element**</span></span>|<span data-ttu-id="4937e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4937e-118">**Type**</span></span>|<span data-ttu-id="4937e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4937e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4937e-120">Shape</span><span class="sxs-lookup"><span data-stu-id="4937e-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4937e-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4937e-122">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4937e-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4937e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4937e-123">Child elements</span></span>

|<span data-ttu-id="4937e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="4937e-124">**Element**</span></span>|<span data-ttu-id="4937e-125">**型**</span><span class="sxs-lookup"><span data-stu-id="4937e-125">**Type**</span></span>|<span data-ttu-id="4937e-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="4937e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4937e-127">cp</span><span class="sxs-lookup"><span data-stu-id="4937e-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4937e-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4937e-129">対応する Char 要素に従って書式設定された、文字プロパティの実行の開始をマークします。</span><span class="sxs-lookup"><span data-stu-id="4937e-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="4937e-130">fld</span><span class="sxs-lookup"><span data-stu-id="4937e-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4937e-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4937e-132">対応する Field 要素のテキストフィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="4937e-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="4937e-133">pptp</span><span class="sxs-lookup"><span data-stu-id="4937e-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4937e-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4937e-135">段落のプロパティを実行する開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="4937e-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="4937e-136">tp</span><span class="sxs-lookup"><span data-stu-id="4937e-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4937e-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="4937e-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4937e-138">Tabs プロパティの実行開始を指定します。</span><span class="sxs-lookup"><span data-stu-id="4937e-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4937e-139">属性</span><span class="sxs-lookup"><span data-stu-id="4937e-139">Attributes</span></span>

<span data-ttu-id="4937e-140">なし。</span><span class="sxs-lookup"><span data-stu-id="4937e-140">None.</span></span>
  

