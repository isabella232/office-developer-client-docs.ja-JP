---
title: snapsettings 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334490"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="31006-103">snapsettings 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="31006-103">SnapSettings element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="31006-104">ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="31006-104">Specifies the objects that shapes snap to when snap is active in the window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31006-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="31006-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31006-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="31006-106">**Element type**</span></span> <br/> |[<span data-ttu-id="31006-107">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="31006-107">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="31006-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="31006-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="31006-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="31006-109">**Schema file**</span></span> <br/> |<span data-ttu-id="31006-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="31006-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="31006-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="31006-111">**Document parts**</span></span> <br/> |<span data-ttu-id="31006-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="31006-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31006-113">定義</span><span class="sxs-lookup"><span data-stu-id="31006-113">Definition</span></span>

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="31006-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="31006-114">Elements and attributes</span></span>

<span data-ttu-id="31006-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="31006-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="31006-116">親要素</span><span class="sxs-lookup"><span data-stu-id="31006-116">Parent elements</span></span>

|<span data-ttu-id="31006-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="31006-117">**Element**</span></span>|<span data-ttu-id="31006-118">**型**</span><span class="sxs-lookup"><span data-stu-id="31006-118">**Type**</span></span>|<span data-ttu-id="31006-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="31006-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31006-120">documentsettings</span><span class="sxs-lookup"><span data-stu-id="31006-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31006-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="31006-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="31006-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="31006-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="31006-123">子要素</span><span class="sxs-lookup"><span data-stu-id="31006-123">Child elements</span></span>

<span data-ttu-id="31006-124">なし。</span><span class="sxs-lookup"><span data-stu-id="31006-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31006-125">属性</span><span class="sxs-lookup"><span data-stu-id="31006-125">Attributes</span></span>

<span data-ttu-id="31006-126">なし。</span><span class="sxs-lookup"><span data-stu-id="31006-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31006-127">解説</span><span class="sxs-lookup"><span data-stu-id="31006-127">Remarks</span></span>

<span data-ttu-id="31006-128">値には、次の表の値の合計を指定できます。</span><span class="sxs-lookup"><span data-stu-id="31006-128">The value may be a sum of the values in the following table.</span></span>
  
|<span data-ttu-id="31006-129">**値**</span><span class="sxs-lookup"><span data-stu-id="31006-129">**Value**</span></span>|<span data-ttu-id="31006-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="31006-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31006-131">.0</span><span class="sxs-lookup"><span data-stu-id="31006-131">0</span></span>  <br/> |<span data-ttu-id="31006-132">何もスナップしません。</span><span class="sxs-lookup"><span data-stu-id="31006-132">Snap to nothing.</span></span>  <br/> |
|<span data-ttu-id="31006-133">1-d</span><span class="sxs-lookup"><span data-stu-id="31006-133">1</span></span>  <br/> |<span data-ttu-id="31006-134">ルーラーの目盛りにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-134">Snap to ruler subdivisions.</span></span>  <br/> |
|<span data-ttu-id="31006-135">pbm-2</span><span class="sxs-lookup"><span data-stu-id="31006-135">2</span></span>  <br/> |<span data-ttu-id="31006-136">グリッドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-136">Snap to grid.</span></span>  <br/> |
|<span data-ttu-id="31006-137">2/4</span><span class="sxs-lookup"><span data-stu-id="31006-137">4</span></span>  <br/> |<span data-ttu-id="31006-138">ガイドにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-138">Snap to guides.</span></span>  <br/> |
|<span data-ttu-id="31006-139">~</span><span class="sxs-lookup"><span data-stu-id="31006-139">8</span></span>  <br/> |<span data-ttu-id="31006-140">選択ハンドルにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-140">Snap to selection handles.</span></span>  <br/> |
|<span data-ttu-id="31006-141">16</span><span class="sxs-lookup"><span data-stu-id="31006-141">16</span></span>  <br/> |<span data-ttu-id="31006-142">頂点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-142">Snap to vertices.</span></span>  <br/> |
|<span data-ttu-id="31006-143">32</span><span class="sxs-lookup"><span data-stu-id="31006-143">32</span></span>  <br/> |<span data-ttu-id="31006-144">接続ポイントにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-144">Snap to connection points.</span></span>  <br/> |
|<span data-ttu-id="31006-145">256</span><span class="sxs-lookup"><span data-stu-id="31006-145">256</span></span>  <br/> |<span data-ttu-id="31006-146">表示されている図形の端にスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-146">Snap to visible edges of shapes.</span></span>  <br/> |
|<span data-ttu-id="31006-147">512</span><span class="sxs-lookup"><span data-stu-id="31006-147">512</span></span>  <br/> |<span data-ttu-id="31006-148">整列ボックスにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-148">Snap to alignment box.</span></span>  <br/> |
|<span data-ttu-id="31006-149">1024</span><span class="sxs-lookup"><span data-stu-id="31006-149">1024</span></span>  <br/> |<span data-ttu-id="31006-150">図形の補助線オプションにスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-150">Snap to shape extensions options.</span></span>  <br/> |
|<span data-ttu-id="31006-151">32768</span><span class="sxs-lookup"><span data-stu-id="31006-151">32768</span></span>  <br/> |<span data-ttu-id="31006-152">スナップは無効です。</span><span class="sxs-lookup"><span data-stu-id="31006-152">Snap disabled.</span></span>  <br/> |
|<span data-ttu-id="31006-153">65536</span><span class="sxs-lookup"><span data-stu-id="31006-153">65536</span></span>  <br/> |<span data-ttu-id="31006-154">交点にスナップします。</span><span class="sxs-lookup"><span data-stu-id="31006-154">Snap to intersections.</span></span>  <br/> |
   

