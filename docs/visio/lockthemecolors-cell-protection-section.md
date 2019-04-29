---
title: '[LockThemeColors] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 81091ea33be2158435d240ba14f3c97e8f3fcc39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436847"
---
# <a name="lockthemecolors-cell-protection-section"></a><span data-ttu-id="96cd4-102">[LockThemeColors] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="96cd4-102">LockThemeColors Cell (Protection Section)</span></span>

<span data-ttu-id="96cd4-103">テーマの色が図形に適用されないようにします。</span><span class="sxs-lookup"><span data-stu-id="96cd4-103">Prevents application of theme colors to the shape.</span></span> 
  
<span data-ttu-id="96cd4-104">[LockThemeColors] セルの値は、[**保護**] ダイアログ ボックスの [**テーマの色を適用不可にする**] チェックボックスの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="96cd4-104">The value of the LockThemeColors cell corresponds to the **From theme colors** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="96cd4-105">別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [LockThemeColors] セルを参照するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="96cd4-105">To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96cd4-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="96cd4-106">Cell name:</span></span>  <br/> |<span data-ttu-id="96cd4-107">[lockthemecolors]</span><span class="sxs-lookup"><span data-stu-id="96cd4-107">LockThemeColors</span></span>  <br/> |
   
<span data-ttu-id="96cd4-108">プログラムから、インデックスによって [LockThemeColors] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="96cd4-108">To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96cd4-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="96cd4-109">Section index:</span></span>  <br/> |<span data-ttu-id="96cd4-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="96cd4-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="96cd4-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="96cd4-111">Row index:</span></span>  <br/> |<span data-ttu-id="96cd4-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="96cd4-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="96cd4-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="96cd4-113">Cell index:</span></span>  <br/> |<span data-ttu-id="96cd4-114">**visLockThemeColors**</span><span class="sxs-lookup"><span data-stu-id="96cd4-114">**visLockThemeColors**</span></span> <br/> |
   

