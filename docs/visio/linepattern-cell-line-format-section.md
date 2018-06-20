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
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805708"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="bef68-104">[LinePattern] セル ([Line Format] セクション)</span><span class="sxs-lookup"><span data-stu-id="bef68-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="bef68-p102">図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="bef68-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="bef68-107">**値**</span><span class="sxs-lookup"><span data-stu-id="bef68-107">**Value**</span></span>|<span data-ttu-id="bef68-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="bef68-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bef68-109">0</span><span class="sxs-lookup"><span data-stu-id="bef68-109">0</span></span>  <br/> |<span data-ttu-id="bef68-110">線の種類なし</span><span class="sxs-lookup"><span data-stu-id="bef68-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="bef68-111">1</span><span class="sxs-lookup"><span data-stu-id="bef68-111">1</span></span>  <br/> |<span data-ttu-id="bef68-112">実線</span><span class="sxs-lookup"><span data-stu-id="bef68-112">Solid</span></span>  <br/> |
|<span data-ttu-id="bef68-113">2-23</span><span class="sxs-lookup"><span data-stu-id="bef68-113">2 - 23</span></span>  <br/> |<span data-ttu-id="bef68-114">さまざまな線の種類</span><span class="sxs-lookup"><span data-stu-id="bef68-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bef68-115">注釈</span><span class="sxs-lookup"><span data-stu-id="bef68-115">Remarks</span></span>

<span data-ttu-id="bef68-116">線のパターンのコレクションを表示するには [**線**] ダイアログ ボックス ([**ホーム**] タブの [**図形**] グループで、**行**、**ダッシュ**をし、**他の線**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="bef68-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="bef68-117">ユーザー設定の線のパターンを指定するには、このセルで USE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="bef68-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="bef68-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LinePattern] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="bef68-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bef68-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="bef68-119">Cell name:</span></span>  <br/> |<span data-ttu-id="bef68-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="bef68-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="bef68-121">プログラムから、インデックスによって [LinePattern] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bef68-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bef68-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bef68-122">Section index:</span></span>  <br/> |<span data-ttu-id="bef68-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bef68-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bef68-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bef68-124">Row index:</span></span>  <br/> |<span data-ttu-id="bef68-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="bef68-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="bef68-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bef68-126">Cell index:</span></span>  <br/> |<span data-ttu-id="bef68-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="bef68-127">**visLinePattern**</span></span> <br/> |
   

