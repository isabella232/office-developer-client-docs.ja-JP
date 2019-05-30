---
title: MasterContents 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: 図面のマスターシェイプ内の図形に関する情報を指定します。
ms.openlocfilehash: 26bc86aedeb96544f61f53052ab723b13b29500d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538040"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="9deaa-103">MasterContents 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9deaa-103">MasterContents element (Visio XML)</span></span>

<span data-ttu-id="9deaa-104">図面のマスターシェイプ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="9deaa-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9deaa-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9deaa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9deaa-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9deaa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9deaa-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="9deaa-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9deaa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9deaa-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9deaa-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9deaa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9deaa-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="9deaa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9deaa-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="9deaa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9deaa-112">マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="9deaa-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9deaa-113">定義</span><span class="sxs-lookup"><span data-stu-id="9deaa-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9deaa-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9deaa-114">Elements and attributes</span></span>

<span data-ttu-id="9deaa-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9deaa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9deaa-116">親要素</span><span class="sxs-lookup"><span data-stu-id="9deaa-116">Parent elements</span></span>

<span data-ttu-id="9deaa-117">なし。</span><span class="sxs-lookup"><span data-stu-id="9deaa-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9deaa-118">子要素</span><span class="sxs-lookup"><span data-stu-id="9deaa-118">Child elements</span></span>

|<span data-ttu-id="9deaa-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="9deaa-119">**Element**</span></span>|<span data-ttu-id="9deaa-120">**型**</span><span class="sxs-lookup"><span data-stu-id="9deaa-120">**Type**</span></span>|<span data-ttu-id="9deaa-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="9deaa-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9deaa-122">Connects</span><span class="sxs-lookup"><span data-stu-id="9deaa-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9deaa-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="9deaa-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9deaa-124">図面内の2つの図形を接続するための**Connect**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="9deaa-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="9deaa-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="9deaa-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9deaa-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="9deaa-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9deaa-127">**Shape**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="9deaa-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9deaa-128">属性</span><span class="sxs-lookup"><span data-stu-id="9deaa-128">Attributes</span></span>

<span data-ttu-id="9deaa-129">なし。</span><span class="sxs-lookup"><span data-stu-id="9deaa-129">None.</span></span>
  

