---
title: '[Type] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: テキスト フィールドの値に対してデータの種類を指定します。
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806705"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="228b0-103">[Type] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="228b0-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="228b0-104">テキスト フィールドの値に対してデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="228b0-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="228b0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="228b0-105">**Value**</span></span>|<span data-ttu-id="228b0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="228b0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="228b0-107">0</span><span class="sxs-lookup"><span data-stu-id="228b0-107">0</span></span>  <br/> |<span data-ttu-id="228b0-108">文字列。</span><span class="sxs-lookup"><span data-stu-id="228b0-108">String.</span></span>  <br/> |
|<span data-ttu-id="228b0-109">2</span><span class="sxs-lookup"><span data-stu-id="228b0-109">2</span></span>  <br/> |<span data-ttu-id="228b0-p101">数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="228b0-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="228b0-113">5</span><span class="sxs-lookup"><span data-stu-id="228b0-113">5</span></span>  <br/> |<span data-ttu-id="228b0-p102">日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="228b0-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="228b0-117">6</span><span class="sxs-lookup"><span data-stu-id="228b0-117">6</span></span>  <br/> |<span data-ttu-id="228b0-p103">期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="228b0-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="228b0-121">7</span><span class="sxs-lookup"><span data-stu-id="228b0-121">7</span></span>  <br/> |<span data-ttu-id="228b0-p104">通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="228b0-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="228b0-125">注釈</span><span class="sxs-lookup"><span data-stu-id="228b0-125">Remarks</span></span>

<span data-ttu-id="228b0-126">**フィールド**] ダイアログ ボックスを使用してこのセルの値を設定することもできます (図形を選択して、[**挿入**] タブの [**テキスト**] で、[**フィールド**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="228b0-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="228b0-127">取得する、[Type] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="228b0-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="228b0-128">セル名:</span><span class="sxs-lookup"><span data-stu-id="228b0-128">Cell name:</span></span>  <br/> |<span data-ttu-id="228b0-129">Fields.Type [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="228b0-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="228b0-130">プログラムから、インデックスによって [Type] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="228b0-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="228b0-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="228b0-131">Section index:</span></span>  <br/> |<span data-ttu-id="228b0-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="228b0-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="228b0-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="228b0-133">Row index:</span></span>  <br/> |<span data-ttu-id="228b0-134">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="228b0-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="228b0-135">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="228b0-135">Cell index:</span></span>  <br/> |<span data-ttu-id="228b0-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="228b0-136">**visFieldType**</span></span> <br/> |
   

