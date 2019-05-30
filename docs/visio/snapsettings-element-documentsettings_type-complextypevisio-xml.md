---
title: SnapSettings 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540295"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="7699d-103">SnapSettings 要素 (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7699d-103">SnapSettings element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7699d-104">ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="7699d-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7699d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="7699d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7699d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="7699d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7699d-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7699d-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7699d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7699d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7699d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="7699d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7699d-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="7699d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7699d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="7699d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7699d-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="7699d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7699d-113">定義</span><span class="sxs-lookup"><span data-stu-id="7699d-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7699d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="7699d-114">Elements and attributes</span></span>

<span data-ttu-id="7699d-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7699d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7699d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="7699d-116">Parent elements</span></span>

|<span data-ttu-id="7699d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="7699d-117">**Element**</span></span>|<span data-ttu-id="7699d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="7699d-118">**Type**</span></span>|<span data-ttu-id="7699d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="7699d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7699d-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="7699d-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7699d-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7699d-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7699d-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="7699d-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7699d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="7699d-123">Child elements</span></span>

<span data-ttu-id="7699d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="7699d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7699d-125">属性</span><span class="sxs-lookup"><span data-stu-id="7699d-125">Attributes</span></span>

<span data-ttu-id="7699d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="7699d-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7699d-127">注釈</span><span class="sxs-lookup"><span data-stu-id="7699d-127">Remarks</span></span>

<span data-ttu-id="7699d-128">値には、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7699d-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="7699d-129">**値**</span><span class="sxs-lookup"><span data-stu-id="7699d-129">**Value**</span></span>|<span data-ttu-id="7699d-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="7699d-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7699d-131">.0</span><span class="sxs-lookup"><span data-stu-id="7699d-131">0</span></span>  <br/> |<span data-ttu-id="7699d-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="7699d-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="7699d-133">1-d</span><span class="sxs-lookup"><span data-stu-id="7699d-133">1</span></span>  <br/> |<span data-ttu-id="7699d-134">ルーラーの目盛りにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="7699d-135">pbm-2</span><span class="sxs-lookup"><span data-stu-id="7699d-135">2</span></span>  <br/> |<span data-ttu-id="7699d-136">グリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="7699d-137">2/4</span><span class="sxs-lookup"><span data-stu-id="7699d-137">4</span></span>  <br/> |<span data-ttu-id="7699d-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="7699d-139">8 </span><span class="sxs-lookup"><span data-stu-id="7699d-139">8</span></span>  <br/> |<span data-ttu-id="7699d-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="7699d-141">16</span><span class="sxs-lookup"><span data-stu-id="7699d-141">16</span></span>  <br/> |<span data-ttu-id="7699d-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="7699d-143">32</span><span class="sxs-lookup"><span data-stu-id="7699d-143">32</span></span>  <br/> |<span data-ttu-id="7699d-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="7699d-145">256</span><span class="sxs-lookup"><span data-stu-id="7699d-145">256</span></span>  <br/> |<span data-ttu-id="7699d-146">表示されている図形の端にスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="7699d-147">512</span><span class="sxs-lookup"><span data-stu-id="7699d-147">512</span></span>  <br/> |<span data-ttu-id="7699d-148">整列ボックスにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="7699d-149">1024</span><span class="sxs-lookup"><span data-stu-id="7699d-149">1024</span></span>  <br/> |<span data-ttu-id="7699d-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="7699d-151">32768</span><span class="sxs-lookup"><span data-stu-id="7699d-151">32768</span></span>  <br/> |<span data-ttu-id="7699d-152">スナップは無効です。</span><span class="sxs-lookup"><span data-stu-id="7699d-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="7699d-153">65536</span><span class="sxs-lookup"><span data-stu-id="7699d-153">65536</span></span>  <br/> |<span data-ttu-id="7699d-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="7699d-154">Snap to intersections.</span></span>  <br/> |
   

