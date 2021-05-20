---
title: Connects 要素 (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: 図面内の 2 Connect間の接続ごとに 1 つの要素を格納します。
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538712"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="8987a-103">Connects 要素 (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8987a-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8987a-104">図面内の **2 Connect** 間の接続ごとに 1 つの要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="8987a-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8987a-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="8987a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8987a-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8987a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8987a-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="8987a-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8987a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8987a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8987a-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8987a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8987a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8987a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8987a-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="8987a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8987a-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="8987a-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8987a-113">定義</span><span class="sxs-lookup"><span data-stu-id="8987a-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8987a-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8987a-114">Elements and attributes</span></span>

<span data-ttu-id="8987a-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8987a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8987a-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8987a-116">Parent elements</span></span>

|<span data-ttu-id="8987a-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8987a-117">**Element**</span></span>|<span data-ttu-id="8987a-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8987a-118">**Type**</span></span>|<span data-ttu-id="8987a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8987a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8987a-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="8987a-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8987a-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8987a-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8987a-122">図面のマスター ページまたは図面ページ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8987a-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="8987a-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="8987a-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="8987a-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="8987a-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8987a-125">図面のマスター ページまたは図面ページ内の図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="8987a-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8987a-126">子要素</span><span class="sxs-lookup"><span data-stu-id="8987a-126">Child elements</span></span>

|<span data-ttu-id="8987a-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="8987a-127">**Element**</span></span>|<span data-ttu-id="8987a-128">**型**</span><span class="sxs-lookup"><span data-stu-id="8987a-128">**Type**</span></span>|<span data-ttu-id="8987a-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="8987a-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8987a-130">Connect</span><span class="sxs-lookup"><span data-stu-id="8987a-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8987a-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="8987a-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8987a-132">組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="8987a-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8987a-133">属性</span><span class="sxs-lookup"><span data-stu-id="8987a-133">Attributes</span></span>

<span data-ttu-id="8987a-134">なし。</span><span class="sxs-lookup"><span data-stu-id="8987a-134">None.</span></span>
  

