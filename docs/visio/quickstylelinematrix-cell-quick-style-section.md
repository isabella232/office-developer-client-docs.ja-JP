---
title: '[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b10221d-30f8-48f5-81ed-0283fdfc3e5d
description: 0-6 の整数として、図形を継承するクイック スタイルのスタイルを指定します。
ms.openlocfilehash: 31d5c6e7c3e0e3f10847c44d5545b2687a7e99b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806139"
---
# <a name="quickstylelinematrix-cell-quick-style-section"></a><span data-ttu-id="4e697-103">[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="4e697-103">QuickStyleLineMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="4e697-104">0-6 の整数として、図形を継承するクイック スタイルのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="4e697-104">Determines the Quick Style line style that the shape inherits, as an integer from 0-6.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4e697-105">備考</span><span class="sxs-lookup"><span data-stu-id="4e697-105">Remarks</span></span>

<span data-ttu-id="4e697-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleLineMatrix** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4e697-106">To get a reference to the **QuickStyleLineMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e697-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="4e697-107">Cell name:</span></span>  <br/> | <span data-ttu-id="4e697-108">QuickStyleLineMatrix</span><span class="sxs-lookup"><span data-stu-id="4e697-108">QuickStyleLineMatrix</span></span>  <br/> |
   
<span data-ttu-id="4e697-109">プログラムから、インデックスによって [ **QuickStyleLineMatrix** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e697-109">To get a reference to the **QuickStyleLineMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e697-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e697-110">Section index:</span></span>  <br/> |<span data-ttu-id="4e697-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4e697-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4e697-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e697-112">Row index:</span></span>  <br/> |<span data-ttu-id="4e697-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="4e697-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="4e697-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4e697-114">Cell index:</span></span>  <br/> |<span data-ttu-id="4e697-115">**visQuickStyleLineMatrix**</span><span class="sxs-lookup"><span data-stu-id="4e697-115">**visQuickStyleLineMatrix**</span></span> <br/> |
   

