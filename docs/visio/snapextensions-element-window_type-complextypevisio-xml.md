---
title: SnapExtensions 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: 特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。 値は、次の表の値の合計を指定できます。
ms.openlocfilehash: 0fe9ce4060fbd6366a188e17ed716cb74034f375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806521"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="236c6-104">SnapExtensions 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="236c6-104">SnapExtensions element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="236c6-105">特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="236c6-105">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> <span data-ttu-id="236c6-106">値は、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="236c6-106">The value can be a sum of the values in the following table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="236c6-107">要素情報</span><span class="sxs-lookup"><span data-stu-id="236c6-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="236c6-108">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="236c6-108">**Element type**</span></span> <br/> |[<span data-ttu-id="236c6-109">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="236c6-109">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="236c6-110">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="236c6-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="236c6-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="236c6-111">**Schema file**</span></span> <br/> |<span data-ttu-id="236c6-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="236c6-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="236c6-113">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="236c6-113">**Document parts**</span></span> <br/> |<span data-ttu-id="236c6-114">windows.xml</span><span class="sxs-lookup"><span data-stu-id="236c6-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="236c6-115">定義</span><span class="sxs-lookup"><span data-stu-id="236c6-115">Definition</span></span>

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="236c6-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="236c6-116">Elements and attributes</span></span>

<span data-ttu-id="236c6-117">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="236c6-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="236c6-118">親要素</span><span class="sxs-lookup"><span data-stu-id="236c6-118">Parent elements</span></span>

|<span data-ttu-id="236c6-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="236c6-119">**Element**</span></span>|<span data-ttu-id="236c6-120">**型**</span><span class="sxs-lookup"><span data-stu-id="236c6-120">**Type**</span></span>|<span data-ttu-id="236c6-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="236c6-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="236c6-122">Window</span><span class="sxs-lookup"><span data-stu-id="236c6-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="236c6-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="236c6-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a><span data-ttu-id="236c6-124">子要素</span><span class="sxs-lookup"><span data-stu-id="236c6-124">Child elements</span></span>

<span data-ttu-id="236c6-125">なし。</span><span class="sxs-lookup"><span data-stu-id="236c6-125">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="236c6-126">属性</span><span class="sxs-lookup"><span data-stu-id="236c6-126">Attributes</span></span>

<span data-ttu-id="236c6-127">なし。</span><span class="sxs-lookup"><span data-stu-id="236c6-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="236c6-128">備考</span><span class="sxs-lookup"><span data-stu-id="236c6-128">Remarks</span></span>

<span data-ttu-id="236c6-129">**SnapExtensions**要素の値は、次の表の値の合計にできます。</span><span class="sxs-lookup"><span data-stu-id="236c6-129">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="236c6-130">**値**</span><span class="sxs-lookup"><span data-stu-id="236c6-130">**Value**</span></span>|<span data-ttu-id="236c6-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="236c6-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="236c6-132">0</span><span class="sxs-lookup"><span data-stu-id="236c6-132">0</span></span>  <br/> |<span data-ttu-id="236c6-133">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="236c6-133">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="236c6-134">1</span><span class="sxs-lookup"><span data-stu-id="236c6-134">1</span></span>  <br/> |<span data-ttu-id="236c6-135">配置ボックスの拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-135">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-136">2</span><span class="sxs-lookup"><span data-stu-id="236c6-136">2</span></span>  <br/> |<span data-ttu-id="236c6-137">軸の拡張機能を中心にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-137">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-138">4</span><span class="sxs-lookup"><span data-stu-id="236c6-138">4</span></span>  <br/> |<span data-ttu-id="236c6-139">カーブ正接の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-139">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-140">8</span><span class="sxs-lookup"><span data-stu-id="236c6-140">8</span></span>  <br/> |<span data-ttu-id="236c6-141">拡張子の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-141">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-142">16</span><span class="sxs-lookup"><span data-stu-id="236c6-142">16</span></span>  <br/> |<span data-ttu-id="236c6-143">拡張子の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-143">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-144">32</span><span class="sxs-lookup"><span data-stu-id="236c6-144">32</span></span>  <br/> |<span data-ttu-id="236c6-145">線形拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-145">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-146">64</span><span class="sxs-lookup"><span data-stu-id="236c6-146">64</span></span>  <br/> |<span data-ttu-id="236c6-147">拡張子のカーブにスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-147">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-148">128</span><span class="sxs-lookup"><span data-stu-id="236c6-148">128</span></span>  <br/> |<span data-ttu-id="236c6-149">端点の垂直な拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-149">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-150">256</span><span class="sxs-lookup"><span data-stu-id="236c6-150">256</span></span>  <br/> |<span data-ttu-id="236c6-151">垂直な拡張機能の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-151">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-152">512</span><span class="sxs-lookup"><span data-stu-id="236c6-152">512</span></span>  <br/> |<span data-ttu-id="236c6-153">水平引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-153">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-154">1024</span><span class="sxs-lookup"><span data-stu-id="236c6-154">1024</span></span>  <br/> |<span data-ttu-id="236c6-155">垂直引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-155">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-156">2048</span><span class="sxs-lookup"><span data-stu-id="236c6-156">2048</span></span>  <br/> |<span data-ttu-id="236c6-157">楕円の中心の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-157">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="236c6-158">4096</span><span class="sxs-lookup"><span data-stu-id="236c6-158">4096</span></span>  <br/> |<span data-ttu-id="236c6-159">等角図の角度の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="236c6-159">Snap to isometric angles extension.</span></span>  <br/> |
   

