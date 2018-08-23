---
title: '[QuickStyleFontColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: 図形のテキストが 0-1 整数値で、作業中のテーマから継承したクイック スタイルからフォントの色を決定します。
ms.openlocfilehash: 8f2d77508dccffccf472f8ab80517e840f860541
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806132"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="7bd1d-103">[QuickStyleFontColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="7bd1d-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="7bd1d-104">図形のテキストが 0-1 整数値で、作業中のテーマから継承したクイック スタイルからフォントの色を決定します。</span><span class="sxs-lookup"><span data-stu-id="7bd1d-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bd1d-105">値</span><span class="sxs-lookup"><span data-stu-id="7bd1d-105">Value</span></span>  <br/> |<span data-ttu-id="7bd1d-106">説明</span><span class="sxs-lookup"><span data-stu-id="7bd1d-106">Description</span></span>  <br/> |
|<span data-ttu-id="7bd1d-107">0</span><span class="sxs-lookup"><span data-stu-id="7bd1d-107">0</span></span>  <br/> |<span data-ttu-id="7bd1d-108">図形のテキストは [ダーク] のフォントの色を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bd1d-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="7bd1d-109">1</span><span class="sxs-lookup"><span data-stu-id="7bd1d-109">1</span></span>  <br/> |<span data-ttu-id="7bd1d-110">図形のテキストは [ライト] のフォントの色を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bd1d-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bd1d-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="7bd1d-111">Remarks</span></span>

<span data-ttu-id="7bd1d-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFontColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bd1d-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7bd1d-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7bd1d-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="7bd1d-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="7bd1d-115">プログラムから、インデックスによって [**QuickStyleFontColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bd1d-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7bd1d-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-116">Section index:</span></span>  <br/> |<span data-ttu-id="7bd1d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7bd1d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7bd1d-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-118">Row index:</span></span>  <br/> |<span data-ttu-id="7bd1d-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="7bd1d-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="7bd1d-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7bd1d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7bd1d-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="7bd1d-121">**visQuickStyleFontColor**</span></span> <br/> |
   

