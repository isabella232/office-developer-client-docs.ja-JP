---
title: '[Type] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: 図形データ値のデータの種類を指定します。
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406249"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="bcc13-103">[Type] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="bcc13-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="bcc13-104">図形データ値のデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="bcc13-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bcc13-105">**Value**</span></span>|<span data-ttu-id="bcc13-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bcc13-106">**Description**</span></span>|<span data-ttu-id="bcc13-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="bcc13-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcc13-108">0</span><span class="sxs-lookup"><span data-stu-id="bcc13-108">0</span></span>  <br/> |<span data-ttu-id="bcc13-p101">文字列。これは既定値です。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="bcc13-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="bcc13-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="bcc13-112">1</span><span class="sxs-lookup"><span data-stu-id="bcc13-112">1</span></span>  <br/> |<span data-ttu-id="bcc13-p102">固定リスト。[**図形データの定義**] ダイアログ ボックスのドロップダウン コンボ ボックスにリスト項目を表示します。リスト項目は [Format] セルで指定します。このリストからは 1 つの項目だけを選択できます。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p102">Fixed list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select only one item from the list.  </span></span><br/> |<span data-ttu-id="bcc13-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="bcc13-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="bcc13-118">2</span><span class="sxs-lookup"><span data-stu-id="bcc13-118">2</span></span>  <br/> |<span data-ttu-id="bcc13-p103">数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="bcc13-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="bcc13-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="bcc13-123">3</span><span class="sxs-lookup"><span data-stu-id="bcc13-123">3</span></span>  <br/> |<span data-ttu-id="bcc13-p104">ブール演算型。[**図形データの定義**] ダイアログ ボックスのドロップダウン リスト ボックスから選択できる項目として、FALSE および TRUE を表示します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p104">Boolean. Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.  </span></span><br/> |<span data-ttu-id="bcc13-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="bcc13-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="bcc13-127">4</span><span class="sxs-lookup"><span data-stu-id="bcc13-127">4</span></span>  <br/> |<span data-ttu-id="bcc13-p105">変数リスト。[**図形データの定義**] ダイアログ ボックスのドロップダウン コンボ ボックスにリスト項目を表示します。リスト項目は [Format] セルで指定します。リスト項目を選択することも、新しい項目を入力して [Format] セルの現在のリストに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p105">Variable list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select a list item or enter a new item that is added to the current list in the Format cell.  </span></span><br/> |<span data-ttu-id="bcc13-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="bcc13-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="bcc13-133">5</span><span class="sxs-lookup"><span data-stu-id="bcc13-133">5</span></span>  <br/> |<span data-ttu-id="bcc13-p106">日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="bcc13-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="bcc13-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="bcc13-138">6</span><span class="sxs-lookup"><span data-stu-id="bcc13-138">6</span></span>  <br/> |<span data-ttu-id="bcc13-p107">期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="bcc13-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="bcc13-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="bcc13-143">7</span><span class="sxs-lookup"><span data-stu-id="bcc13-143">7</span></span>  <br/> |<span data-ttu-id="bcc13-p108">通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="bcc13-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="bcc13-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcc13-148">注釈</span><span class="sxs-lookup"><span data-stu-id="bcc13-148">Remarks</span></span>

<span data-ttu-id="bcc13-149">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcc13-150">セル名:</span><span class="sxs-lookup"><span data-stu-id="bcc13-150">Cell name:</span></span>  <br/> |<span data-ttu-id="bcc13-151">Prop. *Name*  .Prop を入力します。  *名前*  は行名です</span><span class="sxs-lookup"><span data-stu-id="bcc13-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bcc13-152">プログラムから、インデックスによって [Type] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcc13-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcc13-153">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcc13-153">Section index:</span></span>  <br/> |<span data-ttu-id="bcc13-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="bcc13-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="bcc13-155">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcc13-155">Row index:</span></span>  <br/> |<span data-ttu-id="bcc13-156">**visRowProp**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bcc13-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bcc13-157">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcc13-157">Cell index:</span></span>  <br/> |<span data-ttu-id="bcc13-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="bcc13-158">**visCustPropsType**</span></span> <br/> |
   

