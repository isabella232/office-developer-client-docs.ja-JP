---
title: 接続要素 (PageContents_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: 図面内の2つの図形を接続するための Connect 要素を含みます。
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318964"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="b23d5-103">接続要素 (PageContents_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b23d5-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b23d5-104">図面内の2つの図形を接続するための**Connect**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="b23d5-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b23d5-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b23d5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b23d5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b23d5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b23d5-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="b23d5-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b23d5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b23d5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b23d5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b23d5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b23d5-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="b23d5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b23d5-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b23d5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b23d5-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="b23d5-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b23d5-113">定義</span><span class="sxs-lookup"><span data-stu-id="b23d5-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b23d5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b23d5-114">Elements and attributes</span></span>

<span data-ttu-id="b23d5-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b23d5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b23d5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b23d5-116">Parent elements</span></span>

|<span data-ttu-id="b23d5-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b23d5-117">**Element**</span></span>|<span data-ttu-id="b23d5-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b23d5-118">**Type**</span></span>|<span data-ttu-id="b23d5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b23d5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b23d5-120">mastercontents</span><span class="sxs-lookup"><span data-stu-id="b23d5-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="b23d5-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="b23d5-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b23d5-122">図面のマスターページまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="b23d5-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="b23d5-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="b23d5-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="b23d5-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="b23d5-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b23d5-125">図面のマスターページまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="b23d5-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b23d5-126">子要素</span><span class="sxs-lookup"><span data-stu-id="b23d5-126">Child elements</span></span>

|<span data-ttu-id="b23d5-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="b23d5-127">**Element**</span></span>|<span data-ttu-id="b23d5-128">**型**</span><span class="sxs-lookup"><span data-stu-id="b23d5-128">**Type**</span></span>|<span data-ttu-id="b23d5-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="b23d5-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b23d5-130">Connect</span><span class="sxs-lookup"><span data-stu-id="b23d5-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b23d5-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="b23d5-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b23d5-132">組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="b23d5-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b23d5-133">属性</span><span class="sxs-lookup"><span data-stu-id="b23d5-133">Attributes</span></span>

<span data-ttu-id="b23d5-134">なし。</span><span class="sxs-lookup"><span data-stu-id="b23d5-134">None.</span></span>
  

