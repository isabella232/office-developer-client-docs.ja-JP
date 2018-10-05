---
title: Data3 要素 (ShapeSheet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 63493467-af55-fa62-6c39-6b5896895952
description: 図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。
ms.openlocfilehash: a21d92e6ff8683ed3e35e233c8cce3aee015e4a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396030"
---
# <a name="data3-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ad51a-103">Data3 要素 (ShapeSheet_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="ad51a-103">Data3 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad51a-104">図形に関する追加情報を提供するために使用される任意の文字列値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad51a-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad51a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ad51a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad51a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ad51a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad51a-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="ad51a-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad51a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="ad51a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad51a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ad51a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad51a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad51a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad51a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ad51a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad51a-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="ad51a-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad51a-113">定義</span><span class="sxs-lookup"><span data-stu-id="ad51a-113">Definition</span></span>

```XML
< xs:element name="Data3" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad51a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ad51a-114">Elements and attributes</span></span>

<span data-ttu-id="ad51a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad51a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad51a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ad51a-116">Parent elements</span></span>

|<span data-ttu-id="ad51a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ad51a-117">**Element**</span></span>|<span data-ttu-id="ad51a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ad51a-118">**Type**</span></span>|<span data-ttu-id="ad51a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad51a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad51a-120">Shape</span><span class="sxs-lookup"><span data-stu-id="ad51a-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad51a-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ad51a-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad51a-122">**マスター シェイプ**、**ページ**、または図形要素のグループ内の図形を定義する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ad51a-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad51a-123">子要素</span><span class="sxs-lookup"><span data-stu-id="ad51a-123">Child elements</span></span>

<span data-ttu-id="ad51a-124">なし。</span><span class="sxs-lookup"><span data-stu-id="ad51a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad51a-125">属性</span><span class="sxs-lookup"><span data-stu-id="ad51a-125">Attributes</span></span>

<span data-ttu-id="ad51a-126">なし。</span><span class="sxs-lookup"><span data-stu-id="ad51a-126">None.</span></span>
  

