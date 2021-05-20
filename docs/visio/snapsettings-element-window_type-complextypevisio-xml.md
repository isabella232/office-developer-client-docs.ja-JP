---
title: SnapSettings 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540316"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a><span data-ttu-id="f53e3-103">SnapSettings 要素 (Window_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f53e3-103">SnapSettings element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f53e3-104">ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="f53e3-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f53e3-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="f53e3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f53e3-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f53e3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f53e3-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="f53e3-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f53e3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f53e3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f53e3-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f53e3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f53e3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f53e3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f53e3-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="f53e3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f53e3-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="f53e3-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f53e3-113">定義</span><span class="sxs-lookup"><span data-stu-id="f53e3-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f53e3-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f53e3-114">Elements and attributes</span></span>

<span data-ttu-id="f53e3-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f53e3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f53e3-116">親要素</span><span class="sxs-lookup"><span data-stu-id="f53e3-116">Parent elements</span></span>

|<span data-ttu-id="f53e3-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="f53e3-117">**Element**</span></span>|<span data-ttu-id="f53e3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="f53e3-118">**Type**</span></span>|<span data-ttu-id="f53e3-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f53e3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f53e3-120">Window</span><span class="sxs-lookup"><span data-stu-id="f53e3-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f53e3-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="f53e3-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f53e3-122">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="f53e3-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f53e3-123">子要素</span><span class="sxs-lookup"><span data-stu-id="f53e3-123">Child elements</span></span>

<span data-ttu-id="f53e3-124">なし。</span><span class="sxs-lookup"><span data-stu-id="f53e3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f53e3-125">属性</span><span class="sxs-lookup"><span data-stu-id="f53e3-125">Attributes</span></span>

<span data-ttu-id="f53e3-126">なし。</span><span class="sxs-lookup"><span data-stu-id="f53e3-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f53e3-127">注釈</span><span class="sxs-lookup"><span data-stu-id="f53e3-127">Remarks</span></span>

<span data-ttu-id="f53e3-128">値は、次の表の値の合計である場合があります。</span><span class="sxs-lookup"><span data-stu-id="f53e3-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="f53e3-129">**値**</span><span class="sxs-lookup"><span data-stu-id="f53e3-129">**Value**</span></span>|<span data-ttu-id="f53e3-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="f53e3-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f53e3-131">0</span><span class="sxs-lookup"><span data-stu-id="f53e3-131">0</span></span>  <br/> |<span data-ttu-id="f53e3-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="f53e3-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="f53e3-133">1</span><span class="sxs-lookup"><span data-stu-id="f53e3-133">1</span></span>  <br/> |<span data-ttu-id="f53e3-134">スナップサブディビジョンに設定します。</span><span class="sxs-lookup"><span data-stu-id="f53e3-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="f53e3-135">2</span><span class="sxs-lookup"><span data-stu-id="f53e3-135">2</span></span>  <br/> |<span data-ttu-id="f53e3-136">スナップグリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="f53e3-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="f53e3-137">4</span><span class="sxs-lookup"><span data-stu-id="f53e3-137">4</span></span>  <br/> |<span data-ttu-id="f53e3-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="f53e3-139">8</span><span class="sxs-lookup"><span data-stu-id="f53e3-139">8</span></span>  <br/> |<span data-ttu-id="f53e3-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="f53e3-141">16 </span><span class="sxs-lookup"><span data-stu-id="f53e3-141">16</span></span>  <br/> |<span data-ttu-id="f53e3-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="f53e3-143">32</span><span class="sxs-lookup"><span data-stu-id="f53e3-143">32</span></span>  <br/> |<span data-ttu-id="f53e3-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="f53e3-145">256</span><span class="sxs-lookup"><span data-stu-id="f53e3-145">256</span></span>  <br/> |<span data-ttu-id="f53e3-146">スナップ図形の可視エッジに対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="f53e3-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="f53e3-147">512</span><span class="sxs-lookup"><span data-stu-id="f53e3-147">512</span></span>  <br/> |<span data-ttu-id="f53e3-148">スナップボックスに配置します。</span><span class="sxs-lookup"><span data-stu-id="f53e3-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="f53e3-149">1024</span><span class="sxs-lookup"><span data-stu-id="f53e3-149">1024</span></span>  <br/> |<span data-ttu-id="f53e3-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="f53e3-151">32768</span><span class="sxs-lookup"><span data-stu-id="f53e3-151">32768</span></span>  <br/> |<span data-ttu-id="f53e3-152">スナップ無効です。</span><span class="sxs-lookup"><span data-stu-id="f53e3-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="f53e3-153">65536</span><span class="sxs-lookup"><span data-stu-id="f53e3-153">65536</span></span>  <br/> |<span data-ttu-id="f53e3-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="f53e3-154">Snap to intersections.</span></span>  <br/> |
   

