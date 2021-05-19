---
title: '[LinePattern] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: 図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。
ms.openlocfilehash: eec5bed18777f7822f9544d59dce7722f2f732bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416756"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="c8afc-104">[LinePattern] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="c8afc-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="c8afc-p102">図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="c8afc-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="c8afc-107">**値**</span><span class="sxs-lookup"><span data-stu-id="c8afc-107">**Value**</span></span>|<span data-ttu-id="c8afc-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="c8afc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c8afc-109">0</span><span class="sxs-lookup"><span data-stu-id="c8afc-109">0</span></span>  <br/> |<span data-ttu-id="c8afc-110">線の種類なし</span><span class="sxs-lookup"><span data-stu-id="c8afc-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="c8afc-111">1</span><span class="sxs-lookup"><span data-stu-id="c8afc-111">1</span></span>  <br/> |<span data-ttu-id="c8afc-112">実線</span><span class="sxs-lookup"><span data-stu-id="c8afc-112">Solid</span></span>  <br/> |
|<span data-ttu-id="c8afc-113">2 ～ 23</span><span class="sxs-lookup"><span data-stu-id="c8afc-113">2 - 23</span></span>  <br/> |<span data-ttu-id="c8afc-114">さまざまな線の種類</span><span class="sxs-lookup"><span data-stu-id="c8afc-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8afc-115">注釈</span><span class="sxs-lookup"><span data-stu-id="c8afc-115">Remarks</span></span>

<span data-ttu-id="c8afc-116">線の種類のコレクションは、[**線**] ダイアログ ボックスで参照できます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**実線/点線**] をポイントして、[**その他の線**] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="c8afc-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="c8afc-117">ユーザー設定の線のパターンを指定するには、このセルで USE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8afc-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="c8afc-118">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LinePattern] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8afc-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8afc-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="c8afc-119">Cell name:</span></span>  <br/> |<span data-ttu-id="c8afc-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="c8afc-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="c8afc-121">プログラムから、インデックスによって [LinePattern] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8afc-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8afc-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8afc-122">Section index:</span></span>  <br/> |<span data-ttu-id="c8afc-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8afc-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c8afc-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8afc-124">Row index:</span></span>  <br/> |<span data-ttu-id="c8afc-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c8afc-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="c8afc-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8afc-126">Cell index:</span></span>  <br/> |<span data-ttu-id="c8afc-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="c8afc-127">**visLinePattern**</span></span> <br/> |
   

