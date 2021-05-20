---
title: PageContents 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: 図面のマスター ページまたは図面ページ内の図形に関する情報を指定します。
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537998"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="d6e0c-103">PageContents 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="d6e0c-104">図面のマスター ページまたは図面ページ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6e0c-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="d6e0c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6e0c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d6e0c-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d6e0c-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d6e0c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d6e0c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d6e0c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d6e0c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d6e0c-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d6e0c-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="d6e0c-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d6e0c-113">定義</span><span class="sxs-lookup"><span data-stu-id="d6e0c-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d6e0c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d6e0c-114">Elements and attributes</span></span>

<span data-ttu-id="d6e0c-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d6e0c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d6e0c-116">Parent elements</span></span>

<span data-ttu-id="d6e0c-117">なし。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6e0c-118">子要素</span><span class="sxs-lookup"><span data-stu-id="d6e0c-118">Child elements</span></span>

|<span data-ttu-id="d6e0c-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-119">**Element**</span></span>|<span data-ttu-id="d6e0c-120">**型**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-120">**Type**</span></span>|<span data-ttu-id="d6e0c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d6e0c-122">Connects</span><span class="sxs-lookup"><span data-stu-id="d6e0c-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6e0c-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="d6e0c-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6e0c-124">図面内の **2 Connect** 間の接続ごとに 1 つの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="d6e0c-125">図形</span><span class="sxs-lookup"><span data-stu-id="d6e0c-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d6e0c-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="d6e0c-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d6e0c-127">図形のコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d6e0c-128">属性</span><span class="sxs-lookup"><span data-stu-id="d6e0c-128">Attributes</span></span>

<span data-ttu-id="d6e0c-129">なし。</span><span class="sxs-lookup"><span data-stu-id="d6e0c-129">None.</span></span>
  

