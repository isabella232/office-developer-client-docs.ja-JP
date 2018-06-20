---
title: '[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: ブール値として、他の図形と図形がグループ化されたときに図形のグラデーションにされるかどうかを決定します。 UseGroupGradient のセルの値は、図形の塗りつぶしのみに影響します。
ms.openlocfilehash: ca11ad1c54097b4883bb5348583c6cf39127e4e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806736"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="64596-104">[UseGroupGradient] セル ([グラデーションのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="64596-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="64596-105">ブール値として、他の図形と図形がグループ化されたときに図形のグラデーションにされるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="64596-105">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean.</span></span> <span data-ttu-id="64596-106">**UseGroupGradient**のセルの値は、図形の塗りつぶしのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="64596-106">The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="64596-107">備考</span><span class="sxs-lookup"><span data-stu-id="64596-107">Remarks</span></span>

<span data-ttu-id="64596-108">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **UseGroupGradient** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="64596-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64596-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="64596-109">Cell name:</span></span>  <br/> | <span data-ttu-id="64596-110">UseGroupGradient</span><span class="sxs-lookup"><span data-stu-id="64596-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="64596-111">プログラムから、インデックスによって [ **UseGroupGradient** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="64596-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="64596-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="64596-112">Section index:</span></span>  <br/> |<span data-ttu-id="64596-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="64596-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="64596-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="64596-114">Row index:</span></span>  <br/> |<span data-ttu-id="64596-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="64596-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="64596-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="64596-116">Cell index:</span></span>  <br/> |<span data-ttu-id="64596-117">* * visUseGroupGradient * *</span><span class="sxs-lookup"><span data-stu-id="64596-117">**visUseGroupGradient **</span></span> <br/> |
   

