---
title: '[Comment] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: 図形のコメント テキストを文字列形式で格納します。
ms.openlocfilehash: e6f21875928bce31dc2004d88f2d281e31265d65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357114"
---
# <a name="comment-cell-miscellaneous-section"></a><span data-ttu-id="d4041-103">[Comment] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4041-103">Comment Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="d4041-104">図形のコメント テキストを文字列形式で格納します。</span><span class="sxs-lookup"><span data-stu-id="d4041-104">Contains the comment text in string format for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4041-105">解説</span><span class="sxs-lookup"><span data-stu-id="d4041-105">Remarks</span></span>

<span data-ttu-id="d4041-106">コメントは、[**校閲**] タブの [**新しいコメント**] をクリックして挿入することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4041-106">You can also insert a comment by clicking **New Comment** on the **Review** tab.</span></span> 
  
<span data-ttu-id="d4041-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4041-107">To get a reference to the Comment cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4041-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="d4041-108">Cell name:</span></span>  <br/> |<span data-ttu-id="d4041-109">Comment</span><span class="sxs-lookup"><span data-stu-id="d4041-109">Comment</span></span>  <br/> |
   
<span data-ttu-id="d4041-110">プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4041-110">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4041-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4041-111">Section index:</span></span>  <br/> |<span data-ttu-id="d4041-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4041-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d4041-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4041-113">Row index:</span></span>  <br/> |<span data-ttu-id="d4041-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="d4041-114">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="d4041-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4041-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d4041-116">**visComment**</span><span class="sxs-lookup"><span data-stu-id="d4041-116">**visComment**</span></span> <br/> |
   

