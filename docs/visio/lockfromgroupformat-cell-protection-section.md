---
title: '[LockFromGroupFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805768"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="3c1c1-102">[LockFromGroupFormat] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="3c1c1-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="3c1c1-103">フォーマットを変更してグループ図形を直接選択したサブ図形の書式を設定するユーザーを許可する一方、サブ図形に反映されません。</span><span class="sxs-lookup"><span data-stu-id="3c1c1-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="3c1c1-104">[LockFromGroupFormat] セルの値は、[**保護**] ダイアログ ボックスにある [**グループ書式設定を適用不可にする**] チェック ボックスの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="3c1c1-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="3c1c1-105">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFromGroupFormat] セルへの参照を取得するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="3c1c1-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c1c1-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="3c1c1-106">Cell name:</span></span>  <br/> |<span data-ttu-id="3c1c1-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="3c1c1-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="3c1c1-108">プログラムから、インデックスによって [LockFromGroupFormat] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。

</span><span class="sxs-lookup"><span data-stu-id="3c1c1-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c1c1-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c1c1-109">Section index:</span></span>  <br/> |<span data-ttu-id="3c1c1-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3c1c1-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3c1c1-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c1c1-111">Row index:</span></span>  <br/> |<span data-ttu-id="3c1c1-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3c1c1-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="3c1c1-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3c1c1-113">Cell index:</span></span>  <br/> |<span data-ttu-id="3c1c1-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="3c1c1-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="3c1c1-115">セルの既定値は 0 (False) となります。</span><span class="sxs-lookup"><span data-stu-id="3c1c1-115">The default value for the cell is 0 (False).</span></span>
  

