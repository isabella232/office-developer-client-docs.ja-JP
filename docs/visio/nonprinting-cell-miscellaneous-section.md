---
title: '[NonPrinting] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: 選択した図形の印刷のオン/オフを切り替えます。
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805922"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="dbe59-103">[NonPrinting] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="dbe59-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="dbe59-104">選択した図形の印刷のオン/オフを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="dbe59-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="dbe59-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dbe59-105">**Value**</span></span>|<span data-ttu-id="dbe59-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="dbe59-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dbe59-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dbe59-107">TRUE</span></span>  <br/> | <span data-ttu-id="dbe59-108">印刷は無効になりますが、図形は図面ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="dbe59-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="dbe59-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dbe59-109">FALSE</span></span>  <br/> | <span data-ttu-id="dbe59-110">印刷は有効になります。</span><span class="sxs-lookup"><span data-stu-id="dbe59-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbe59-111">備考</span><span class="sxs-lookup"><span data-stu-id="dbe59-111">Remarks</span></span>

<span data-ttu-id="dbe59-112">ガイドを選択し、その [NonPrinting] セルの値を FALSE に設定すると、ガイドを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="dbe59-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="dbe59-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NonPrinting] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="dbe59-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbe59-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="dbe59-114">Cell name:</span></span>  <br/> | <span data-ttu-id="dbe59-115">印刷できません。</span><span class="sxs-lookup"><span data-stu-id="dbe59-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="dbe59-116">プログラムから、インデックスによって [NonPrinting] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="dbe59-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbe59-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dbe59-117">Section index:</span></span>  <br/> |<span data-ttu-id="dbe59-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dbe59-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dbe59-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dbe59-119">Row index:</span></span>  <br/> |<span data-ttu-id="dbe59-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="dbe59-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="dbe59-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dbe59-121">Cell index:</span></span>  <br/> |<span data-ttu-id="dbe59-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="dbe59-122">**visNonPrinting**</span></span> <br/> |
   

