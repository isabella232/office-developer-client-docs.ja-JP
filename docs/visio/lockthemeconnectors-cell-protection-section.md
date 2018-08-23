---
title: '[LockThemeConnectors] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: '[テーマのプロパティ] 行の [ConnectorsSchemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805778"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="23efe-104">[LockThemeConnectors] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="23efe-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="23efe-p102">[**テーマのプロパティ**] 行の [**ConnectorsSchemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。</span><span class="sxs-lookup"><span data-stu-id="23efe-p102">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme. Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="23efe-107">**値**</span><span class="sxs-lookup"><span data-stu-id="23efe-107">**Value**</span></span>|<span data-ttu-id="23efe-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="23efe-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23efe-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="23efe-109">TRUE</span></span>  <br/> |<span data-ttu-id="23efe-110">シェイプシートを直接変更しない限り、[**ConnectorsSchemeIndex**] セルの現在の値は変更できません。</span><span class="sxs-lookup"><span data-stu-id="23efe-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="23efe-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="23efe-111">FALSE</span></span>  <br/> |<span data-ttu-id="23efe-112">[**ConnectorsSchemeIndex**] セルの現在の値は、UI を使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="23efe-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23efe-113">注釈</span><span class="sxs-lookup"><span data-stu-id="23efe-113">Remarks</span></span>

<span data-ttu-id="23efe-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeConnectors**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="23efe-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23efe-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="23efe-115">Cell name:</span></span>  <br/> | <span data-ttu-id="23efe-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="23efe-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="23efe-117">プログラムから、インデックスによって [**LockThemeConnectors**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="23efe-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23efe-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="23efe-118">Section index:</span></span>  <br/> |<span data-ttu-id="23efe-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23efe-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23efe-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="23efe-120">Row index:</span></span>  <br/> |<span data-ttu-id="23efe-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="23efe-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="23efe-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="23efe-122">Cell index:</span></span>  <br/> |<span data-ttu-id="23efe-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="23efe-123">**visLockThemeConnectors**</span></span> <br/> |
   

