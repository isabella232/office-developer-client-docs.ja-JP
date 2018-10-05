---
title: PageContents 要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: 図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。
ms.openlocfilehash: aec860f4135e15f18436dba50986b0ad0e6ee9e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396569"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="88b5a-103">PageContents 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="88b5a-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="88b5a-104">図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="88b5a-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88b5a-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="88b5a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88b5a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="88b5a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="88b5a-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="88b5a-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="88b5a-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="88b5a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="88b5a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="88b5a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="88b5a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="88b5a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="88b5a-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="88b5a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="88b5a-112">ページ # .xml</span><span class="sxs-lookup"><span data-stu-id="88b5a-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88b5a-113">定義</span><span class="sxs-lookup"><span data-stu-id="88b5a-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88b5a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="88b5a-114">Elements and attributes</span></span>

<span data-ttu-id="88b5a-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88b5a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="88b5a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="88b5a-116">Parent elements</span></span>

<span data-ttu-id="88b5a-117">なし。</span><span class="sxs-lookup"><span data-stu-id="88b5a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88b5a-118">子要素</span><span class="sxs-lookup"><span data-stu-id="88b5a-118">Child elements</span></span>

|<span data-ttu-id="88b5a-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="88b5a-119">**Element**</span></span>|<span data-ttu-id="88b5a-120">**型**</span><span class="sxs-lookup"><span data-stu-id="88b5a-120">**Type**</span></span>|<span data-ttu-id="88b5a-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="88b5a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88b5a-122">Connects</span><span class="sxs-lookup"><span data-stu-id="88b5a-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88b5a-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="88b5a-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88b5a-124">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="88b5a-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="88b5a-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="88b5a-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="88b5a-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="88b5a-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="88b5a-127">図形のコレクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="88b5a-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="88b5a-128">属性</span><span class="sxs-lookup"><span data-stu-id="88b5a-128">Attributes</span></span>

<span data-ttu-id="88b5a-129">なし。</span><span class="sxs-lookup"><span data-stu-id="88b5a-129">None.</span></span>
  

