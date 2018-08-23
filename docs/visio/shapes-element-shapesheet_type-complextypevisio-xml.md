---
title: 図形要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: 図形要素のコレクションが含まれています。
ms.openlocfilehash: d2e725a28873cac8dded49587a98400df1d9bf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806427"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="68fae-103">図形要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="68fae-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="68fae-104">図形要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="68fae-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68fae-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="68fae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68fae-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="68fae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68fae-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="68fae-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68fae-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="68fae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68fae-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="68fae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68fae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="68fae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68fae-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="68fae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68fae-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="68fae-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68fae-113">定義</span><span class="sxs-lookup"><span data-stu-id="68fae-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68fae-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="68fae-114">Elements and attributes</span></span>

<span data-ttu-id="68fae-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="68fae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68fae-116">親要素</span><span class="sxs-lookup"><span data-stu-id="68fae-116">Parent elements</span></span>

|<span data-ttu-id="68fae-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="68fae-117">**Element**</span></span>|<span data-ttu-id="68fae-118">**型**</span><span class="sxs-lookup"><span data-stu-id="68fae-118">**Type**</span></span>|<span data-ttu-id="68fae-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="68fae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68fae-120">Shape</span><span class="sxs-lookup"><span data-stu-id="68fae-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68fae-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="68fae-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68fae-122">図形に関連付けられているプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="68fae-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68fae-123">子要素</span><span class="sxs-lookup"><span data-stu-id="68fae-123">Child elements</span></span>

|<span data-ttu-id="68fae-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="68fae-124">**Element**</span></span>|<span data-ttu-id="68fae-125">**型**</span><span class="sxs-lookup"><span data-stu-id="68fae-125">**Type**</span></span>|<span data-ttu-id="68fae-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="68fae-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68fae-127">Shape</span><span class="sxs-lookup"><span data-stu-id="68fae-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68fae-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="68fae-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68fae-129">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="68fae-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68fae-130">属性</span><span class="sxs-lookup"><span data-stu-id="68fae-130">Attributes</span></span>

<span data-ttu-id="68fae-131">なし。</span><span class="sxs-lookup"><span data-stu-id="68fae-131">None.</span></span>
  

