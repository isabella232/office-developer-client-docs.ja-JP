---
title: '[DefaultTabstop] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: テキスト ブロックの既定のタブ位置の間隔を指定します。
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805214"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="27468-103">[DefaultTabstop] セル ([テキスト ブロックの書式設定] セクション)</span><span class="sxs-lookup"><span data-stu-id="27468-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="27468-104">テキスト ブロックの既定のタブ位置の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="27468-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27468-105">注釈</span><span class="sxs-lookup"><span data-stu-id="27468-105">Remarks</span></span>

<span data-ttu-id="27468-106">既定値は、英国単位で図面を作成した場合は 0.5 インチ、メートル法単位の場合は 1.5 cm になります。</span><span class="sxs-lookup"><span data-stu-id="27468-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="27468-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DefaultTabstop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="27468-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27468-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="27468-108">Cell name:</span></span>  <br/> |<span data-ttu-id="27468-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="27468-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="27468-110">プログラムから、インデックスによって [DefaultTabstop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="27468-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27468-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="27468-111">Section index:</span></span>  <br/> |<span data-ttu-id="27468-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27468-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="27468-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="27468-113">Row index:</span></span>  <br/> |<span data-ttu-id="27468-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="27468-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="27468-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="27468-115">Cell index:</span></span>  <br/> |<span data-ttu-id="27468-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="27468-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

