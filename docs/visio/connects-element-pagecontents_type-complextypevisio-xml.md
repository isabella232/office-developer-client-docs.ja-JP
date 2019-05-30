---
title: 結び付ける要素 (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: 図面内の2つの図形を接続するための Connect 要素を含みます。
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538712"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="ea347-103">結び付ける要素 (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ea347-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ea347-104">図面内の2つの図形を接続するための**Connect**要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="ea347-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ea347-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="ea347-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea347-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ea347-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ea347-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="ea347-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ea347-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ea347-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ea347-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ea347-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ea347-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="ea347-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ea347-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="ea347-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ea347-112">ページ # .xml、マスター # .xml</span><span class="sxs-lookup"><span data-stu-id="ea347-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ea347-113">定義</span><span class="sxs-lookup"><span data-stu-id="ea347-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ea347-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ea347-114">Elements and attributes</span></span>

<span data-ttu-id="ea347-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea347-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ea347-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ea347-116">Parent elements</span></span>

|<span data-ttu-id="ea347-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="ea347-117">**Element**</span></span>|<span data-ttu-id="ea347-118">**型**</span><span class="sxs-lookup"><span data-stu-id="ea347-118">**Type**</span></span>|<span data-ttu-id="ea347-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea347-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea347-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="ea347-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="ea347-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="ea347-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea347-122">図面のマスターページまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea347-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="ea347-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="ea347-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="ea347-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="ea347-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea347-125">図面のマスターページまたは図面ページの図形に関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="ea347-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ea347-126">子要素</span><span class="sxs-lookup"><span data-stu-id="ea347-126">Child elements</span></span>

|<span data-ttu-id="ea347-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="ea347-127">**Element**</span></span>|<span data-ttu-id="ea347-128">**型**</span><span class="sxs-lookup"><span data-stu-id="ea347-128">**Type**</span></span>|<span data-ttu-id="ea347-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea347-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ea347-130">Connect</span><span class="sxs-lookup"><span data-stu-id="ea347-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ea347-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="ea347-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ea347-132">組織図の線やボックスなど、図面内の 2 つの図形の接続を表します。</span><span class="sxs-lookup"><span data-stu-id="ea347-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ea347-133">属性</span><span class="sxs-lookup"><span data-stu-id="ea347-133">Attributes</span></span>

<span data-ttu-id="ea347-134">なし。</span><span class="sxs-lookup"><span data-stu-id="ea347-134">None.</span></span>
  

