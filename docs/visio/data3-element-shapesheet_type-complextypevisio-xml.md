---
title: Data3 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 63493467-af55-fa62-6c39-6b5896895952
description: 図形に関する追加情報を提供するために使用される任意の文字列値を含む。
ms.openlocfilehash: 1ce286c0c8db53305f78def465ac31a3ef3afdec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541254"
---
# <a name="data3-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="5af3d-103">Data3 要素 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="5af3d-103">Data3 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="5af3d-104">図形に関する追加情報を提供するために使用される任意の文字列値を含む。</span><span class="sxs-lookup"><span data-stu-id="5af3d-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5af3d-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="5af3d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5af3d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="5af3d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5af3d-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="5af3d-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5af3d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5af3d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5af3d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5af3d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5af3d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5af3d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5af3d-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="5af3d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5af3d-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="5af3d-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5af3d-113">定義</span><span class="sxs-lookup"><span data-stu-id="5af3d-113">Definition</span></span>

```XML
< xs:element name="Data3" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5af3d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5af3d-114">Elements and attributes</span></span>

<span data-ttu-id="5af3d-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5af3d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5af3d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5af3d-116">Parent elements</span></span>

|<span data-ttu-id="5af3d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5af3d-117">**Element**</span></span>|<span data-ttu-id="5af3d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5af3d-118">**Type**</span></span>|<span data-ttu-id="5af3d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5af3d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5af3d-120">Shape</span><span class="sxs-lookup"><span data-stu-id="5af3d-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5af3d-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5af3d-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5af3d-122">**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。</span><span class="sxs-lookup"><span data-stu-id="5af3d-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5af3d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5af3d-123">Child elements</span></span>

<span data-ttu-id="5af3d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5af3d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5af3d-125">属性</span><span class="sxs-lookup"><span data-stu-id="5af3d-125">Attributes</span></span>

<span data-ttu-id="5af3d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="5af3d-126">None.</span></span>
  

