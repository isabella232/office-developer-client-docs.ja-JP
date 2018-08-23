---
title: SnapSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: 図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
ms.openlocfilehash: 0e784ddf9d5e04dae20a6a811557455c476b11a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806525"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="84e0d-103">SnapSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="84e0d-103">SnapSettings element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="84e0d-104">図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="84e0d-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84e0d-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="84e0d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84e0d-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="84e0d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="84e0d-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="84e0d-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="84e0d-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="84e0d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="84e0d-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="84e0d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="84e0d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="84e0d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="84e0d-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="84e0d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="84e0d-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="84e0d-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="84e0d-113">定義</span><span class="sxs-lookup"><span data-stu-id="84e0d-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="84e0d-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="84e0d-114">Elements and attributes</span></span>

<span data-ttu-id="84e0d-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="84e0d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="84e0d-116">親要素</span><span class="sxs-lookup"><span data-stu-id="84e0d-116">Parent elements</span></span>

|<span data-ttu-id="84e0d-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="84e0d-117">**Element**</span></span>|<span data-ttu-id="84e0d-118">**型**</span><span class="sxs-lookup"><span data-stu-id="84e0d-118">**Type**</span></span>|<span data-ttu-id="84e0d-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="84e0d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="84e0d-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="84e0d-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="84e0d-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="84e0d-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="84e0d-122">ドキュメントの設定を指定する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84e0d-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="84e0d-123">子要素</span><span class="sxs-lookup"><span data-stu-id="84e0d-123">Child elements</span></span>

<span data-ttu-id="84e0d-124">なし。</span><span class="sxs-lookup"><span data-stu-id="84e0d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84e0d-125">属性</span><span class="sxs-lookup"><span data-stu-id="84e0d-125">Attributes</span></span>

<span data-ttu-id="84e0d-126">なし。</span><span class="sxs-lookup"><span data-stu-id="84e0d-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84e0d-127">注釈</span><span class="sxs-lookup"><span data-stu-id="84e0d-127">Remarks</span></span>

<span data-ttu-id="84e0d-128">次の表の値の合計値があります。</span><span class="sxs-lookup"><span data-stu-id="84e0d-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="84e0d-129">**値**</span><span class="sxs-lookup"><span data-stu-id="84e0d-129">**Value**</span></span>|<span data-ttu-id="84e0d-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="84e0d-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84e0d-131">0</span><span class="sxs-lookup"><span data-stu-id="84e0d-131">0</span></span>  <br/> |<span data-ttu-id="84e0d-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="84e0d-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="84e0d-133">1</span><span class="sxs-lookup"><span data-stu-id="84e0d-133">1</span></span>  <br/> |<span data-ttu-id="84e0d-134">ルーラーの目盛りにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="84e0d-135">2</span><span class="sxs-lookup"><span data-stu-id="84e0d-135">2</span></span>  <br/> |<span data-ttu-id="84e0d-136">グリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="84e0d-137">4</span><span class="sxs-lookup"><span data-stu-id="84e0d-137">4</span></span>  <br/> |<span data-ttu-id="84e0d-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="84e0d-139">8</span><span class="sxs-lookup"><span data-stu-id="84e0d-139">8</span></span>  <br/> |<span data-ttu-id="84e0d-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="84e0d-141">16</span><span class="sxs-lookup"><span data-stu-id="84e0d-141">16</span></span>  <br/> |<span data-ttu-id="84e0d-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="84e0d-143">32</span><span class="sxs-lookup"><span data-stu-id="84e0d-143">32</span></span>  <br/> |<span data-ttu-id="84e0d-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="84e0d-145">256</span><span class="sxs-lookup"><span data-stu-id="84e0d-145">256</span></span>  <br/> |<span data-ttu-id="84e0d-146">図形の可視のエッジにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="84e0d-147">512</span><span class="sxs-lookup"><span data-stu-id="84e0d-147">512</span></span>  <br/> |<span data-ttu-id="84e0d-148">図形枠にスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="84e0d-149">1024</span><span class="sxs-lookup"><span data-stu-id="84e0d-149">1024</span></span>  <br/> |<span data-ttu-id="84e0d-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="84e0d-151">32768</span><span class="sxs-lookup"><span data-stu-id="84e0d-151">32768</span></span>  <br/> |<span data-ttu-id="84e0d-152">スナップが無効になります。</span><span class="sxs-lookup"><span data-stu-id="84e0d-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="84e0d-153">65536</span><span class="sxs-lookup"><span data-stu-id="84e0d-153">65536</span></span>  <br/> |<span data-ttu-id="84e0d-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="84e0d-154">Snap to intersections.</span></span>  <br/> |
   

