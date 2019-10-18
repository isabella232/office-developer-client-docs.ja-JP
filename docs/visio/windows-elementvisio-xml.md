---
title: Windows 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: ドキュメントの Window 要素が含まれます。
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538446"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="ab17d-103">Windows 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ab17d-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="ab17d-104">ドキュメントの **Window** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ab17d-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="ab17d-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="ab17d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab17d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="ab17d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ab17d-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="ab17d-107">Windows_Type complexType</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ab17d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ab17d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ab17d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="ab17d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ab17d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ab17d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ab17d-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="ab17d-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="ab17d-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="ab17d-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab17d-113">定義</span><span class="sxs-lookup"><span data-stu-id="ab17d-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ab17d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="ab17d-114">Elements and attributes</span></span>

<span data-ttu-id="ab17d-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab17d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ab17d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="ab17d-116">Parent elements</span></span>

<span data-ttu-id="ab17d-117">なし。</span><span class="sxs-lookup"><span data-stu-id="ab17d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab17d-118">子要素</span><span class="sxs-lookup"><span data-stu-id="ab17d-118">Child elements</span></span>

|<span data-ttu-id="ab17d-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab17d-119">**Element**</span></span>|<span data-ttu-id="ab17d-120">**型**</span><span class="sxs-lookup"><span data-stu-id="ab17d-120">**Type**</span></span>|<span data-ttu-id="ab17d-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab17d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab17d-122">Window</span><span class="sxs-lookup"><span data-stu-id="ab17d-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ab17d-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="ab17d-123">WindowType</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ab17d-124">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="ab17d-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ab17d-125">属性</span><span class="sxs-lookup"><span data-stu-id="ab17d-125">Attributes</span></span>

|<span data-ttu-id="ab17d-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="ab17d-126">**Attribute**</span></span>|<span data-ttu-id="ab17d-127">**型**</span><span class="sxs-lookup"><span data-stu-id="ab17d-127">**Type**</span></span>|<span data-ttu-id="ab17d-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="ab17d-128">**Required**</span></span>|<span data-ttu-id="ab17d-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab17d-129">**Description**</span></span>|<span data-ttu-id="ab17d-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="ab17d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab17d-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="ab17d-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="ab17d-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab17d-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab17d-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="ab17d-133">optional</span></span>  <br/> |<span data-ttu-id="ab17d-134">表示領域の高さの寸法を表します</span><span class="sxs-lookup"><span data-stu-id="ab17d-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="ab17d-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ab17d-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ab17d-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="ab17d-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="ab17d-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ab17d-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ab17d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="ab17d-138">optional</span></span>  <br/> |<span data-ttu-id="ab17d-139">表示領域の幅の寸法を表します</span><span class="sxs-lookup"><span data-stu-id="ab17d-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="ab17d-140">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="ab17d-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

