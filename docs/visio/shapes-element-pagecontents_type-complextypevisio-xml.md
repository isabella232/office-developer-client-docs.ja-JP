---
title: 図形要素 (PageContents_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: 図形要素のコレクションが含まれています。
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397570"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="4f9b8-103">図形要素 (PageContents_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="4f9b8-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4f9b8-104">図形要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f9b8-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4f9b8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f9b8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f9b8-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="4f9b8-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f9b8-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f9b8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f9b8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4f9b8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f9b8-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4f9b8-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="4f9b8-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f9b8-113">定義</span><span class="sxs-lookup"><span data-stu-id="4f9b8-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f9b8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4f9b8-114">Elements and attributes</span></span>

<span data-ttu-id="4f9b8-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f9b8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4f9b8-116">Parent elements</span></span>

|<span data-ttu-id="4f9b8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-117">**Element**</span></span>|<span data-ttu-id="4f9b8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-118">**Type**</span></span>|<span data-ttu-id="4f9b8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f9b8-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="4f9b8-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f9b8-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="4f9b8-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f9b8-122">Web 図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="4f9b8-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="4f9b8-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f9b8-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="4f9b8-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f9b8-125">Web 図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f9b8-126">子要素</span><span class="sxs-lookup"><span data-stu-id="4f9b8-126">Child elements</span></span>

|<span data-ttu-id="4f9b8-127">**要素**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-127">**Element**</span></span>|<span data-ttu-id="4f9b8-128">**型**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-128">**Type**</span></span>|<span data-ttu-id="4f9b8-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f9b8-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f9b8-130">Shape</span><span class="sxs-lookup"><span data-stu-id="4f9b8-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f9b8-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4f9b8-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f9b8-132">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f9b8-133">属性</span><span class="sxs-lookup"><span data-stu-id="4f9b8-133">Attributes</span></span>

<span data-ttu-id="4f9b8-134">なし。</span><span class="sxs-lookup"><span data-stu-id="4f9b8-134">None.</span></span>
  

