---
title: '[LockThemeIndex] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: 新しいテーマを適用するか、新しいコネクタの設定を選択することによって変更されているテーマのプロパティの行のセルを ThemeIndex できないようにします。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805781"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="dfca3-104">[LockThemeIndex] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="dfca3-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="dfca3-105">新しいテーマを適用するか、新しいコネクタの設定を選択することによって変更されている**テーマのプロパティ**の行のセルを**ThemeIndex**できないようにします。</span><span class="sxs-lookup"><span data-stu-id="dfca3-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="dfca3-106">でも、ユーザーからシェイプ シート内でこの値を手動で編集します。</span><span class="sxs-lookup"><span data-stu-id="dfca3-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="dfca3-107">**値**</span><span class="sxs-lookup"><span data-stu-id="dfca3-107">**Value**</span></span>|<span data-ttu-id="dfca3-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="dfca3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dfca3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="dfca3-109">TRUE</span></span>  <br/> |<span data-ttu-id="dfca3-110">シェイプ シートで直接変更しない限り、現在の値から**ThemeIndex**のセルを変更できません。</span><span class="sxs-lookup"><span data-stu-id="dfca3-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="dfca3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="dfca3-111">FALSE</span></span>  <br/> |<span data-ttu-id="dfca3-112">テーマが変更されると、現在の値から**ThemeIndex**のセルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="dfca3-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfca3-113">備考</span><span class="sxs-lookup"><span data-stu-id="dfca3-113">Remarks</span></span>

<span data-ttu-id="dfca3-114">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="dfca3-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfca3-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="dfca3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="dfca3-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="dfca3-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="dfca3-117">プログラムから、インデックスによって [ **LockThemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="dfca3-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dfca3-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfca3-118">Section index:</span></span>  <br/> |<span data-ttu-id="dfca3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfca3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dfca3-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfca3-120">Row index:</span></span>  <br/> |<span data-ttu-id="dfca3-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="dfca3-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="dfca3-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfca3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dfca3-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="dfca3-123">**visLockThemeIndex**</span></span> <br/> |
   

