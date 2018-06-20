---
title: '[LockVariation] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805795"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="054e1-103">[LockVariation] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="054e1-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="054e1-104">ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="054e1-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="054e1-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="054e1-105">TRUE</span></span>  <br/> |<span data-ttu-id="054e1-106">ページまたは図形に適用された現在のバリエーションは変更できません。</span><span class="sxs-lookup"><span data-stu-id="054e1-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="054e1-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="054e1-107">FALSE</span></span>  <br/> |<span data-ttu-id="054e1-108">ページまたは図形のバリエーションは変更できます。</span><span class="sxs-lookup"><span data-stu-id="054e1-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="054e1-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="054e1-109">Remarks</span></span>

<span data-ttu-id="054e1-110">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockVariation** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="054e1-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="054e1-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="054e1-111">Cell name:</span></span>  <br/> | <span data-ttu-id="054e1-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="054e1-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="054e1-113">プログラムから、インデックスによって [ **LockVariation** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="054e1-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="054e1-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="054e1-114">Section index:</span></span>  <br/> |<span data-ttu-id="054e1-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="054e1-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="054e1-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="054e1-116">Row index:</span></span>  <br/> |<span data-ttu-id="054e1-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="054e1-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="054e1-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="054e1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="054e1-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="054e1-119">**visLockVariation**</span></span> <br/> |
   

