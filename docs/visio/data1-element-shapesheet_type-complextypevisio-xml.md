---
title: Data1 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: 図形に関する追加情報を提供するために使用される任意の文字列値を格納します。
ms.openlocfilehash: e4ff724eee51e3a7efe8bc4f270568da066901a5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542486"
---
# <a name="data1-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="5d7a6-103">Data1 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5d7a6-103">Data1 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5d7a6-104">図形に関する追加情報を提供するために使用される任意の文字列値を格納します。</span><span class="sxs-lookup"><span data-stu-id="5d7a6-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d7a6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5d7a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d7a6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5d7a6-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5d7a6-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5d7a6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5d7a6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5d7a6-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="5d7a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5d7a6-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5d7a6-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="5d7a6-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5d7a6-113">定義</span><span class="sxs-lookup"><span data-stu-id="5d7a6-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5d7a6-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5d7a6-114">Elements and attributes</span></span>

<span data-ttu-id="5d7a6-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d7a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5d7a6-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5d7a6-116">Parent elements</span></span>

|<span data-ttu-id="5d7a6-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-117">**Element**</span></span>|<span data-ttu-id="5d7a6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-118">**Type**</span></span>|<span data-ttu-id="5d7a6-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5d7a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5d7a6-120">Shape</span><span class="sxs-lookup"><span data-stu-id="5d7a6-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5d7a6-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5d7a6-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5d7a6-122">**マスター**シェイプ、**ページ**、またはグループの shape 要素の図形を定義する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d7a6-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d7a6-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5d7a6-123">Child elements</span></span>

<span data-ttu-id="5d7a6-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5d7a6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d7a6-125">属性</span><span class="sxs-lookup"><span data-stu-id="5d7a6-125">Attributes</span></span>

<span data-ttu-id="5d7a6-126">なし。</span><span class="sxs-lookup"><span data-stu-id="5d7a6-126">None.</span></span>
  

