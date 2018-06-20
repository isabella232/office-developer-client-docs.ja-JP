---
title: SnapSettings 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: 図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
ms.openlocfilehash: 55558301b1f85f70f723d4282b438e4883d90c25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806526"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="5b2f5-103">SnapSettings 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="5b2f5-103">SnapSettings element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5b2f5-104">図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b2f5-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="5b2f5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b2f5-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5b2f5-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="5b2f5-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5b2f5-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5b2f5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5b2f5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5b2f5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5b2f5-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5b2f5-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="5b2f5-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5b2f5-113">定義</span><span class="sxs-lookup"><span data-stu-id="5b2f5-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5b2f5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="5b2f5-114">Elements and attributes</span></span>

<span data-ttu-id="5b2f5-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5b2f5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="5b2f5-116">Parent elements</span></span>

|<span data-ttu-id="5b2f5-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-117">**Element**</span></span>|<span data-ttu-id="5b2f5-118">**型**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-118">**Type**</span></span>|<span data-ttu-id="5b2f5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b2f5-120">Window</span><span class="sxs-lookup"><span data-stu-id="5b2f5-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5b2f5-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="5b2f5-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5b2f5-122">Microsoft Visio のインスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b2f5-123">子要素</span><span class="sxs-lookup"><span data-stu-id="5b2f5-123">Child elements</span></span>

<span data-ttu-id="5b2f5-124">なし。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b2f5-125">属性</span><span class="sxs-lookup"><span data-stu-id="5b2f5-125">Attributes</span></span>

<span data-ttu-id="5b2f5-126">なし。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b2f5-127">備考</span><span class="sxs-lookup"><span data-stu-id="5b2f5-127">Remarks</span></span>

<span data-ttu-id="5b2f5-128">次の表の値の合計値があります。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="5b2f5-129">**値**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-129">**Value**</span></span>|<span data-ttu-id="5b2f5-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b2f5-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b2f5-131">0</span><span class="sxs-lookup"><span data-stu-id="5b2f5-131">0</span></span>  <br/> |<span data-ttu-id="5b2f5-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-133">1</span><span class="sxs-lookup"><span data-stu-id="5b2f5-133">1</span></span>  <br/> |<span data-ttu-id="5b2f5-134">ルーラーの目盛りにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-135">2</span><span class="sxs-lookup"><span data-stu-id="5b2f5-135">2</span></span>  <br/> |<span data-ttu-id="5b2f5-136">グリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-137">4</span><span class="sxs-lookup"><span data-stu-id="5b2f5-137">4</span></span>  <br/> |<span data-ttu-id="5b2f5-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-139">8</span><span class="sxs-lookup"><span data-stu-id="5b2f5-139">8</span></span>  <br/> |<span data-ttu-id="5b2f5-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-141">16</span><span class="sxs-lookup"><span data-stu-id="5b2f5-141">16</span></span>  <br/> |<span data-ttu-id="5b2f5-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-143">32</span><span class="sxs-lookup"><span data-stu-id="5b2f5-143">32</span></span>  <br/> |<span data-ttu-id="5b2f5-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-145">256</span><span class="sxs-lookup"><span data-stu-id="5b2f5-145">256</span></span>  <br/> |<span data-ttu-id="5b2f5-146">図形の可視のエッジにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-147">512</span><span class="sxs-lookup"><span data-stu-id="5b2f5-147">512</span></span>  <br/> |<span data-ttu-id="5b2f5-148">図形枠にスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-149">1024</span><span class="sxs-lookup"><span data-stu-id="5b2f5-149">1024</span></span>  <br/> |<span data-ttu-id="5b2f5-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-151">32768</span><span class="sxs-lookup"><span data-stu-id="5b2f5-151">32768</span></span>  <br/> |<span data-ttu-id="5b2f5-152">スナップが無効になります。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="5b2f5-153">65536</span><span class="sxs-lookup"><span data-stu-id="5b2f5-153">65536</span></span>  <br/> |<span data-ttu-id="5b2f5-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="5b2f5-154">Snap to intersections.</span></span>  <br/> |
   

