---
title: mastercontents 要素 (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: 図面のマスターシェイプ内の図形に関する情報を指定します。
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341357"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="d9da9-103">mastercontents 要素 (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="d9da9-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="d9da9-104">図面のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9da9-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d9da9-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="d9da9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9da9-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d9da9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d9da9-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d9da9-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d9da9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d9da9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d9da9-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d9da9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d9da9-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="d9da9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d9da9-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d9da9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d9da9-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="d9da9-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9da9-113">定義</span><span class="sxs-lookup"><span data-stu-id="d9da9-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d9da9-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d9da9-114">Elements and attributes</span></span>

<span data-ttu-id="d9da9-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9da9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d9da9-116">親要素</span><span class="sxs-lookup"><span data-stu-id="d9da9-116">Parent elements</span></span>

<span data-ttu-id="d9da9-117">なし。</span><span class="sxs-lookup"><span data-stu-id="d9da9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9da9-118">子要素</span><span class="sxs-lookup"><span data-stu-id="d9da9-118">Child elements</span></span>

|<span data-ttu-id="d9da9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9da9-119">**Element**</span></span>|<span data-ttu-id="d9da9-120">**型**</span><span class="sxs-lookup"><span data-stu-id="d9da9-120">**Type**</span></span>|<span data-ttu-id="d9da9-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9da9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9da9-122">Connects</span><span class="sxs-lookup"><span data-stu-id="d9da9-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9da9-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="d9da9-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9da9-124">図面内の2つの図形を接続するための**Connect**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="d9da9-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="d9da9-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="d9da9-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9da9-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="d9da9-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9da9-127">**Shape**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="d9da9-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d9da9-128">属性</span><span class="sxs-lookup"><span data-stu-id="d9da9-128">Attributes</span></span>

<span data-ttu-id="d9da9-129">なし。</span><span class="sxs-lookup"><span data-stu-id="d9da9-129">None.</span></span>
  

