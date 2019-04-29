---
title: '[LockThemeFonts] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: 新しいテーマを適用することで、[Theme Properties] 行の [FontIndex] セルが変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421229"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="b28ba-104">[LockThemeFonts] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="b28ba-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="b28ba-105">新しいテーマを適用することで、[**Theme Properties**] 行の [**FontIndex**] セルが変更されないようにします。</span><span class="sxs-lookup"><span data-stu-id="b28ba-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="b28ba-106">ユーザーがシェイプシートのこの値を手動で変更することは防げません。</span><span class="sxs-lookup"><span data-stu-id="b28ba-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="b28ba-107">**値**</span><span class="sxs-lookup"><span data-stu-id="b28ba-107">**Value**</span></span>|<span data-ttu-id="b28ba-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="b28ba-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b28ba-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="b28ba-109">TRUE</span></span>  <br/> |<span data-ttu-id="b28ba-110">[**FontIndex**] セルは、直接シェイプシートで変更しない限り、現在の値を変更できません。</span><span class="sxs-lookup"><span data-stu-id="b28ba-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="b28ba-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="b28ba-111">FALSE</span></span>  <br/> |<span data-ttu-id="b28ba-112">[**FontIndex**] セルは、テーマが変更された場合に現在の値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="b28ba-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b28ba-113">注釈</span><span class="sxs-lookup"><span data-stu-id="b28ba-113">Remarks</span></span>

<span data-ttu-id="b28ba-114">別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeFonts**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b28ba-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b28ba-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="b28ba-115">Cell name:</span></span>  <br/> | <span data-ttu-id="b28ba-116">[lockthemefonts]</span><span class="sxs-lookup"><span data-stu-id="b28ba-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="b28ba-117">プログラムから、インデックスによって [**LockThemeFonts**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b28ba-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b28ba-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b28ba-118">Section index:</span></span>  <br/> |<span data-ttu-id="b28ba-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b28ba-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b28ba-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b28ba-120">Row index:</span></span>  <br/> |<span data-ttu-id="b28ba-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b28ba-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b28ba-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b28ba-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b28ba-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="b28ba-123">**visLockThemeFonts**</span></span> <br/> |
   

