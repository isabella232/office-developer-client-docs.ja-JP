---
title: SnapExtensions 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。 値には、次の表の値の合計を指定できます。
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540323"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a><span data-ttu-id="17497-104">SnapExtensions 要素 (Window_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="17497-104">SnapExtensions element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="17497-105">アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="17497-105">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> <span data-ttu-id="17497-106">値には、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="17497-106">The value can be a sum of the values in the following table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17497-107">要素の情報</span><span class="sxs-lookup"><span data-stu-id="17497-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17497-108">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="17497-108">**Element type**</span></span> <br/> |[<span data-ttu-id="17497-109">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="17497-109">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17497-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17497-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17497-111">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="17497-111">**Schema file**</span></span> <br/> |<span data-ttu-id="17497-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17497-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17497-113">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="17497-113">**Document parts**</span></span> <br/> |<span data-ttu-id="17497-114">windows.xml</span><span class="sxs-lookup"><span data-stu-id="17497-114">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17497-115">定義</span><span class="sxs-lookup"><span data-stu-id="17497-115">Definition</span></span>

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17497-116">要素と属性</span><span class="sxs-lookup"><span data-stu-id="17497-116">Elements and attributes</span></span>

<span data-ttu-id="17497-117">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17497-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17497-118">親要素</span><span class="sxs-lookup"><span data-stu-id="17497-118">Parent elements</span></span>

|<span data-ttu-id="17497-119">**要素**</span><span class="sxs-lookup"><span data-stu-id="17497-119">**Element**</span></span>|<span data-ttu-id="17497-120">**型**</span><span class="sxs-lookup"><span data-stu-id="17497-120">**Type**</span></span>|<span data-ttu-id="17497-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="17497-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17497-122">Window</span><span class="sxs-lookup"><span data-stu-id="17497-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17497-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="17497-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a><span data-ttu-id="17497-124">子要素</span><span class="sxs-lookup"><span data-stu-id="17497-124">Child elements</span></span>

<span data-ttu-id="17497-125">なし。</span><span class="sxs-lookup"><span data-stu-id="17497-125">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17497-126">属性</span><span class="sxs-lookup"><span data-stu-id="17497-126">Attributes</span></span>

<span data-ttu-id="17497-127">なし。</span><span class="sxs-lookup"><span data-stu-id="17497-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17497-128">注釈</span><span class="sxs-lookup"><span data-stu-id="17497-128">Remarks</span></span>

<span data-ttu-id="17497-129">**SnapExtensions** 要素の値は、次の表の値の合計になります。</span><span class="sxs-lookup"><span data-stu-id="17497-129">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="17497-130">**値**</span><span class="sxs-lookup"><span data-stu-id="17497-130">**Value**</span></span>|<span data-ttu-id="17497-131">**説明**</span><span class="sxs-lookup"><span data-stu-id="17497-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17497-132">0</span><span class="sxs-lookup"><span data-stu-id="17497-132">0</span></span>  <br/> |<span data-ttu-id="17497-133">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="17497-133">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="17497-134">1</span><span class="sxs-lookup"><span data-stu-id="17497-134">1</span></span>  <br/> |<span data-ttu-id="17497-135">スナップボックスの拡張子に変更します。</span><span class="sxs-lookup"><span data-stu-id="17497-135">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="17497-136">2</span><span class="sxs-lookup"><span data-stu-id="17497-136">2</span></span>  <br/> |<span data-ttu-id="17497-137">スナップ軸の拡張子に移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-137">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="17497-138">4</span><span class="sxs-lookup"><span data-stu-id="17497-138">4</span></span>  <br/> |<span data-ttu-id="17497-139">スナップ接線の延長に移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-139">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="17497-140">8</span><span class="sxs-lookup"><span data-stu-id="17497-140">8</span></span>  <br/> |<span data-ttu-id="17497-141">スナップエンドポイント拡張機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="17497-141">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="17497-142">16 </span><span class="sxs-lookup"><span data-stu-id="17497-142">16</span></span>  <br/> |<span data-ttu-id="17497-143">スナップ中点の拡張子に変更します。</span><span class="sxs-lookup"><span data-stu-id="17497-143">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="17497-144">32</span><span class="sxs-lookup"><span data-stu-id="17497-144">32</span></span>  <br/> |<span data-ttu-id="17497-145">スナップの拡張を指定します。</span><span class="sxs-lookup"><span data-stu-id="17497-145">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="17497-146">64</span><span class="sxs-lookup"><span data-stu-id="17497-146">64</span></span>  <br/> |<span data-ttu-id="17497-147">スナップに移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-147">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="17497-148">128</span><span class="sxs-lookup"><span data-stu-id="17497-148">128</span></span>  <br/> |<span data-ttu-id="17497-149">スナップ垂直な拡張子に移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-149">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="17497-150">256</span><span class="sxs-lookup"><span data-stu-id="17497-150">256</span></span>  <br/> |<span data-ttu-id="17497-151">スナップ垂直な拡張に移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-151">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="17497-152">512</span><span class="sxs-lookup"><span data-stu-id="17497-152">512</span></span>  <br/> |<span data-ttu-id="17497-153">スナップの拡張をエンドポイントに移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-153">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="17497-154">1024</span><span class="sxs-lookup"><span data-stu-id="17497-154">1024</span></span>  <br/> |<span data-ttu-id="17497-155">スナップ垂直方向の拡張機能に移動します。</span><span class="sxs-lookup"><span data-stu-id="17497-155">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="17497-156">2048</span><span class="sxs-lookup"><span data-stu-id="17497-156">2048</span></span>  <br/> |<span data-ttu-id="17497-157">スナップ中心の拡張子に変換します。</span><span class="sxs-lookup"><span data-stu-id="17497-157">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="17497-158">4096</span><span class="sxs-lookup"><span data-stu-id="17497-158">4096</span></span>  <br/> |<span data-ttu-id="17497-159">スナップ等角角度の拡張を指定します。</span><span class="sxs-lookup"><span data-stu-id="17497-159">Snap to isometric angles extension.</span></span>  <br/> |
   

