---
title: Data3 要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 63493467-af55-fa62-6c39-6b5896895952
description: 図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。
ms.openlocfilehash: 68f35887cc84b87caddb87072e50649ada9ea25a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805165"
---
# <a name="data3-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="a1bb1-103">Data3 要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a1bb1-103">Data3 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a1bb1-104">図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1bb1-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1bb1-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a1bb1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1bb1-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a1bb1-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="a1bb1-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a1bb1-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a1bb1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a1bb1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a1bb1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a1bb1-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a1bb1-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="a1bb1-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1bb1-113">定義</span><span class="sxs-lookup"><span data-stu-id="a1bb1-113">Definition</span></span>

```XML
< xs:element name="Data3" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1bb1-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a1bb1-114">Elements and attributes</span></span>

<span data-ttu-id="a1bb1-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1bb1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a1bb1-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a1bb1-116">Parent elements</span></span>

|<span data-ttu-id="a1bb1-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-117">**Element**</span></span>|<span data-ttu-id="a1bb1-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-118">**Type**</span></span>|<span data-ttu-id="a1bb1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a1bb1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1bb1-120">Shape</span><span class="sxs-lookup"><span data-stu-id="a1bb1-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1bb1-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a1bb1-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1bb1-122">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1bb1-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a1bb1-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a1bb1-123">Child elements</span></span>

<span data-ttu-id="a1bb1-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a1bb1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1bb1-125">属性</span><span class="sxs-lookup"><span data-stu-id="a1bb1-125">Attributes</span></span>

<span data-ttu-id="a1bb1-126">なし。</span><span class="sxs-lookup"><span data-stu-id="a1bb1-126">None.</span></span>
  

