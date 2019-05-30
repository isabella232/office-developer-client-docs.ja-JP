---
title: Shapes 要素 (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Shape 要素のコレクションを格納します。
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542122"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="6ac30-103">Shapes 要素 (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6ac30-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6ac30-104">Shape 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="6ac30-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ac30-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="6ac30-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ac30-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="6ac30-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6ac30-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="6ac30-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6ac30-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ac30-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6ac30-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6ac30-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6ac30-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="6ac30-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6ac30-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="6ac30-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6ac30-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="6ac30-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ac30-113">定義</span><span class="sxs-lookup"><span data-stu-id="6ac30-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ac30-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6ac30-114">Elements and attributes</span></span>

<span data-ttu-id="6ac30-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ac30-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6ac30-116">親要素</span><span class="sxs-lookup"><span data-stu-id="6ac30-116">Parent elements</span></span>

|<span data-ttu-id="6ac30-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="6ac30-117">**Element**</span></span>|<span data-ttu-id="6ac30-118">**型**</span><span class="sxs-lookup"><span data-stu-id="6ac30-118">**Type**</span></span>|<span data-ttu-id="6ac30-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ac30-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ac30-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="6ac30-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6ac30-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6ac30-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ac30-122">Web 図面内のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ac30-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="6ac30-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="6ac30-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="6ac30-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="6ac30-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ac30-125">Web 図面内のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ac30-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6ac30-126">子要素</span><span class="sxs-lookup"><span data-stu-id="6ac30-126">Child elements</span></span>

|<span data-ttu-id="6ac30-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="6ac30-127">**Element**</span></span>|<span data-ttu-id="6ac30-128">**型**</span><span class="sxs-lookup"><span data-stu-id="6ac30-128">**Type**</span></span>|<span data-ttu-id="6ac30-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ac30-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ac30-130">Shape</span><span class="sxs-lookup"><span data-stu-id="6ac30-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6ac30-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6ac30-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6ac30-132">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ac30-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6ac30-133">属性</span><span class="sxs-lookup"><span data-stu-id="6ac30-133">Attributes</span></span>

<span data-ttu-id="6ac30-134">なし。</span><span class="sxs-lookup"><span data-stu-id="6ac30-134">None.</span></span>
  

