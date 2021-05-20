---
title: '[LockVariation] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427928"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="a0ec5-103">[LockVariation] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="a0ec5-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="a0ec5-104">ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="a0ec5-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0ec5-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="a0ec5-105">TRUE</span></span>  <br/> |<span data-ttu-id="a0ec5-106">ページまたは図形に適用された現在のバリエーションは変更できません。</span><span class="sxs-lookup"><span data-stu-id="a0ec5-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="a0ec5-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="a0ec5-107">FALSE</span></span>  <br/> |<span data-ttu-id="a0ec5-108">ページまたは図形のバリエーションは変更できます。</span><span class="sxs-lookup"><span data-stu-id="a0ec5-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0ec5-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a0ec5-109">Remarks</span></span>

<span data-ttu-id="a0ec5-110">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockVariation**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0ec5-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0ec5-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="a0ec5-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a0ec5-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="a0ec5-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="a0ec5-113">プログラムから、インデックスによって [**LockVariation**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0ec5-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a0ec5-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0ec5-114">Section index:</span></span>  <br/> |<span data-ttu-id="a0ec5-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0ec5-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a0ec5-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0ec5-116">Row index:</span></span>  <br/> |<span data-ttu-id="a0ec5-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="a0ec5-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="a0ec5-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a0ec5-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a0ec5-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="a0ec5-119">**visLockVariation**</span></span> <br/> |
   

