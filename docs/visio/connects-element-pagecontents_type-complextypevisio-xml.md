---
title: 要素 (PageContents_Type の複合型) を接続する ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: 図面内の 2 つの図形間の各接続の接続の要素が含まれています。
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399957"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="765f0-103">要素 (PageContents_Type の複合型) を接続する ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="765f0-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="765f0-104">図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="765f0-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="765f0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="765f0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="765f0-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="765f0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="765f0-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="765f0-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="765f0-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="765f0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="765f0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="765f0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="765f0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="765f0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="765f0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="765f0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="765f0-112"># .xml のページで、マスターの # .xml</span><span class="sxs-lookup"><span data-stu-id="765f0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="765f0-113">定義</span><span class="sxs-lookup"><span data-stu-id="765f0-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="765f0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="765f0-114">Elements and attributes</span></span>

<span data-ttu-id="765f0-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="765f0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="765f0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="765f0-116">Parent elements</span></span>

|<span data-ttu-id="765f0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="765f0-117">**Element**</span></span>|<span data-ttu-id="765f0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="765f0-118">**Type**</span></span>|<span data-ttu-id="765f0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="765f0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="765f0-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="765f0-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="765f0-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="765f0-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="765f0-122">図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="765f0-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="765f0-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="765f0-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="765f0-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="765f0-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="765f0-125">図面のマスター シェイプまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="765f0-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="765f0-126">子要素</span><span class="sxs-lookup"><span data-stu-id="765f0-126">Child elements</span></span>

|<span data-ttu-id="765f0-127">**要素**</span><span class="sxs-lookup"><span data-stu-id="765f0-127">**Element**</span></span>|<span data-ttu-id="765f0-128">**型**</span><span class="sxs-lookup"><span data-stu-id="765f0-128">**Type**</span></span>|<span data-ttu-id="765f0-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="765f0-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="765f0-130">Connect</span><span class="sxs-lookup"><span data-stu-id="765f0-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="765f0-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="765f0-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="765f0-132">
			組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。
</span><span class="sxs-lookup"><span data-stu-id="765f0-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="765f0-133">属性</span><span class="sxs-lookup"><span data-stu-id="765f0-133">Attributes</span></span>

<span data-ttu-id="765f0-134">なし。</span><span class="sxs-lookup"><span data-stu-id="765f0-134">None.</span></span>
  

