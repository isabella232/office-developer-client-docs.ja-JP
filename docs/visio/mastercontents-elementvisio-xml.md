---
title: MasterContents 要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: 図面のマスター シェイプ内の図形に関する情報を指定します。
ms.openlocfilehash: d1ba67a414ac80be9da2beebb93acc89faf71172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805826"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="86d50-103">MasterContents 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="86d50-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="86d50-104">図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="86d50-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="86d50-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="86d50-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86d50-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="86d50-106">**Element type**</span></span> <br/> |[<span data-ttu-id="86d50-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="86d50-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="86d50-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="86d50-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="86d50-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="86d50-109">**Schema file**</span></span> <br/> |<span data-ttu-id="86d50-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="86d50-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="86d50-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="86d50-111">**Document parts**</span></span> <br/> |<span data-ttu-id="86d50-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="86d50-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86d50-113">定義</span><span class="sxs-lookup"><span data-stu-id="86d50-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86d50-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="86d50-114">Elements and attributes</span></span>

<span data-ttu-id="86d50-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86d50-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="86d50-116">親要素</span><span class="sxs-lookup"><span data-stu-id="86d50-116">Parent elements</span></span>

<span data-ttu-id="86d50-117">なし。</span><span class="sxs-lookup"><span data-stu-id="86d50-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86d50-118">子要素</span><span class="sxs-lookup"><span data-stu-id="86d50-118">Child elements</span></span>

|<span data-ttu-id="86d50-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="86d50-119">**Element**</span></span>|<span data-ttu-id="86d50-120">**型**</span><span class="sxs-lookup"><span data-stu-id="86d50-120">**Type**</span></span>|<span data-ttu-id="86d50-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="86d50-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86d50-122">接続</span><span class="sxs-lookup"><span data-stu-id="86d50-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86d50-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="86d50-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86d50-124">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86d50-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="86d50-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="86d50-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86d50-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="86d50-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86d50-127">**図形**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="86d50-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="86d50-128">属性</span><span class="sxs-lookup"><span data-stu-id="86d50-128">Attributes</span></span>

<span data-ttu-id="86d50-129">なし。</span><span class="sxs-lookup"><span data-stu-id="86d50-129">None.</span></span>
  

