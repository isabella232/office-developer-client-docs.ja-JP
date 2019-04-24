---
title: '[LockThemeIndex] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: '[テーマのプロパティ] 行の [ThemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358080"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="640ab-104">[LockThemeIndex] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="640ab-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="640ab-105">[**テーマのプロパティ**] 行の [**ThemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。</span><span class="sxs-lookup"><span data-stu-id="640ab-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="640ab-106">ユーザーがシェイプシートのこの値を手動で変更することは防げません。</span><span class="sxs-lookup"><span data-stu-id="640ab-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="640ab-107">**値**</span><span class="sxs-lookup"><span data-stu-id="640ab-107">**Value**</span></span>|<span data-ttu-id="640ab-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="640ab-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="640ab-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="640ab-109">TRUE</span></span>  <br/> |<span data-ttu-id="640ab-110">シェイプシートを直接変更しない限り、[**ThemeIndex**] セルの現在の値は変更できません。</span><span class="sxs-lookup"><span data-stu-id="640ab-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="640ab-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="640ab-111">FALSE</span></span>  <br/> |<span data-ttu-id="640ab-112">テーマが変更された場合、 [**ThemeIndex**] セルの現在の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="640ab-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="640ab-113">解説</span><span class="sxs-lookup"><span data-stu-id="640ab-113">Remarks</span></span>

<span data-ttu-id="640ab-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeIndex**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="640ab-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="640ab-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="640ab-115">Cell name:</span></span>  <br/> | <span data-ttu-id="640ab-116">[lockthemeindex]</span><span class="sxs-lookup"><span data-stu-id="640ab-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="640ab-117">プログラムから、インデックスによって [**LockThemeIndex**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="640ab-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="640ab-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="640ab-118">Section index:</span></span>  <br/> |<span data-ttu-id="640ab-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="640ab-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="640ab-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="640ab-120">Row index:</span></span>  <br/> |<span data-ttu-id="640ab-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="640ab-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="640ab-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="640ab-122">Cell index:</span></span>  <br/> |<span data-ttu-id="640ab-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="640ab-123">**visLockThemeIndex**</span></span> <br/> |
   

