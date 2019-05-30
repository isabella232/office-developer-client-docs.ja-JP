---
title: Shapes 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Shape 要素のコレクションを格納します。
ms.openlocfilehash: e9f45d1f61b83339274d24aea2c0473adf282bac
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542101"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="75f39-103">Shapes 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="75f39-103">Shapes element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="75f39-104">Shape 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="75f39-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75f39-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="75f39-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75f39-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="75f39-106">**Element type**</span></span> <br/> |[<span data-ttu-id="75f39-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="75f39-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="75f39-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75f39-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="75f39-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="75f39-109">**Schema file**</span></span> <br/> |<span data-ttu-id="75f39-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="75f39-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="75f39-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="75f39-111">**Document parts**</span></span> <br/> |<span data-ttu-id="75f39-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="75f39-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75f39-113">定義</span><span class="sxs-lookup"><span data-stu-id="75f39-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="75f39-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="75f39-114">Elements and attributes</span></span>

<span data-ttu-id="75f39-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75f39-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="75f39-116">親要素</span><span class="sxs-lookup"><span data-stu-id="75f39-116">Parent elements</span></span>

|<span data-ttu-id="75f39-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="75f39-117">**Element**</span></span>|<span data-ttu-id="75f39-118">**型**</span><span class="sxs-lookup"><span data-stu-id="75f39-118">**Type**</span></span>|<span data-ttu-id="75f39-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="75f39-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75f39-120">Shape</span><span class="sxs-lookup"><span data-stu-id="75f39-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75f39-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="75f39-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75f39-122">図形に関連付けられたプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="75f39-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="75f39-123">子要素</span><span class="sxs-lookup"><span data-stu-id="75f39-123">Child elements</span></span>

|<span data-ttu-id="75f39-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="75f39-124">**Element**</span></span>|<span data-ttu-id="75f39-125">**型**</span><span class="sxs-lookup"><span data-stu-id="75f39-125">**Type**</span></span>|<span data-ttu-id="75f39-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="75f39-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="75f39-127">Shape</span><span class="sxs-lookup"><span data-stu-id="75f39-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="75f39-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="75f39-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="75f39-129">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="75f39-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="75f39-130">属性</span><span class="sxs-lookup"><span data-stu-id="75f39-130">Attributes</span></span>

<span data-ttu-id="75f39-131">なし。</span><span class="sxs-lookup"><span data-stu-id="75f39-131">None.</span></span>
  

