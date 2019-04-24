---
title: Data1 要素 (ShapeSheet_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: 図形に関する追加情報を提供するために使用される任意の文字列値を格納します。
ms.openlocfilehash: a203f915e9a5ff86e7cf75d96639157f76d3c151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345006"
---
# <a name="data1-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="1e291-103">Data1 要素 (ShapeSheet_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1e291-103">Data1 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1e291-104">図形に関する追加情報を提供するために使用される任意の文字列値を格納します。</span><span class="sxs-lookup"><span data-stu-id="1e291-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e291-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1e291-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e291-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1e291-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1e291-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="1e291-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1e291-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1e291-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1e291-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1e291-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1e291-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="1e291-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1e291-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1e291-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1e291-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="1e291-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e291-113">定義</span><span class="sxs-lookup"><span data-stu-id="1e291-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1e291-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1e291-114">Elements and attributes</span></span>

<span data-ttu-id="1e291-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e291-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1e291-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1e291-116">Parent elements</span></span>

|<span data-ttu-id="1e291-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1e291-117">**Element**</span></span>|<span data-ttu-id="1e291-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1e291-118">**Type**</span></span>|<span data-ttu-id="1e291-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1e291-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1e291-120">Shape</span><span class="sxs-lookup"><span data-stu-id="1e291-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1e291-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1e291-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1e291-122">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e291-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e291-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1e291-123">Child elements</span></span>

<span data-ttu-id="1e291-124">なし。</span><span class="sxs-lookup"><span data-stu-id="1e291-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e291-125">属性</span><span class="sxs-lookup"><span data-stu-id="1e291-125">Attributes</span></span>

<span data-ttu-id="1e291-126">なし。</span><span class="sxs-lookup"><span data-stu-id="1e291-126">None.</span></span>
  

