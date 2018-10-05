---
title: 図形要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: 図形要素のコレクションが含まれています。
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392096"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="92425-103">図形要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="92425-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="92425-104">図形要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="92425-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92425-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="92425-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92425-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="92425-106">**Element type**</span></span> <br/> |[<span data-ttu-id="92425-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="92425-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="92425-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="92425-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="92425-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="92425-109">**Schema file**</span></span> <br/> |<span data-ttu-id="92425-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="92425-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="92425-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="92425-111">**Document parts**</span></span> <br/> |<span data-ttu-id="92425-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="92425-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92425-113">定義</span><span class="sxs-lookup"><span data-stu-id="92425-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92425-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="92425-114">Elements and attributes</span></span>

<span data-ttu-id="92425-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92425-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="92425-116">親要素</span><span class="sxs-lookup"><span data-stu-id="92425-116">Parent elements</span></span>

|<span data-ttu-id="92425-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="92425-117">**Element**</span></span>|<span data-ttu-id="92425-118">**型**</span><span class="sxs-lookup"><span data-stu-id="92425-118">**Type**</span></span>|<span data-ttu-id="92425-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="92425-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92425-120">Shape</span><span class="sxs-lookup"><span data-stu-id="92425-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92425-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="92425-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92425-122">図形に関連付けられているプロパティのコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="92425-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92425-123">子要素</span><span class="sxs-lookup"><span data-stu-id="92425-123">Child elements</span></span>

|<span data-ttu-id="92425-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="92425-124">**Element**</span></span>|<span data-ttu-id="92425-125">**型**</span><span class="sxs-lookup"><span data-stu-id="92425-125">**Type**</span></span>|<span data-ttu-id="92425-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="92425-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92425-127">Shape</span><span class="sxs-lookup"><span data-stu-id="92425-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92425-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="92425-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92425-129">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92425-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="92425-130">属性</span><span class="sxs-lookup"><span data-stu-id="92425-130">Attributes</span></span>

<span data-ttu-id="92425-131">なし。</span><span class="sxs-lookup"><span data-stu-id="92425-131">None.</span></span>
  

