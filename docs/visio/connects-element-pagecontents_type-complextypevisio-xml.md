---
title: 要素 (PageContents_Type の複合型) を接続する ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: 図面内の 2 つの図形間の各接続の接続の要素が含まれています。
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805099"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="053c1-103">要素 (PageContents_Type の複合型) を接続する ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="053c1-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="053c1-104">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="053c1-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="053c1-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="053c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="053c1-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="053c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="053c1-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="053c1-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="053c1-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="053c1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="053c1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="053c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="053c1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="053c1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="053c1-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="053c1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="053c1-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="053c1-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="053c1-113">定義</span><span class="sxs-lookup"><span data-stu-id="053c1-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="053c1-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="053c1-114">Elements and attributes</span></span>

<span data-ttu-id="053c1-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="053c1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="053c1-116">親要素</span><span class="sxs-lookup"><span data-stu-id="053c1-116">Parent elements</span></span>

|<span data-ttu-id="053c1-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="053c1-117">**Element**</span></span>|<span data-ttu-id="053c1-118">**型**</span><span class="sxs-lookup"><span data-stu-id="053c1-118">**Type**</span></span>|<span data-ttu-id="053c1-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="053c1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="053c1-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="053c1-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="053c1-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="053c1-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="053c1-122">図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="053c1-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="053c1-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="053c1-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="053c1-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="053c1-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="053c1-125">図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="053c1-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="053c1-126">子要素</span><span class="sxs-lookup"><span data-stu-id="053c1-126">Child elements</span></span>

|<span data-ttu-id="053c1-127">**要素**</span><span class="sxs-lookup"><span data-stu-id="053c1-127">**Element**</span></span>|<span data-ttu-id="053c1-128">**型**</span><span class="sxs-lookup"><span data-stu-id="053c1-128">**Type**</span></span>|<span data-ttu-id="053c1-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="053c1-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="053c1-130">Connect</span><span class="sxs-lookup"><span data-stu-id="053c1-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="053c1-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="053c1-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="053c1-132">線と組織図内のボックスなど、図面内の 2 つの図形間の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="053c1-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="053c1-133">属性</span><span class="sxs-lookup"><span data-stu-id="053c1-133">Attributes</span></span>

<span data-ttu-id="053c1-134">なし。</span><span class="sxs-lookup"><span data-stu-id="053c1-134">None.</span></span>
  

