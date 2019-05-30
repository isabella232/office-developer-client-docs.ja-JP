---
title: SnapExtensions 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。 この値には、次の表の値の合計を指定できます。
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540323"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="81e9a-104">SnapExtensions 要素 (Window_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="81e9a-104">SnapExtensions element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="81e9a-105">アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="81e9a-105">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> <span data-ttu-id="81e9a-106">この値には、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81e9a-106">The value can be a sum of the values in the following table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81e9a-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="81e9a-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81e9a-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="81e9a-108">**Element type**</span></span> <br/> |[<span data-ttu-id="81e9a-109">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="81e9a-109">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="81e9a-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="81e9a-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="81e9a-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="81e9a-111">**Schema file**</span></span> <br/> |<span data-ttu-id="81e9a-112">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="81e9a-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="81e9a-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="81e9a-113">**Document parts**</span></span> <br/> |<span data-ttu-id="81e9a-114">windows .xml</span><span class="sxs-lookup"><span data-stu-id="81e9a-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81e9a-115">定義</span><span class="sxs-lookup"><span data-stu-id="81e9a-115">Definition</span></span>

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="81e9a-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="81e9a-116">Elements and attributes</span></span>

<span data-ttu-id="81e9a-117">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="81e9a-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="81e9a-118">親要素</span><span class="sxs-lookup"><span data-stu-id="81e9a-118">Parent elements</span></span>

|<span data-ttu-id="81e9a-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="81e9a-119">**Element**</span></span>|<span data-ttu-id="81e9a-120">**型**</span><span class="sxs-lookup"><span data-stu-id="81e9a-120">**Type**</span></span>|<span data-ttu-id="81e9a-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="81e9a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81e9a-122">Window</span><span class="sxs-lookup"><span data-stu-id="81e9a-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81e9a-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="81e9a-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a><span data-ttu-id="81e9a-124">子要素</span><span class="sxs-lookup"><span data-stu-id="81e9a-124">Child elements</span></span>

<span data-ttu-id="81e9a-125">なし。</span><span class="sxs-lookup"><span data-stu-id="81e9a-125">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81e9a-126">属性</span><span class="sxs-lookup"><span data-stu-id="81e9a-126">Attributes</span></span>

<span data-ttu-id="81e9a-127">なし。</span><span class="sxs-lookup"><span data-stu-id="81e9a-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81e9a-128">注釈</span><span class="sxs-lookup"><span data-stu-id="81e9a-128">Remarks</span></span>

<span data-ttu-id="81e9a-129">**Snapextensions**要素の値には、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81e9a-129">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="81e9a-130">**値**</span><span class="sxs-lookup"><span data-stu-id="81e9a-130">**Value**</span></span>|<span data-ttu-id="81e9a-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="81e9a-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81e9a-132">.0</span><span class="sxs-lookup"><span data-stu-id="81e9a-132">0</span></span>  <br/> |<span data-ttu-id="81e9a-133">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="81e9a-133">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="81e9a-134">1-d</span><span class="sxs-lookup"><span data-stu-id="81e9a-134">1</span></span>  <br/> |<span data-ttu-id="81e9a-135">図形枠の補助線にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-135">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-136">pbm-2</span><span class="sxs-lookup"><span data-stu-id="81e9a-136">2</span></span>  <br/> |<span data-ttu-id="81e9a-137">中央軸の拡張位置にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-137">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-138">2/4</span><span class="sxs-lookup"><span data-stu-id="81e9a-138">4</span></span>  <br/> |<span data-ttu-id="81e9a-139">曲線正接拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-139">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-140">8 </span><span class="sxs-lookup"><span data-stu-id="81e9a-140">8</span></span>  <br/> |<span data-ttu-id="81e9a-141">エンドポイント拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-141">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-142">16</span><span class="sxs-lookup"><span data-stu-id="81e9a-142">16</span></span>  <br/> |<span data-ttu-id="81e9a-143">中点拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-143">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-144">32</span><span class="sxs-lookup"><span data-stu-id="81e9a-144">32</span></span>  <br/> |<span data-ttu-id="81e9a-145">直線の延長形にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-145">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-146">64</span><span class="sxs-lookup"><span data-stu-id="81e9a-146">64</span></span>  <br/> |<span data-ttu-id="81e9a-147">曲線拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-147">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-148">128</span><span class="sxs-lookup"><span data-stu-id="81e9a-148">128</span></span>  <br/> |<span data-ttu-id="81e9a-149">端点の垂直拡張線にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-149">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-150">256</span><span class="sxs-lookup"><span data-stu-id="81e9a-150">256</span></span>  <br/> |<span data-ttu-id="81e9a-151">中点の垂線拡張にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-151">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-152">512</span><span class="sxs-lookup"><span data-stu-id="81e9a-152">512</span></span>  <br/> |<span data-ttu-id="81e9a-153">端点の水平方向の拡張位置にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-153">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-154">1024</span><span class="sxs-lookup"><span data-stu-id="81e9a-154">1024</span></span>  <br/> |<span data-ttu-id="81e9a-155">端点の垂直方向の拡張位置にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-155">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-156">2048</span><span class="sxs-lookup"><span data-stu-id="81e9a-156">2048</span></span>  <br/> |<span data-ttu-id="81e9a-157">楕円形の中央拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-157">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="81e9a-158">4096</span><span class="sxs-lookup"><span data-stu-id="81e9a-158">4096</span></span>  <br/> |<span data-ttu-id="81e9a-159">等角投影の角度の拡張にスナップします。</span><span class="sxs-lookup"><span data-stu-id="81e9a-159">Snap to isometric angles extension.</span></span>  <br/> |
   

