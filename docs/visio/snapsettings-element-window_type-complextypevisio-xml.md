---
title: SnapSettings 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: 図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385208"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="c5084-103">SnapSettings 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="c5084-103">SnapSettings element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c5084-104">図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="c5084-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5084-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="c5084-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5084-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="c5084-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5084-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="c5084-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5084-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="c5084-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5084-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="c5084-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5084-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5084-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5084-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="c5084-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c5084-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="c5084-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5084-113">定義</span><span class="sxs-lookup"><span data-stu-id="c5084-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5084-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="c5084-114">Elements and attributes</span></span>

<span data-ttu-id="c5084-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5084-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5084-116">親要素</span><span class="sxs-lookup"><span data-stu-id="c5084-116">Parent elements</span></span>

|<span data-ttu-id="c5084-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="c5084-117">**Element**</span></span>|<span data-ttu-id="c5084-118">**型**</span><span class="sxs-lookup"><span data-stu-id="c5084-118">**Type**</span></span>|<span data-ttu-id="c5084-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5084-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5084-120">Window</span><span class="sxs-lookup"><span data-stu-id="c5084-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c5084-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="c5084-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5084-122">Microsoft Visio インスタンスで開いているウィンドウを表します。
</span><span class="sxs-lookup"><span data-stu-id="c5084-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5084-123">子要素</span><span class="sxs-lookup"><span data-stu-id="c5084-123">Child elements</span></span>

<span data-ttu-id="c5084-124">なし。</span><span class="sxs-lookup"><span data-stu-id="c5084-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5084-125">属性</span><span class="sxs-lookup"><span data-stu-id="c5084-125">Attributes</span></span>

<span data-ttu-id="c5084-126">なし。</span><span class="sxs-lookup"><span data-stu-id="c5084-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5084-127">備考</span><span class="sxs-lookup"><span data-stu-id="c5084-127">Remarks</span></span>

<span data-ttu-id="c5084-128">次の表の値の合計値があります。</span><span class="sxs-lookup"><span data-stu-id="c5084-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="c5084-129">**値**</span><span class="sxs-lookup"><span data-stu-id="c5084-129">**Value**</span></span>|<span data-ttu-id="c5084-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5084-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5084-131">0</span><span class="sxs-lookup"><span data-stu-id="c5084-131">0</span></span>  <br/> |<span data-ttu-id="c5084-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="c5084-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="c5084-133">1</span><span class="sxs-lookup"><span data-stu-id="c5084-133">1</span></span>  <br/> |<span data-ttu-id="c5084-134">ルーラーの目盛りにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="c5084-135">2</span><span class="sxs-lookup"><span data-stu-id="c5084-135">2</span></span>  <br/> |<span data-ttu-id="c5084-136">グリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="c5084-137">4</span><span class="sxs-lookup"><span data-stu-id="c5084-137">4</span></span>  <br/> |<span data-ttu-id="c5084-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="c5084-139">8</span><span class="sxs-lookup"><span data-stu-id="c5084-139">8</span></span>  <br/> |<span data-ttu-id="c5084-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="c5084-141">16</span><span class="sxs-lookup"><span data-stu-id="c5084-141">16</span></span>  <br/> |<span data-ttu-id="c5084-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="c5084-143">32</span><span class="sxs-lookup"><span data-stu-id="c5084-143">32</span></span>  <br/> |<span data-ttu-id="c5084-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="c5084-145">256</span><span class="sxs-lookup"><span data-stu-id="c5084-145">256</span></span>  <br/> |<span data-ttu-id="c5084-146">図形の可視のエッジにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="c5084-147">512</span><span class="sxs-lookup"><span data-stu-id="c5084-147">512</span></span>  <br/> |<span data-ttu-id="c5084-148">図形枠にスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="c5084-149">1024</span><span class="sxs-lookup"><span data-stu-id="c5084-149">1024</span></span>  <br/> |<span data-ttu-id="c5084-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="c5084-151">32768</span><span class="sxs-lookup"><span data-stu-id="c5084-151">32768</span></span>  <br/> |<span data-ttu-id="c5084-152">スナップが無効になります。</span><span class="sxs-lookup"><span data-stu-id="c5084-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="c5084-153">65536</span><span class="sxs-lookup"><span data-stu-id="c5084-153">65536</span></span>  <br/> |<span data-ttu-id="c5084-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="c5084-154">Snap to intersections.</span></span>  <br/> |
   

