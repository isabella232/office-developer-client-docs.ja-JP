---
title: '[LockThemeEffects] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70002
localization_priority: Normal
ms.assetid: 84179718-d7a6-d503-08f2-213571bf108f
ms.openlocfilehash: 41c9e9c021c5ad954c16599f9e376063655ffa07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805779"
---
# <a name="lockthemeeffects-cell-protection-section"></a><span data-ttu-id="37d87-102">[LockThemeEffects] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="37d87-102">LockThemeEffects Cell (Protection Section)</span></span>

<span data-ttu-id="37d87-103">図形にテーマの効果の適用を防止します。</span><span class="sxs-lookup"><span data-stu-id="37d87-103">Prevents application of theme effects to the shape.</span></span> 
  
<span data-ttu-id="37d87-104">**テーマの効果を**チェック ボックスの設定で、[**保護**] ダイアログ ボックスに対応します。</span><span class="sxs-lookup"><span data-stu-id="37d87-104">Corresponds to the **From theme effects** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="37d87-105">別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [LockThemeColors] セルを参照するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="37d87-105">To refer ti the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37d87-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="37d87-106">Cell name:</span></span>  <br/> |<span data-ttu-id="37d87-107">LockThemeEffects</span><span class="sxs-lookup"><span data-stu-id="37d87-107">LockThemeEffects</span></span>  <br/> |
   
<span data-ttu-id="37d87-108">プログラムから、インデックスによって [LockThemeEffects] セルを参照するには、 **CellsSRC** プロパティを使用し、次の引数を指定します。

</span><span class="sxs-lookup"><span data-stu-id="37d87-108">To refer to the LockThemeEffects cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37d87-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d87-109">Section index:</span></span>  <br/> |<span data-ttu-id="37d87-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37d87-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37d87-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d87-111">Row index:</span></span>  <br/> |<span data-ttu-id="37d87-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="37d87-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="37d87-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="37d87-113">Cell index:</span></span>  <br/> |<span data-ttu-id="37d87-114">**visLockThemeEffects**</span><span class="sxs-lookup"><span data-stu-id="37d87-114">**visLockThemeEffects**</span></span> <br/> |
   

