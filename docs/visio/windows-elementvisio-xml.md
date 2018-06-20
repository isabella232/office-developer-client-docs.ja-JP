---
title: Windows 要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: ドキュメントのウィンドウの要素が含まれています。
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806788"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="22206-103">Windows 要素 ' Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="22206-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="22206-104">ドキュメントの**ウィンドウ**の要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="22206-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="22206-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="22206-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22206-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="22206-106">**Element type**</span></span> <br/> |[<span data-ttu-id="22206-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="22206-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="22206-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="22206-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="22206-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="22206-109">**Schema file**</span></span> <br/> |<span data-ttu-id="22206-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="22206-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="22206-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="22206-111">**Document parts**</span></span> <br/> |<span data-ttu-id="22206-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="22206-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="22206-113">定義</span><span class="sxs-lookup"><span data-stu-id="22206-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="22206-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="22206-114">Elements and attributes</span></span>

<span data-ttu-id="22206-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="22206-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="22206-116">親要素</span><span class="sxs-lookup"><span data-stu-id="22206-116">Parent elements</span></span>

<span data-ttu-id="22206-117">なし。</span><span class="sxs-lookup"><span data-stu-id="22206-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22206-118">子要素</span><span class="sxs-lookup"><span data-stu-id="22206-118">Child elements</span></span>

|<span data-ttu-id="22206-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="22206-119">**Element**</span></span>|<span data-ttu-id="22206-120">**型**</span><span class="sxs-lookup"><span data-stu-id="22206-120">**Type**</span></span>|<span data-ttu-id="22206-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="22206-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22206-122">Window</span><span class="sxs-lookup"><span data-stu-id="22206-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="22206-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="22206-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="22206-124">Microsoft Visio のインスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="22206-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="22206-125">属性</span><span class="sxs-lookup"><span data-stu-id="22206-125">Attributes</span></span>

|<span data-ttu-id="22206-126">**属性**</span><span class="sxs-lookup"><span data-stu-id="22206-126">**Attribute**</span></span>|<span data-ttu-id="22206-127">**型**</span><span class="sxs-lookup"><span data-stu-id="22206-127">**Type**</span></span>|<span data-ttu-id="22206-128">**必須**</span><span class="sxs-lookup"><span data-stu-id="22206-128">**Required**</span></span>|<span data-ttu-id="22206-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="22206-129">**Description**</span></span>|<span data-ttu-id="22206-130">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="22206-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22206-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="22206-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="22206-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="22206-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="22206-133">省略可能</span><span class="sxs-lookup"><span data-stu-id="22206-133">optional</span></span>  <br/> |<span data-ttu-id="22206-134">表示領域の高さを表します</span><span class="sxs-lookup"><span data-stu-id="22206-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="22206-135">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22206-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="22206-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="22206-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="22206-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="22206-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="22206-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="22206-138">optional</span></span>  <br/> |<span data-ttu-id="22206-139">表示領域の幅の寸法を表す</span><span class="sxs-lookup"><span data-stu-id="22206-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="22206-140">Xsd:unsignedShort の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22206-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

