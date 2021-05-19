---
title: '[LockFromGroupFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426059"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="6820b-102">[LockFromGroupFormat] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="6820b-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="6820b-103">グループ図形に対する変更がサブ図形に伝達されるのをブロックし、ユーザーは選択したサブ図形を直接書式設定できます。</span><span class="sxs-lookup"><span data-stu-id="6820b-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="6820b-104">[LockFromGroupFormat] セルの値は、[**保護**] ダイアログ ボックスにある [**グループ書式設定を適用不可にする**] チェック ボックスの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="6820b-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="6820b-105">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFromGroupFormat] セルへの参照を取得するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="6820b-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6820b-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="6820b-106">Cell name:</span></span>  <br/> |<span data-ttu-id="6820b-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="6820b-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="6820b-108">プログラムから、インデックスによって [LockFromGroupFormat] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6820b-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6820b-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6820b-109">Section index:</span></span>  <br/> |<span data-ttu-id="6820b-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6820b-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6820b-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6820b-111">Row index:</span></span>  <br/> |<span data-ttu-id="6820b-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6820b-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="6820b-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6820b-113">Cell index:</span></span>  <br/> |<span data-ttu-id="6820b-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="6820b-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="6820b-115">セルの既定値は 0 (False) となります。</span><span class="sxs-lookup"><span data-stu-id="6820b-115">The default value for the cell is 0 (False).</span></span>
  

