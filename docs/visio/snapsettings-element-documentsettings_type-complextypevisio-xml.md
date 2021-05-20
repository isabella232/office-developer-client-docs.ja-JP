---
title: SnapSettings 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540295"
---
# <a name="snapsettings-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="573b5-103">SnapSettings 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="573b5-103">SnapSettings element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="573b5-104">ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="573b5-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="573b5-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="573b5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="573b5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="573b5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="573b5-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="573b5-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="573b5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="573b5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="573b5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="573b5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="573b5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="573b5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="573b5-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="573b5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="573b5-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="573b5-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="573b5-113">定義</span><span class="sxs-lookup"><span data-stu-id="573b5-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="573b5-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="573b5-114">Elements and attributes</span></span>

<span data-ttu-id="573b5-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="573b5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="573b5-116">親要素</span><span class="sxs-lookup"><span data-stu-id="573b5-116">Parent elements</span></span>

|<span data-ttu-id="573b5-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="573b5-117">**Element**</span></span>|<span data-ttu-id="573b5-118">**型**</span><span class="sxs-lookup"><span data-stu-id="573b5-118">**Type**</span></span>|<span data-ttu-id="573b5-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="573b5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="573b5-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="573b5-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="573b5-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="573b5-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="573b5-122">ドキュメント設定を指定する要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="573b5-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="573b5-123">子要素</span><span class="sxs-lookup"><span data-stu-id="573b5-123">Child elements</span></span>

<span data-ttu-id="573b5-124">なし。</span><span class="sxs-lookup"><span data-stu-id="573b5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="573b5-125">属性</span><span class="sxs-lookup"><span data-stu-id="573b5-125">Attributes</span></span>

<span data-ttu-id="573b5-126">なし。</span><span class="sxs-lookup"><span data-stu-id="573b5-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="573b5-127">注釈</span><span class="sxs-lookup"><span data-stu-id="573b5-127">Remarks</span></span>

<span data-ttu-id="573b5-128">値は、次の表の値の合計である場合があります。</span><span class="sxs-lookup"><span data-stu-id="573b5-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="573b5-129">**値**</span><span class="sxs-lookup"><span data-stu-id="573b5-129">**Value**</span></span>|<span data-ttu-id="573b5-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="573b5-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="573b5-131">0</span><span class="sxs-lookup"><span data-stu-id="573b5-131">0</span></span>  <br/> |<span data-ttu-id="573b5-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="573b5-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="573b5-133">1</span><span class="sxs-lookup"><span data-stu-id="573b5-133">1</span></span>  <br/> |<span data-ttu-id="573b5-134">スナップサブディビジョンに設定します。</span><span class="sxs-lookup"><span data-stu-id="573b5-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="573b5-135">2</span><span class="sxs-lookup"><span data-stu-id="573b5-135">2</span></span>  <br/> |<span data-ttu-id="573b5-136">スナップグリッドに移動します。</span><span class="sxs-lookup"><span data-stu-id="573b5-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="573b5-137">4</span><span class="sxs-lookup"><span data-stu-id="573b5-137">4</span></span>  <br/> |<span data-ttu-id="573b5-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="573b5-139">8</span><span class="sxs-lookup"><span data-stu-id="573b5-139">8</span></span>  <br/> |<span data-ttu-id="573b5-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="573b5-141">16 </span><span class="sxs-lookup"><span data-stu-id="573b5-141">16</span></span>  <br/> |<span data-ttu-id="573b5-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="573b5-143">32</span><span class="sxs-lookup"><span data-stu-id="573b5-143">32</span></span>  <br/> |<span data-ttu-id="573b5-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="573b5-145">256</span><span class="sxs-lookup"><span data-stu-id="573b5-145">256</span></span>  <br/> |<span data-ttu-id="573b5-146">スナップ図形の可視エッジに対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="573b5-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="573b5-147">512</span><span class="sxs-lookup"><span data-stu-id="573b5-147">512</span></span>  <br/> |<span data-ttu-id="573b5-148">スナップボックスに配置します。</span><span class="sxs-lookup"><span data-stu-id="573b5-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="573b5-149">1024</span><span class="sxs-lookup"><span data-stu-id="573b5-149">1024</span></span>  <br/> |<span data-ttu-id="573b5-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="573b5-151">32768</span><span class="sxs-lookup"><span data-stu-id="573b5-151">32768</span></span>  <br/> |<span data-ttu-id="573b5-152">スナップ無効です。</span><span class="sxs-lookup"><span data-stu-id="573b5-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="573b5-153">65536</span><span class="sxs-lookup"><span data-stu-id="573b5-153">65536</span></span>  <br/> |<span data-ttu-id="573b5-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="573b5-154">Snap to intersections.</span></span>  <br/> |
   

