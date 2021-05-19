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
# <a name="shapes-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="a306d-103">Shapes 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a306d-103">Shapes element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a306d-104">Shape 要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="a306d-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a306d-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="a306d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a306d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a306d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a306d-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="a306d-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a306d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a306d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a306d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a306d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a306d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a306d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a306d-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="a306d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a306d-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="a306d-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a306d-113">定義</span><span class="sxs-lookup"><span data-stu-id="a306d-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a306d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a306d-114">Elements and attributes</span></span>

<span data-ttu-id="a306d-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a306d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a306d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a306d-116">Parent elements</span></span>

|<span data-ttu-id="a306d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a306d-117">**Element**</span></span>|<span data-ttu-id="a306d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a306d-118">**Type**</span></span>|<span data-ttu-id="a306d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a306d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a306d-120">Shape</span><span class="sxs-lookup"><span data-stu-id="a306d-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a306d-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a306d-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a306d-122">図形に関連付けられたプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="a306d-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a306d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a306d-123">Child elements</span></span>

|<span data-ttu-id="a306d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a306d-124">**Element**</span></span>|<span data-ttu-id="a306d-125">**型**</span><span class="sxs-lookup"><span data-stu-id="a306d-125">**Type**</span></span>|<span data-ttu-id="a306d-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="a306d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a306d-127">Shape</span><span class="sxs-lookup"><span data-stu-id="a306d-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a306d-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a306d-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a306d-129">**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。</span><span class="sxs-lookup"><span data-stu-id="a306d-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a306d-130">属性</span><span class="sxs-lookup"><span data-stu-id="a306d-130">Attributes</span></span>

<span data-ttu-id="a306d-131">なし。</span><span class="sxs-lookup"><span data-stu-id="a306d-131">None.</span></span>
  

