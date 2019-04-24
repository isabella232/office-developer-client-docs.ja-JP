---
title: Shapes 要素 (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Shape 要素のコレクションを格納します。
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348252"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="dc524-103">Shapes 要素 (ShapeSheet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="dc524-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="dc524-104">Shape 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="dc524-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc524-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="dc524-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc524-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="dc524-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dc524-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="dc524-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dc524-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc524-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dc524-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="dc524-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dc524-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="dc524-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dc524-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="dc524-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dc524-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="dc524-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc524-113">定義</span><span class="sxs-lookup"><span data-stu-id="dc524-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc524-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="dc524-114">Elements and attributes</span></span>

<span data-ttu-id="dc524-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc524-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dc524-116">親要素</span><span class="sxs-lookup"><span data-stu-id="dc524-116">Parent elements</span></span>

|<span data-ttu-id="dc524-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="dc524-117">**Element**</span></span>|<span data-ttu-id="dc524-118">**型**</span><span class="sxs-lookup"><span data-stu-id="dc524-118">**Type**</span></span>|<span data-ttu-id="dc524-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="dc524-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dc524-120">Shape</span><span class="sxs-lookup"><span data-stu-id="dc524-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dc524-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="dc524-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dc524-122">図形に関連付けられたプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="dc524-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dc524-123">子要素</span><span class="sxs-lookup"><span data-stu-id="dc524-123">Child elements</span></span>

|<span data-ttu-id="dc524-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc524-124">**Element**</span></span>|<span data-ttu-id="dc524-125">**型**</span><span class="sxs-lookup"><span data-stu-id="dc524-125">**Type**</span></span>|<span data-ttu-id="dc524-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="dc524-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dc524-127">Shape</span><span class="sxs-lookup"><span data-stu-id="dc524-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dc524-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="dc524-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dc524-129">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc524-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dc524-130">属性</span><span class="sxs-lookup"><span data-stu-id="dc524-130">Attributes</span></span>

<span data-ttu-id="dc524-131">なし。</span><span class="sxs-lookup"><span data-stu-id="dc524-131">None.</span></span>
  

