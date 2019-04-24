---
title: Text 要素 (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: 図形のテキストを格納します。
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332372"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="1779f-103">Text 要素 (ShapeSheet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1779f-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1779f-104">図形のテキストを格納します。</span><span class="sxs-lookup"><span data-stu-id="1779f-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1779f-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1779f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1779f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1779f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1779f-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1779f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1779f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1779f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1779f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1779f-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="1779f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1779f-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1779f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1779f-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="1779f-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1779f-113">定義</span><span class="sxs-lookup"><span data-stu-id="1779f-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1779f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1779f-114">Elements and attributes</span></span>

<span data-ttu-id="1779f-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1779f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1779f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1779f-116">Parent elements</span></span>

|<span data-ttu-id="1779f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1779f-117">**Element**</span></span>|<span data-ttu-id="1779f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1779f-118">**Type**</span></span>|<span data-ttu-id="1779f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1779f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1779f-120">Shape</span><span class="sxs-lookup"><span data-stu-id="1779f-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1779f-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1779f-122">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1779f-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1779f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1779f-123">Child elements</span></span>

|<span data-ttu-id="1779f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1779f-124">**Element**</span></span>|<span data-ttu-id="1779f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1779f-125">**Type**</span></span>|<span data-ttu-id="1779f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1779f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1779f-127">cp</span><span class="sxs-lookup"><span data-stu-id="1779f-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1779f-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1779f-129">対応する Char 要素に従って書式設定された、文字プロパティの実行の開始をマークします。</span><span class="sxs-lookup"><span data-stu-id="1779f-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="1779f-130">fld</span><span class="sxs-lookup"><span data-stu-id="1779f-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1779f-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1779f-132">対応する field 要素のテキストフィールドの挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="1779f-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="1779f-133">pptp</span><span class="sxs-lookup"><span data-stu-id="1779f-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1779f-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1779f-135">段落のプロパティを実行する開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="1779f-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="1779f-136">tp</span><span class="sxs-lookup"><span data-stu-id="1779f-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1779f-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="1779f-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1779f-138">tabs プロパティの実行開始を指定します。</span><span class="sxs-lookup"><span data-stu-id="1779f-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1779f-139">属性</span><span class="sxs-lookup"><span data-stu-id="1779f-139">Attributes</span></span>

<span data-ttu-id="1779f-140">なし。</span><span class="sxs-lookup"><span data-stu-id="1779f-140">None.</span></span>
  

