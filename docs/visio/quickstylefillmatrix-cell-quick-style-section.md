---
title: '[QuickStyleFillMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8513cf3f-42bd-4e76-bfa8-8bf12f0d1296
description: 使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。
ms.openlocfilehash: fca0d9f8fe58fdc7c227e9c093b418ffef1ccb52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358717"
---
# <a name="quickstylefillmatrix-cell-quick-style-section"></a><span data-ttu-id="cbd02-103">[QuickStyleFillMatrix] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="cbd02-103">QuickStyleFillMatrix Cell (Quick Style Section)</span></span>

<span data-ttu-id="cbd02-104">使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。</span><span class="sxs-lookup"><span data-stu-id="cbd02-104">Determines the Quick Style fill style that the shape inherits from the active theme, as an integer from 0-6.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cbd02-105">解説</span><span class="sxs-lookup"><span data-stu-id="cbd02-105">Remarks</span></span>

<span data-ttu-id="cbd02-106">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFillMatrix**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cbd02-106">To get a reference to the **QuickStyleFillMatrix** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbd02-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="cbd02-107">Cell name:</span></span>  <br/> | <span data-ttu-id="cbd02-108">[quickstylefillmatrix]</span><span class="sxs-lookup"><span data-stu-id="cbd02-108">QuickStyleFillMatrix</span></span>  <br/> |
   
<span data-ttu-id="cbd02-109">プログラムから、インデックスによって [**QuickStyleFillMatrix**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cbd02-109">To get a reference to the **QuickStyleFillMatrix** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbd02-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbd02-110">Section index:</span></span>  <br/> |<span data-ttu-id="cbd02-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cbd02-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cbd02-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbd02-112">Row index:</span></span>  <br/> |<span data-ttu-id="cbd02-113">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="cbd02-113">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="cbd02-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cbd02-114">Cell index:</span></span>  <br/> |<span data-ttu-id="cbd02-115">**visQuickStyleFillMatrix**</span><span class="sxs-lookup"><span data-stu-id="cbd02-115">**visQuickStyleFillMatrix**</span></span> <br/> |
   

