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
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407985"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="6ca84-103">[Type] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="6ca84-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="6ca84-104">テキスト フィールドの値に対してデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="6ca84-105">**値**</span><span class="sxs-lookup"><span data-stu-id="6ca84-105">**Value**</span></span>|<span data-ttu-id="6ca84-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ca84-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ca84-107">0</span><span class="sxs-lookup"><span data-stu-id="6ca84-107">0</span></span>  <br/> |<span data-ttu-id="6ca84-108">文字列。</span><span class="sxs-lookup"><span data-stu-id="6ca84-108">String.</span></span>  <br/> |
|<span data-ttu-id="6ca84-109">2</span><span class="sxs-lookup"><span data-stu-id="6ca84-109">2</span></span>  <br/> |<span data-ttu-id="6ca84-p101">数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="6ca84-113">5</span><span class="sxs-lookup"><span data-stu-id="6ca84-113">5</span></span>  <br/> |<span data-ttu-id="6ca84-p102">日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="6ca84-117">6</span><span class="sxs-lookup"><span data-stu-id="6ca84-117">6</span></span>  <br/> |<span data-ttu-id="6ca84-p103">期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="6ca84-121">7</span><span class="sxs-lookup"><span data-stu-id="6ca84-121">7</span></span>  <br/> |<span data-ttu-id="6ca84-p104">通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ca84-125">注釈</span><span class="sxs-lookup"><span data-stu-id="6ca84-125">Remarks</span></span>

<span data-ttu-id="6ca84-126">[フィールド] ダイアログ ボックスを使用して、このセルの値を設定することもできます (図形が選択されている場合は、[挿入] タブの [テキスト] グループで、[フィールド] をクリック **します**)。 </span><span class="sxs-lookup"><span data-stu-id="6ca84-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="6ca84-127">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ca84-128">セル名:</span><span class="sxs-lookup"><span data-stu-id="6ca84-128">Cell name:</span></span>  <br/> |<span data-ttu-id="6ca84-129">Fields.Type[ *i*  ] where i =  *<*  1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="6ca84-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6ca84-130">プログラムから、インデックスによって [Type] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ca84-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ca84-131">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ca84-131">Section index:</span></span>  <br/> |<span data-ttu-id="6ca84-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="6ca84-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="6ca84-133">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ca84-133">Row index:</span></span>  <br/> |<span data-ttu-id="6ca84-134">**visRowField**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6ca84-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6ca84-135">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6ca84-135">Cell index:</span></span>  <br/> |<span data-ttu-id="6ca84-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="6ca84-136">**visFieldType**</span></span> <br/> |
   

