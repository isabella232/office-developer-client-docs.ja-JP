---
title: SnapExtensions 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: 特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387616"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="67366-103">SnapExtensions 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="67366-103">SnapExtensions element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67366-104">特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="67366-104">Specifies whether a specific snap extension setting is enabled or disabled for the active window.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="67366-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="67366-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67366-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="67366-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67366-107">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="67366-107">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67366-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="67366-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67366-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="67366-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67366-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67366-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67366-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="67366-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67366-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="67366-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67366-113">定義</span><span class="sxs-lookup"><span data-stu-id="67366-113">Definition</span></span>

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67366-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="67366-114">Elements and attributes</span></span>

<span data-ttu-id="67366-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="67366-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67366-116">親要素</span><span class="sxs-lookup"><span data-stu-id="67366-116">Parent elements</span></span>

|<span data-ttu-id="67366-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="67366-117">**Element**</span></span>|<span data-ttu-id="67366-118">**型**</span><span class="sxs-lookup"><span data-stu-id="67366-118">**Type**</span></span>|<span data-ttu-id="67366-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="67366-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67366-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="67366-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67366-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="67366-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67366-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="67366-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67366-123">子要素</span><span class="sxs-lookup"><span data-stu-id="67366-123">Child elements</span></span>

<span data-ttu-id="67366-124">なし。</span><span class="sxs-lookup"><span data-stu-id="67366-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67366-125">属性</span><span class="sxs-lookup"><span data-stu-id="67366-125">Attributes</span></span>

<span data-ttu-id="67366-126">なし。</span><span class="sxs-lookup"><span data-stu-id="67366-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67366-127">備考</span><span class="sxs-lookup"><span data-stu-id="67366-127">Remarks</span></span>

<span data-ttu-id="67366-128">**SnapExtensions**要素の値は、次の表の値の合計にできます。</span><span class="sxs-lookup"><span data-stu-id="67366-128">The value of the **SnapExtensions** element can be a sum of the values in the following table.</span></span> 
  
|<span data-ttu-id="67366-129">**値**</span><span class="sxs-lookup"><span data-stu-id="67366-129">**Value**</span></span>|<span data-ttu-id="67366-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="67366-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67366-131">0</span><span class="sxs-lookup"><span data-stu-id="67366-131">0</span></span>  <br/> |<span data-ttu-id="67366-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="67366-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="67366-133">1</span><span class="sxs-lookup"><span data-stu-id="67366-133">1</span></span>  <br/> |<span data-ttu-id="67366-134">配置ボックスの拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-134">Snap to alignment box extension.</span></span>  <br/> |
|<span data-ttu-id="67366-135">2</span><span class="sxs-lookup"><span data-stu-id="67366-135">2</span></span>  <br/> |<span data-ttu-id="67366-136">軸の拡張機能を中心にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-136">Snap to center axis extension.</span></span>  <br/> |
|<span data-ttu-id="67366-137">4</span><span class="sxs-lookup"><span data-stu-id="67366-137">4</span></span>  <br/> |<span data-ttu-id="67366-138">カーブ正接の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-138">Snap to curve tangent extension.</span></span>  <br/> |
|<span data-ttu-id="67366-139">8</span><span class="sxs-lookup"><span data-stu-id="67366-139">8</span></span>  <br/> |<span data-ttu-id="67366-140">拡張子の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-140">Snap to endpoint extension.</span></span>  <br/> |
|<span data-ttu-id="67366-141">16</span><span class="sxs-lookup"><span data-stu-id="67366-141">16</span></span>  <br/> |<span data-ttu-id="67366-142">拡張子の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-142">Snap to midpoint extension.</span></span>  <br/> |
|<span data-ttu-id="67366-143">32</span><span class="sxs-lookup"><span data-stu-id="67366-143">32</span></span>  <br/> |<span data-ttu-id="67366-144">線形拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-144">Snap to linear extension.</span></span>  <br/> |
|<span data-ttu-id="67366-145">64</span><span class="sxs-lookup"><span data-stu-id="67366-145">64</span></span>  <br/> |<span data-ttu-id="67366-146">拡張子のカーブにスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-146">Snap to curve extension.</span></span>  <br/> |
|<span data-ttu-id="67366-147"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="67366-147">128</span></span>  <br/> |<span data-ttu-id="67366-148">端点の垂直な拡張子にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-148">Snap to endpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="67366-149">256</span><span class="sxs-lookup"><span data-stu-id="67366-149">256</span></span>  <br/> |<span data-ttu-id="67366-150">垂直な拡張機能の中間点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-150">Snap to midpoint perpendicular extension.</span></span>  <br/> |
|<span data-ttu-id="67366-151">512</span><span class="sxs-lookup"><span data-stu-id="67366-151">512</span></span>  <br/> |<span data-ttu-id="67366-152">水平引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-152">Snap to endpoint horizontal extension.</span></span>  <br/> |
|<span data-ttu-id="67366-153">1024</span><span class="sxs-lookup"><span data-stu-id="67366-153">1024</span></span>  <br/> |<span data-ttu-id="67366-154">垂直引き出し線の端点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-154">Snap to endpoint vertical extension.</span></span>  <br/> |
|<span data-ttu-id="67366-155">2048</span><span class="sxs-lookup"><span data-stu-id="67366-155">2048</span></span>  <br/> |<span data-ttu-id="67366-156">楕円の中心の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-156">Snap to ellipse center extension.</span></span>  <br/> |
|<span data-ttu-id="67366-157">4096</span><span class="sxs-lookup"><span data-stu-id="67366-157">4096</span></span>  <br/> |<span data-ttu-id="67366-158">等角図の角度の拡張機能にスナップします。</span><span class="sxs-lookup"><span data-stu-id="67366-158">Snap to isometric angles extension.</span></span>  <br/> |
   

