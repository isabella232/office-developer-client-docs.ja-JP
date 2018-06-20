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
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806704"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="0b06f-103">[Type] セル ([Shape Data] セクション)</span><span class="sxs-lookup"><span data-stu-id="0b06f-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="0b06f-104">図形データ値のデータの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="0b06f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0b06f-105">**Value**</span></span>|<span data-ttu-id="0b06f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0b06f-106">**Description**</span></span>|<span data-ttu-id="0b06f-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0b06f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b06f-108">0</span><span class="sxs-lookup"><span data-stu-id="0b06f-108">0</span></span>  <br/> |<span data-ttu-id="0b06f-p101">文字列。これは既定値です。</span><span class="sxs-lookup"><span data-stu-id="0b06f-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="0b06f-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="0b06f-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="0b06f-112">1</span><span class="sxs-lookup"><span data-stu-id="0b06f-112">1</span></span>  <br/> |<span data-ttu-id="0b06f-113">固定リスト。</span><span class="sxs-lookup"><span data-stu-id="0b06f-113">Fixed list.</span></span> <span data-ttu-id="0b06f-114">**図形データの定義**] ダイアログ ボックスの一覧の項目のドロップダウン コンボ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-114">Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="0b06f-115">Format] セルに、リスト項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-115">Specify the list items in the Format cell.</span></span> <span data-ttu-id="0b06f-116">ユーザーは、一覧から 1 項目だけを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0b06f-116">Users can select only one item from the list.</span></span>  <br/> |<span data-ttu-id="0b06f-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="0b06f-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="0b06f-118">2</span><span class="sxs-lookup"><span data-stu-id="0b06f-118">2</span></span>  <br/> |<span data-ttu-id="0b06f-p103">数値。日付、時刻、期間、通貨の値の他、スカラー、寸法、角度も含まれます。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="0b06f-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="0b06f-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="0b06f-123">3</span><span class="sxs-lookup"><span data-stu-id="0b06f-123">3</span></span>  <br/> |<span data-ttu-id="0b06f-124">ブール値です。</span><span class="sxs-lookup"><span data-stu-id="0b06f-124">Boolean.</span></span> <span data-ttu-id="0b06f-125">FALSE および true を指定するように、[**図形データの定義**] ダイアログ ボックス内のドロップ ダウン リスト ボックスから選択できる項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-125">Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.</span></span>  <br/> |<span data-ttu-id="0b06f-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="0b06f-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="0b06f-127">4</span><span class="sxs-lookup"><span data-stu-id="0b06f-127">4</span></span>  <br/> |<span data-ttu-id="0b06f-128">変数の一覧です。</span><span class="sxs-lookup"><span data-stu-id="0b06f-128">Variable list.</span></span> <span data-ttu-id="0b06f-129">**図形データの定義**] ダイアログ ボックスの一覧の項目のドロップダウン コンボ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-129">Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="0b06f-130">Format] セルに、リスト項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-130">Specify the list items in the Format cell.</span></span> <span data-ttu-id="0b06f-131">ユーザーでは、リスト項目を選択したり、セルの書式での現在のリストに追加される新しい項目を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="0b06f-131">Users can select a list item or enter a new item that is added to the current list in the Format cell.</span></span>  <br/> |<span data-ttu-id="0b06f-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="0b06f-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="0b06f-133">5</span><span class="sxs-lookup"><span data-stu-id="0b06f-133">5</span></span>  <br/> |<span data-ttu-id="0b06f-p106">日付または時刻の値。日、月、年、および秒、分、時間、または日付と時刻の組み合わせを表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="0b06f-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="0b06f-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="0b06f-138">6</span><span class="sxs-lookup"><span data-stu-id="0b06f-138">6</span></span>  <br/> |<span data-ttu-id="0b06f-p107">期間の値。経過時間を表示します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="0b06f-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="0b06f-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="0b06f-143">7</span><span class="sxs-lookup"><span data-stu-id="0b06f-143">7</span></span>  <br/> |<span data-ttu-id="0b06f-p108">通貨の値。システムに適用されている現在の地域別設定を使用します。書式形式は [Format] セルで指定します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="0b06f-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="0b06f-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b06f-148">備考</span><span class="sxs-lookup"><span data-stu-id="0b06f-148">Remarks</span></span>

<span data-ttu-id="0b06f-149">取得する、[Type] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b06f-150">セル名:</span><span class="sxs-lookup"><span data-stu-id="0b06f-150">Cell name:</span></span>  <br/> |<span data-ttu-id="0b06f-151">プロペラです。*名*です。型、プロペラします。 *名前*は、行の名前</span><span class="sxs-lookup"><span data-stu-id="0b06f-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="0b06f-152">プログラムから、インデックスによって [Type] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b06f-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b06f-153">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b06f-153">Section index:</span></span>  <br/> |<span data-ttu-id="0b06f-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="0b06f-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="0b06f-155">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b06f-155">Row index:</span></span>  <br/> |<span data-ttu-id="0b06f-156">**visRowProp** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="0b06f-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0b06f-157">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0b06f-157">Cell index:</span></span>  <br/> |<span data-ttu-id="0b06f-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="0b06f-158">**visCustPropsType**</span></span> <br/> |
   

