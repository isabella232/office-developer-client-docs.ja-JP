---
title: '[LockThemeFonts] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: 新しいテーマを適用することで、[Theme Properties] 行の [FontIndex] セルが変更されないようにします。ユーザーが手動でシェイプシートのこの値を編集することは防げません。
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805799"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="487a6-104">[LockThemeFonts] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="487a6-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="487a6-p102">新しいテーマを適用することで、[**Theme Properties**] 行の [**FontIndex**] セルが変更されないようにします。ユーザーが手動でシェイプシートのこの値を編集することは防げません。</span><span class="sxs-lookup"><span data-stu-id="487a6-p102">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme. Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="487a6-107">**値**</span><span class="sxs-lookup"><span data-stu-id="487a6-107">**Value**</span></span>|<span data-ttu-id="487a6-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="487a6-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="487a6-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="487a6-109">TRUE</span></span>  <br/> |<span data-ttu-id="487a6-110">[**FontIndex**] セルは、直接シェイプシートで変更しない限り、現在の値を変更できません。</span><span class="sxs-lookup"><span data-stu-id="487a6-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="487a6-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="487a6-111">FALSE</span></span>  <br/> |<span data-ttu-id="487a6-112">[**FontIndex**] セルは、テーマが変更された場合に現在の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="487a6-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="487a6-113">注釈</span><span class="sxs-lookup"><span data-stu-id="487a6-113">Remarks</span></span>

<span data-ttu-id="487a6-114">別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeFonts**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="487a6-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="487a6-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="487a6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="487a6-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="487a6-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="487a6-117">プログラムから、インデックスによって [**LockThemeFonts**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="487a6-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="487a6-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="487a6-118">Section index:</span></span>  <br/> |<span data-ttu-id="487a6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="487a6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="487a6-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="487a6-120">Row index:</span></span>  <br/> |<span data-ttu-id="487a6-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="487a6-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="487a6-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="487a6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="487a6-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="487a6-123">**visLockThemeFonts**</span></span> <br/> |
   

