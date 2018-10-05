---
title: MasterContents 要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: 図面のマスター シェイプ内の図形に関する情報を指定します。
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385467"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="06b09-103">MasterContents 要素 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="06b09-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="06b09-104">図面のマスター シェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="06b09-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="06b09-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="06b09-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06b09-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="06b09-106">**Element type**</span></span> <br/> |[<span data-ttu-id="06b09-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="06b09-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="06b09-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="06b09-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="06b09-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="06b09-109">**Schema file**</span></span> <br/> |<span data-ttu-id="06b09-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="06b09-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="06b09-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="06b09-111">**Document parts**</span></span> <br/> |<span data-ttu-id="06b09-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="06b09-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06b09-113">定義</span><span class="sxs-lookup"><span data-stu-id="06b09-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="06b09-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="06b09-114">Elements and attributes</span></span>

<span data-ttu-id="06b09-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="06b09-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="06b09-116">親要素</span><span class="sxs-lookup"><span data-stu-id="06b09-116">Parent elements</span></span>

<span data-ttu-id="06b09-117">なし。</span><span class="sxs-lookup"><span data-stu-id="06b09-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06b09-118">子要素</span><span class="sxs-lookup"><span data-stu-id="06b09-118">Child elements</span></span>

|<span data-ttu-id="06b09-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="06b09-119">**Element**</span></span>|<span data-ttu-id="06b09-120">**型**</span><span class="sxs-lookup"><span data-stu-id="06b09-120">**Type**</span></span>|<span data-ttu-id="06b09-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="06b09-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06b09-122">Connects</span><span class="sxs-lookup"><span data-stu-id="06b09-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06b09-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="06b09-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="06b09-124">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b09-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="06b09-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="06b09-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06b09-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="06b09-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="06b09-127">**図形**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b09-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="06b09-128">属性</span><span class="sxs-lookup"><span data-stu-id="06b09-128">Attributes</span></span>

<span data-ttu-id="06b09-129">なし。</span><span class="sxs-lookup"><span data-stu-id="06b09-129">None.</span></span>
  

