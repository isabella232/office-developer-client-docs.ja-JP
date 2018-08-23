---
title: '[LockThemeIndex] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: '[テーマのプロパティ] 行の [ThemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805781"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="af725-104">[LockThemeIndex] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="af725-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="af725-p102">[**テーマのプロパティ**] 行の [**ThemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。</span><span class="sxs-lookup"><span data-stu-id="af725-p102">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme. Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="af725-107">**値**</span><span class="sxs-lookup"><span data-stu-id="af725-107">**Value**</span></span>|<span data-ttu-id="af725-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="af725-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af725-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="af725-109">TRUE</span></span>  <br/> |<span data-ttu-id="af725-110">シェイプシートを直接変更しない限り、[**ThemeIndex**] セルの現在の値は変更できません。</span><span class="sxs-lookup"><span data-stu-id="af725-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="af725-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="af725-111">FALSE</span></span>  <br/> |<span data-ttu-id="af725-112">テーマが変更された場合、 [**ThemeIndex**] セルの現在の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="af725-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af725-113">注釈</span><span class="sxs-lookup"><span data-stu-id="af725-113">Remarks</span></span>

<span data-ttu-id="af725-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeIndex**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="af725-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af725-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="af725-115">Cell name:</span></span>  <br/> | <span data-ttu-id="af725-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="af725-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="af725-117">プログラムから、インデックスによって [**LockThemeIndex**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="af725-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af725-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="af725-118">Section index:</span></span>  <br/> |<span data-ttu-id="af725-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af725-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="af725-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="af725-120">Row index:</span></span>  <br/> |<span data-ttu-id="af725-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="af725-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="af725-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="af725-122">Cell index:</span></span>  <br/> |<span data-ttu-id="af725-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="af725-123">**visLockThemeIndex**</span></span> <br/> |
   

