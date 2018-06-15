---
title: '[EmbellishmentIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98f7ebdc-fdd5-4534-97dc-9d4c00490d62
description: コールアウト、コンテナー、タイムライン、および組織図の図形の外観と動作 (装飾) を変更します。
ms.openlocfilehash: 93c12a3eed1c7298b37f143fc836ad90ec3b09ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805299"
---
# <a name="embellishmentindex-cell-theme-properties-section"></a><span data-ttu-id="9fc11-103">[EmbellishmentIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="9fc11-103">EmbellishmentIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="9fc11-104">コールアウト、コンテナー、タイムライン、および組織図の図形の外観と動作 (装飾) を変更します。</span><span class="sxs-lookup"><span data-stu-id="9fc11-104">Changes the look and feel (embellishment) of callouts, containers, timelines, and organization chart shapes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9fc11-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="9fc11-105">Remarks</span></span>

<span data-ttu-id="9fc11-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **EmbellishmentIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9fc11-106">To get a reference to the **EmbellishmentIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fc11-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="9fc11-107">Cell name:</span></span>  <br/> | <span data-ttu-id="9fc11-108">EmbellishmentIndex</span><span class="sxs-lookup"><span data-stu-id="9fc11-108">EmbellishmentIndex</span></span>  <br/> |
   
<span data-ttu-id="9fc11-109">プログラムから、インデックスによって [ **EmbellishmentIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9fc11-109">To get a reference to the **EmbellishmentIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9fc11-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fc11-110">Section index:</span></span>  <br/> |<span data-ttu-id="9fc11-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9fc11-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9fc11-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fc11-112">Row index:</span></span>  <br/> |<span data-ttu-id="9fc11-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="9fc11-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="9fc11-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fc11-114">Cell index:</span></span>  <br/> |<span data-ttu-id="9fc11-115">**visEmbellishmentIndex**</span><span class="sxs-lookup"><span data-stu-id="9fc11-115">**visEmbellishmentIndex**</span></span> <br/> |
   

