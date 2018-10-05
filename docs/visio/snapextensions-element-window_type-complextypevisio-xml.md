---
title: SnapExtensions 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: 特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。 値は、次の表の値の合計を指定できます。
ms.openlocfilehash: 57fde520d3dc8e0582c0062a599d5f38a73169b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394406"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="d59c8-104">SnapExtensions 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="d59c8-104">SnapExtensions element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d59c8-105">特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d59c8-105">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> <span data-ttu-id="d59c8-106">値は、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d59c8-106">The value can be a sum of the values in the following table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d59c8-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="d59c8-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d59c8-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="d59c8-108">**Element type**</span></span> <br/> |[<span data-ttu-id="d59c8-109">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="d59c8-109">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d59c8-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="d59c8-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d59c8-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d59c8-111">**Schema file**</span></span> <br/> |<span data-ttu-id="d59c8-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d59c8-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d59c8-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="d59c8-113">**Document parts**</span></span> <br/> |<span data-ttu-id="d59c8-114">windows.xml</span><span class="sxs-lookup"><span data-stu-id="d59c8-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d59c8-115">定義</span><span class="sxs-lookup"><span data-stu-id="d59c8-115">Definition</span></span>

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d59c8-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d59c8-116">Elements and attributes</span></span>

<span data-ttu-id="d59c8-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d59c8-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d59c8-118">親要素</span><span class="sxs-lookup"><span data-stu-id="d59c8-118">Parent elements</span></span>

|<span data-ttu-id="d59c8-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="d59c8-119">**Element**</span></span>|<span data-ttu-id="d59c8-120">**型**</span><span class="sxs-lookup"><span data-stu-id="d59c8-120">**Type**</span></span>|<span data-ttu-id="d59c8-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="d59c8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d59c8-122">Window</span><span class="sxs-lookup"><span data-stu-id="d59c8-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d59c8-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="d59c8-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a><span data-ttu-id="d59c8-124">子要素</span><span class="sxs-lookup"><span data-stu-id="d59c8-124">Child elements</span></span>

<span data-ttu-id="d59c8-125">なし。</span><span class="sxs-lookup"><span data-stu-id="d59c8-125">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d59c8-126">属性</span><span class="sxs-lookup"><span data-stu-id="d59c8-126">Attributes</span></span>

<span data-ttu-id="d59c8-127">なし。</span><span class="sxs-lookup"><span data-stu-id="d59c8-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d59c8-128">備考</span><span class="sxs-lookup"><span data-stu-id="d59c8-128">Remarks</span></span>

<span data-ttu-id="d59c8-129">**SnapExtensions**要素の値は、次の表の値の合計にできます。</span><span class="sxs-lookup"><span data-stu-id="d59c8-129">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="d59c8-130">**値**</span><span class="sxs-lookup"><span data-stu-id="d59c8-130">**Value**</span></span>|<span data-ttu-id="d59c8-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="d59c8-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d59c8-132">0</span><span class="sxs-lookup"><span data-stu-id="d59c8-132">0</span></span>  <br/> |<span data-ttu-id="d59c8-133">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="d59c8-133">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="d59c8-134">1</span><span class="sxs-lookup"><span data-stu-id="d59c8-134">1</span></span>  <br/> |<span data-ttu-id="d59c8-135">配置ボックスの拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-135">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-136">2</span><span class="sxs-lookup"><span data-stu-id="d59c8-136">2</span></span>  <br/> |<span data-ttu-id="d59c8-137">軸の拡張機能を中心にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-137">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-138">4</span><span class="sxs-lookup"><span data-stu-id="d59c8-138">4</span></span>  <br/> |<span data-ttu-id="d59c8-139">カーブ正接の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-139">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-140">8</span><span class="sxs-lookup"><span data-stu-id="d59c8-140">8</span></span>  <br/> |<span data-ttu-id="d59c8-141">拡張子の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-141">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-142">16</span><span class="sxs-lookup"><span data-stu-id="d59c8-142">16</span></span>  <br/> |<span data-ttu-id="d59c8-143">拡張子の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-143">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-144">32</span><span class="sxs-lookup"><span data-stu-id="d59c8-144">32</span></span>  <br/> |<span data-ttu-id="d59c8-145">線形拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-145">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-146">64</span><span class="sxs-lookup"><span data-stu-id="d59c8-146">64</span></span>  <br/> |<span data-ttu-id="d59c8-147">拡張子のカーブにスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-147">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-148"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="d59c8-148">128</span></span>  <br/> |<span data-ttu-id="d59c8-149">端点の垂直な拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-149">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-150">256</span><span class="sxs-lookup"><span data-stu-id="d59c8-150">256</span></span>  <br/> |<span data-ttu-id="d59c8-151">垂直な拡張機能の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-151">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-152">512</span><span class="sxs-lookup"><span data-stu-id="d59c8-152">512</span></span>  <br/> |<span data-ttu-id="d59c8-153">水平引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-153">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-154">1024</span><span class="sxs-lookup"><span data-stu-id="d59c8-154">1024</span></span>  <br/> |<span data-ttu-id="d59c8-155">垂直引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-155">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-156">2048</span><span class="sxs-lookup"><span data-stu-id="d59c8-156">2048</span></span>  <br/> |<span data-ttu-id="d59c8-157">楕円の中心の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-157">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="d59c8-158">4096</span><span class="sxs-lookup"><span data-stu-id="d59c8-158">4096</span></span>  <br/> |<span data-ttu-id="d59c8-159">等角図の角度の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="d59c8-159">Snap to isometric angles extension.</span></span>  <br/> |
   

