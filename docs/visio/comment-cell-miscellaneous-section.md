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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419066"
---
# <a name="comment-cell-miscellaneous-section"></a><span data-ttu-id="5fc6f-103">[Comment] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="5fc6f-103">Comment Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5fc6f-104">図形のコメント テキストを文字列形式で格納します。</span><span class="sxs-lookup"><span data-stu-id="5fc6f-104">Contains the comment text in string format for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fc6f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="5fc6f-105">Remarks</span></span>

<span data-ttu-id="5fc6f-106">コメントは、[**校閲**] タブの [**新しいコメント**] をクリックして挿入することもできます。</span><span class="sxs-lookup"><span data-stu-id="5fc6f-106">You can also insert a comment by clicking **New Comment** on the **Review** tab.</span></span> 
  
<span data-ttu-id="5fc6f-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fc6f-107">To get a reference to the Comment cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fc6f-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="5fc6f-108">Cell name:</span></span>  <br/> |<span data-ttu-id="5fc6f-109">Comment</span><span class="sxs-lookup"><span data-stu-id="5fc6f-109">Comment</span></span>  <br/> |
   
<span data-ttu-id="5fc6f-110">プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fc6f-110">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fc6f-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5fc6f-111">Section index:</span></span>  <br/> |<span data-ttu-id="5fc6f-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5fc6f-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5fc6f-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5fc6f-113">Row index:</span></span>  <br/> |<span data-ttu-id="5fc6f-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5fc6f-114">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="5fc6f-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5fc6f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5fc6f-116">**visComment**</span><span class="sxs-lookup"><span data-stu-id="5fc6f-116">**visComment**</span></span> <br/> |
   

