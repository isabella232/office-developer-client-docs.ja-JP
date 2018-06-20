---
title: '[FontSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b832d75b-dac2-495f-b86e-d7fc5a484cab
description: 整数値で、図形に適用されているテーマのフォント パターンを決定します。
ms.openlocfilehash: 5b93a24afd113d8019c891e324ebcf4757d1e587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805424"
---
# <a name="fontschemeindex-cell-theme-properties-section"></a><span data-ttu-id="b3224-103">[FontSchemeIndex] セル ([テーマのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="b3224-103">FontSchemeIndex Cell (Theme Properties Section</span></span>

<span data-ttu-id="b3224-104">整数値で、図形に適用されているテーマのフォント パターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="b3224-104">Determines the font scheme of a theme that is applied to the shape, as an integer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3224-105">備考</span><span class="sxs-lookup"><span data-stu-id="b3224-105">Remarks</span></span>

<span data-ttu-id="b3224-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **FontSchemeIndex** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="b3224-106">To get a reference to the **FontSchemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3224-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="b3224-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b3224-108">FontSchemeIndex</span><span class="sxs-lookup"><span data-stu-id="b3224-108">FontSchemeIndex</span></span>  <br/> |
   
<span data-ttu-id="b3224-109">プログラムから、インデックスによって [ **FontSchemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3224-109">To get a reference to the **FontSchemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3224-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3224-110">Section index:</span></span>  <br/> |<span data-ttu-id="b3224-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3224-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3224-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3224-112">Row index:</span></span>  <br/> |<span data-ttu-id="b3224-113">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="b3224-113">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="b3224-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b3224-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b3224-115">**visFontSchemeIndex**</span><span class="sxs-lookup"><span data-stu-id="b3224-115">**visFontSchemeIndex**</span></span> <br/> |
   

