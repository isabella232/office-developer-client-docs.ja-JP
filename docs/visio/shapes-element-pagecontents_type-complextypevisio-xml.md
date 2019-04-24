---
title: Shapes 要素 (PageContents_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Shape 要素のコレクションを格納します。
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349169"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="a9293-103">Shapes 要素 (PageContents_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a9293-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a9293-104">Shape 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="a9293-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9293-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a9293-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9293-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a9293-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a9293-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="a9293-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a9293-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a9293-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a9293-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a9293-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a9293-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="a9293-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a9293-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a9293-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a9293-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="a9293-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a9293-113">定義</span><span class="sxs-lookup"><span data-stu-id="a9293-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a9293-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a9293-114">Elements and attributes</span></span>

<span data-ttu-id="a9293-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9293-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a9293-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a9293-116">Parent elements</span></span>

|<span data-ttu-id="a9293-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a9293-117">**Element**</span></span>|<span data-ttu-id="a9293-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a9293-118">**Type**</span></span>|<span data-ttu-id="a9293-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a9293-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a9293-120">mastercontents</span><span class="sxs-lookup"><span data-stu-id="a9293-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="a9293-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="a9293-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a9293-122">Web 図面内のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9293-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="a9293-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="a9293-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="a9293-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="a9293-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a9293-125">Web 図面内のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9293-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a9293-126">子要素</span><span class="sxs-lookup"><span data-stu-id="a9293-126">Child elements</span></span>

|<span data-ttu-id="a9293-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9293-127">**Element**</span></span>|<span data-ttu-id="a9293-128">**型**</span><span class="sxs-lookup"><span data-stu-id="a9293-128">**Type**</span></span>|<span data-ttu-id="a9293-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="a9293-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a9293-130">Shape</span><span class="sxs-lookup"><span data-stu-id="a9293-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a9293-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a9293-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a9293-132">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9293-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a9293-133">属性</span><span class="sxs-lookup"><span data-stu-id="a9293-133">Attributes</span></span>

<span data-ttu-id="a9293-134">なし。</span><span class="sxs-lookup"><span data-stu-id="a9293-134">None.</span></span>
  

