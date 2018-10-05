---
title: Data1 要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: 図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。
ms.openlocfilehash: a203f915e9a5ff86e7cf75d96639157f76d3c151
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390969"
---
# <a name="data1-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="a3b1c-103">Data1 要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a3b1c-103">Data1 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a3b1c-104">図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3b1c-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3b1c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a3b1c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3b1c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a3b1c-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a3b1c-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3b1c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3b1c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a3b1c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a3b1c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3b1c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a3b1c-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="a3b1c-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3b1c-113">定義</span><span class="sxs-lookup"><span data-stu-id="a3b1c-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3b1c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a3b1c-114">Elements and attributes</span></span>

<span data-ttu-id="a3b1c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3b1c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3b1c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a3b1c-116">Parent elements</span></span>

|<span data-ttu-id="a3b1c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-117">**Element**</span></span>|<span data-ttu-id="a3b1c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-118">**Type**</span></span>|<span data-ttu-id="a3b1c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3b1c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3b1c-120">Shape</span><span class="sxs-lookup"><span data-stu-id="a3b1c-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3b1c-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a3b1c-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3b1c-122">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a3b1c-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3b1c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a3b1c-123">Child elements</span></span>

<span data-ttu-id="a3b1c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a3b1c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3b1c-125">属性</span><span class="sxs-lookup"><span data-stu-id="a3b1c-125">Attributes</span></span>

<span data-ttu-id="a3b1c-126">なし。</span><span class="sxs-lookup"><span data-stu-id="a3b1c-126">None.</span></span>
  

