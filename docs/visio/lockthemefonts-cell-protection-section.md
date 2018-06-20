---
title: '[LockThemeFonts] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: FontIndex、テーマのプロパティの行のセルが新しいテーマを適用することによって変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805799"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="8ddae-104">[LockThemeFonts] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="8ddae-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="8ddae-105">**FontIndex** **テーマのプロパティ**の行のセルが新しいテーマを適用することによって変更するを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="8ddae-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="8ddae-106">でも、ユーザーからシェイプ シート内でこの値を手動で編集します。</span><span class="sxs-lookup"><span data-stu-id="8ddae-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="8ddae-107">**値**</span><span class="sxs-lookup"><span data-stu-id="8ddae-107">**Value**</span></span>|<span data-ttu-id="8ddae-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="8ddae-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ddae-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8ddae-109">TRUE</span></span>  <br/> |<span data-ttu-id="8ddae-110">シェイプ シートで直接変更しない限り、現在の値から**FontIndex**のセルを変更できません。</span><span class="sxs-lookup"><span data-stu-id="8ddae-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="8ddae-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8ddae-111">FALSE</span></span>  <br/> |<span data-ttu-id="8ddae-112">テーマが変更されると、現在の値から**FontIndex**のセルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="8ddae-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ddae-113">備考</span><span class="sxs-lookup"><span data-stu-id="8ddae-113">Remarks</span></span>

<span data-ttu-id="8ddae-114">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeFonts** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8ddae-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ddae-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="8ddae-115">Cell name:</span></span>  <br/> | <span data-ttu-id="8ddae-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="8ddae-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="8ddae-117">プログラムから、インデックスによって [ **LockThemeFonts** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ddae-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8ddae-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ddae-118">Section index:</span></span>  <br/> |<span data-ttu-id="8ddae-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8ddae-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8ddae-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ddae-120">Row index:</span></span>  <br/> |<span data-ttu-id="8ddae-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8ddae-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8ddae-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8ddae-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8ddae-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="8ddae-123">**visLockThemeFonts**</span></span> <br/> |
   

