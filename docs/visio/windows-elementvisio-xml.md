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
# <a name="windows-element-visio-xml"></a><span data-ttu-id="76382-103">Windows 要素 (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="76382-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="76382-104">ドキュメントの **Window** 要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76382-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="76382-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="76382-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76382-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="76382-106">**Element type**</span></span> <br/> |[<span data-ttu-id="76382-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="76382-107">Windows_Type complexType</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="76382-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="76382-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="76382-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="76382-109">**Schema file**</span></span> <br/> |<span data-ttu-id="76382-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="76382-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="76382-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="76382-111">\*\*\*\* Document parts and themes</span></span> <br/> |<span data-ttu-id="76382-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="76382-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="76382-113">定義</span><span class="sxs-lookup"><span data-stu-id="76382-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="76382-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="76382-114">Elements and attributes</span></span>

<span data-ttu-id="76382-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76382-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**,
    **maxOccurs**, and
    **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="76382-116">親要素</span><span class="sxs-lookup"><span data-stu-id="76382-116">Parent elements</span></span>

<span data-ttu-id="76382-117">なし。</span><span class="sxs-lookup"><span data-stu-id="76382-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76382-118">子要素</span><span class="sxs-lookup"><span data-stu-id="76382-118">Child elements</span></span>

|<span data-ttu-id="76382-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="76382-119">**Element**</span></span>|<span data-ttu-id="76382-120">**型**</span><span class="sxs-lookup"><span data-stu-id="76382-120">**Type**</span></span>|<span data-ttu-id="76382-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="76382-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="76382-122">Window</span><span class="sxs-lookup"><span data-stu-id="76382-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="76382-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="76382-123">WindowType</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="76382-124">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="76382-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="76382-125">属性</span><span class="sxs-lookup"><span data-stu-id="76382-125">Attributes</span></span>

|<span data-ttu-id="76382-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="76382-126">**Attribute**</span></span>|<span data-ttu-id="76382-127">**型**</span><span class="sxs-lookup"><span data-stu-id="76382-127">**Type**</span></span>|<span data-ttu-id="76382-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="76382-128">**Required**</span></span>|<span data-ttu-id="76382-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="76382-129">**Description**</span></span>|<span data-ttu-id="76382-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="76382-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="76382-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="76382-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="76382-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="76382-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="76382-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="76382-133">optional</span></span>  <br/> |<span data-ttu-id="76382-134">表示領域の高さの寸法を表します</span><span class="sxs-lookup"><span data-stu-id="76382-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="76382-135">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="76382-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="76382-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="76382-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="76382-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="76382-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="76382-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="76382-138">optional</span></span>  <br/> |<span data-ttu-id="76382-139">表示領域の幅の寸法を表します</span><span class="sxs-lookup"><span data-stu-id="76382-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="76382-140">xsd:unsignedShort 型の値。</span><span class="sxs-lookup"><span data-stu-id="76382-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

