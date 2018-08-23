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
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805775"
---
# <a name="lockthemecolors-cell-protection-section"></a><span data-ttu-id="fb384-102">[LockThemeColors] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="fb384-102">LockThemeColors Cell (Protection Section)</span></span>

<span data-ttu-id="fb384-103">図形には、テーマの色のアプリケーションを防止します。</span><span class="sxs-lookup"><span data-stu-id="fb384-103">Prevents application of theme colors to the shape.</span></span> 
  
<span data-ttu-id="fb384-104">[LockThemeColors] セルの値は、[**保護**] ダイアログ ボックスの [**テーマの色を適用不可にする**] チェックボックスの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="fb384-104">The value of the LockThemeColors cell corresponds to the **From theme colors** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="fb384-105">別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [LockThemeColors] セルを参照するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="fb384-105">To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb384-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="fb384-106">Cell name:</span></span>  <br/> |<span data-ttu-id="fb384-107">LockThemeColors</span><span class="sxs-lookup"><span data-stu-id="fb384-107">LockThemeColors</span></span>  <br/> |
   
<span data-ttu-id="fb384-108">プログラムから、インデックスによって [LockThemeColors] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。

</span><span class="sxs-lookup"><span data-stu-id="fb384-108">To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb384-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb384-109">Section index:</span></span>  <br/> |<span data-ttu-id="fb384-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb384-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fb384-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb384-111">Row index:</span></span>  <br/> |<span data-ttu-id="fb384-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fb384-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="fb384-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="fb384-113">Cell index:</span></span>  <br/> |<span data-ttu-id="fb384-114">**visLockThemeColors**</span><span class="sxs-lookup"><span data-stu-id="fb384-114">**visLockThemeColors**</span></span> <br/> |
   

