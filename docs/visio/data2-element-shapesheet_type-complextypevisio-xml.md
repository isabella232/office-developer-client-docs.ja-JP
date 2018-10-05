---
title: Data2 の要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: 図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。
ms.openlocfilehash: ebd70fc0f83bd7cbf0bd6465c5e06276675a8022
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401714"
---
# <a name="data2-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="e167e-103">Data2 の要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e167e-103">Data2 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e167e-104">図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e167e-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e167e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e167e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e167e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e167e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e167e-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e167e-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e167e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e167e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e167e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e167e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e167e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e167e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e167e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e167e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e167e-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="e167e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e167e-113">定義</span><span class="sxs-lookup"><span data-stu-id="e167e-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e167e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e167e-114">Elements and attributes</span></span>

<span data-ttu-id="e167e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e167e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e167e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e167e-116">Parent elements</span></span>

|<span data-ttu-id="e167e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e167e-117">**Element**</span></span>|<span data-ttu-id="e167e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e167e-118">**Type**</span></span>|<span data-ttu-id="e167e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e167e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e167e-120">Shape</span><span class="sxs-lookup"><span data-stu-id="e167e-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e167e-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e167e-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e167e-122">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e167e-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e167e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e167e-123">Child elements</span></span>

<span data-ttu-id="e167e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="e167e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e167e-125">属性</span><span class="sxs-lookup"><span data-stu-id="e167e-125">Attributes</span></span>

<span data-ttu-id="e167e-126">なし。</span><span class="sxs-lookup"><span data-stu-id="e167e-126">None.</span></span>
  

