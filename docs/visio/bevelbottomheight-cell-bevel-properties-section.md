---
title: '[BevelBottomHeight] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ff681afd-c058-4fce-855f-5075b8c680c2
description: ポイント単位での図形の下の面取りの高さを決定します。
ms.openlocfilehash: 4ff422a885dba214559792e17407b349223e9633
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804819"
---
# <a name="bevelbottomheight-cell-bevel-properties-section"></a><span data-ttu-id="cf99c-103">[BevelBottomHeight] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="cf99c-103">BevelBottomHeight Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="cf99c-104">ポイント単位での図形の下の面取りの高さを決定します。</span><span class="sxs-lookup"><span data-stu-id="cf99c-104">Determines the height of a shape's bottom bevel in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf99c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="cf99c-105">Remarks</span></span>

<span data-ttu-id="cf99c-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelBottomHeight** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="cf99c-106">To get a reference to the **BevelBottomHeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf99c-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="cf99c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="cf99c-108">BevelBottomHeight</span><span class="sxs-lookup"><span data-stu-id="cf99c-108">BevelBottomHeight</span></span>  <br/> |
   
<span data-ttu-id="cf99c-109">プログラムから、インデックスによって [ **BevelBottomHeight** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf99c-109">To get a reference to the **BevelBottomHeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf99c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf99c-110">Section index:</span></span>  <br/> |<span data-ttu-id="cf99c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf99c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cf99c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf99c-112">Row index:</span></span>  <br/> |<span data-ttu-id="cf99c-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="cf99c-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="cf99c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf99c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="cf99c-115">**visBevelBottomHeight**</span><span class="sxs-lookup"><span data-stu-id="cf99c-115">**visBevelBottomHeight**</span></span> <br/> |
   

