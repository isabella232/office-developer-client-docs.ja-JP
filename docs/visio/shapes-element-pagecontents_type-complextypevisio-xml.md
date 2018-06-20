---
title: 図形要素 (PageContents_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: 図形要素のコレクションが含まれています。
ms.openlocfilehash: eae86d230c19f1db8c7ed43cca8682460c3f7af1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806422"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="0d63d-103">図形要素 (PageContents_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="0d63d-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0d63d-104">図形要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d63d-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d63d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="0d63d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d63d-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="0d63d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0d63d-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="0d63d-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0d63d-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="0d63d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0d63d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="0d63d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0d63d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0d63d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0d63d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="0d63d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0d63d-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="0d63d-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d63d-113">定義</span><span class="sxs-lookup"><span data-stu-id="0d63d-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d63d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="0d63d-114">Elements and attributes</span></span>

<span data-ttu-id="0d63d-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d63d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0d63d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="0d63d-116">Parent elements</span></span>

|<span data-ttu-id="0d63d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="0d63d-117">**Element**</span></span>|<span data-ttu-id="0d63d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="0d63d-118">**Type**</span></span>|<span data-ttu-id="0d63d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d63d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d63d-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="0d63d-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="0d63d-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="0d63d-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d63d-122">Web 図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d63d-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="0d63d-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="0d63d-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="0d63d-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="0d63d-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d63d-125">Web 図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d63d-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0d63d-126">子要素</span><span class="sxs-lookup"><span data-stu-id="0d63d-126">Child elements</span></span>

|<span data-ttu-id="0d63d-127">**要素**</span><span class="sxs-lookup"><span data-stu-id="0d63d-127">**Element**</span></span>|<span data-ttu-id="0d63d-128">**型**</span><span class="sxs-lookup"><span data-stu-id="0d63d-128">**Type**</span></span>|<span data-ttu-id="0d63d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="0d63d-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d63d-130">Shape</span><span class="sxs-lookup"><span data-stu-id="0d63d-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d63d-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0d63d-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0d63d-132">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d63d-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0d63d-133">属性</span><span class="sxs-lookup"><span data-stu-id="0d63d-133">Attributes</span></span>

<span data-ttu-id="0d63d-134">なし。</span><span class="sxs-lookup"><span data-stu-id="0d63d-134">None.</span></span>
  

