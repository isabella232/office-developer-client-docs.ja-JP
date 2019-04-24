---
title: Windows 要素 (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: 文書のウィンドウ要素を格納します。
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339824"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="a8bec-103">Windows 要素 (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a8bec-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="a8bec-104">文書の**ウィンドウ**要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="a8bec-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a8bec-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a8bec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8bec-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a8bec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a8bec-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="a8bec-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a8bec-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a8bec-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a8bec-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a8bec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a8bec-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="a8bec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a8bec-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a8bec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a8bec-112">windows .xml</span><span class="sxs-lookup"><span data-stu-id="a8bec-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a8bec-113">定義</span><span class="sxs-lookup"><span data-stu-id="a8bec-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a8bec-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a8bec-114">Elements and attributes</span></span>

<span data-ttu-id="a8bec-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8bec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a8bec-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a8bec-116">Parent elements</span></span>

<span data-ttu-id="a8bec-117">なし。</span><span class="sxs-lookup"><span data-stu-id="a8bec-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8bec-118">子要素</span><span class="sxs-lookup"><span data-stu-id="a8bec-118">Child elements</span></span>

|<span data-ttu-id="a8bec-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8bec-119">**Element**</span></span>|<span data-ttu-id="a8bec-120">**型**</span><span class="sxs-lookup"><span data-stu-id="a8bec-120">**Type**</span></span>|<span data-ttu-id="a8bec-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8bec-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a8bec-122">Window</span><span class="sxs-lookup"><span data-stu-id="a8bec-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a8bec-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="a8bec-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a8bec-124">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="a8bec-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a8bec-125">属性</span><span class="sxs-lookup"><span data-stu-id="a8bec-125">Attributes</span></span>

|<span data-ttu-id="a8bec-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="a8bec-126">**Attribute**</span></span>|<span data-ttu-id="a8bec-127">**型**</span><span class="sxs-lookup"><span data-stu-id="a8bec-127">**Type**</span></span>|<span data-ttu-id="a8bec-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="a8bec-128">**Required**</span></span>|<span data-ttu-id="a8bec-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8bec-129">**Description**</span></span>|<span data-ttu-id="a8bec-130">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a8bec-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8bec-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="a8bec-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="a8bec-132">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="a8bec-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a8bec-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="a8bec-133">optional</span></span>  <br/> |<span data-ttu-id="a8bec-134">表示領域の高さの次元を表します。</span><span class="sxs-lookup"><span data-stu-id="a8bec-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="a8bec-135">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="a8bec-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a8bec-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="a8bec-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="a8bec-137">xsd: アン signedshort</span><span class="sxs-lookup"><span data-stu-id="a8bec-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a8bec-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="a8bec-138">optional</span></span>  <br/> |<span data-ttu-id="a8bec-139">表示領域の幅の大きさを表します。</span><span class="sxs-lookup"><span data-stu-id="a8bec-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="a8bec-140">xsd: _ signedshort 型の値。</span><span class="sxs-lookup"><span data-stu-id="a8bec-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

