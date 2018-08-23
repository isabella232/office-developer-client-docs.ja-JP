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
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="efb6c-103">MasterContents 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="efb6c-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="efb6c-104">図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="efb6c-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="efb6c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="efb6c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efb6c-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="efb6c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="efb6c-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="efb6c-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="efb6c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="efb6c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="efb6c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="efb6c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="efb6c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="efb6c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="efb6c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="efb6c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="efb6c-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="efb6c-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efb6c-113">定義</span><span class="sxs-lookup"><span data-stu-id="efb6c-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="efb6c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="efb6c-114">Elements and attributes</span></span>

<span data-ttu-id="efb6c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efb6c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="efb6c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="efb6c-116">Parent elements</span></span>

<span data-ttu-id="efb6c-117">なし。</span><span class="sxs-lookup"><span data-stu-id="efb6c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efb6c-118">子要素</span><span class="sxs-lookup"><span data-stu-id="efb6c-118">Child elements</span></span>

|<span data-ttu-id="efb6c-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="efb6c-119">**Element**</span></span>|<span data-ttu-id="efb6c-120">**型**</span><span class="sxs-lookup"><span data-stu-id="efb6c-120">**Type**</span></span>|<span data-ttu-id="efb6c-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="efb6c-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efb6c-122">Connects</span><span class="sxs-lookup"><span data-stu-id="efb6c-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efb6c-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="efb6c-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="efb6c-124">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="efb6c-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="efb6c-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="efb6c-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="efb6c-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="efb6c-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="efb6c-127">**図形**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="efb6c-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="efb6c-128">属性</span><span class="sxs-lookup"><span data-stu-id="efb6c-128">Attributes</span></span>

<span data-ttu-id="efb6c-129">なし。</span><span class="sxs-lookup"><span data-stu-id="efb6c-129">None.</span></span>
  

