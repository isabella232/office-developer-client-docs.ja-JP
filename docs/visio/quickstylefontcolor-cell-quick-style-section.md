---
title: '[QuickStyleFontColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: 図形のテキストがアクティブなテーマから継承するクイックスタイルのフォントの色を、0-1 からの整数で指定します。
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282636"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="ca4b9-103">[QuickStyleFontColor] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="ca4b9-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="ca4b9-104">図形のテキストがアクティブなテーマから継承するクイックスタイルのフォントの色を、0-1 からの整数で指定します。</span><span class="sxs-lookup"><span data-stu-id="ca4b9-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca4b9-105">値</span><span class="sxs-lookup"><span data-stu-id="ca4b9-105">Value</span></span>  <br/> |<span data-ttu-id="ca4b9-106">説明</span><span class="sxs-lookup"><span data-stu-id="ca4b9-106">Description</span></span>  <br/> |
|<span data-ttu-id="ca4b9-107">.0</span><span class="sxs-lookup"><span data-stu-id="ca4b9-107">0</span></span>  <br/> |<span data-ttu-id="ca4b9-108">図形のテキストは [ダーク] のフォントの色を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca4b9-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="ca4b9-109">1-d</span><span class="sxs-lookup"><span data-stu-id="ca4b9-109">1</span></span>  <br/> |<span data-ttu-id="ca4b9-110">図形のテキストは [ライト] のフォントの色を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca4b9-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca4b9-111">解説</span><span class="sxs-lookup"><span data-stu-id="ca4b9-111">Remarks</span></span>

<span data-ttu-id="ca4b9-112">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFontColor**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca4b9-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca4b9-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="ca4b9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ca4b9-114">[quickstylefontcolor]</span><span class="sxs-lookup"><span data-stu-id="ca4b9-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="ca4b9-115">プログラムから、インデックスによって [**QuickStyleFontColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca4b9-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca4b9-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca4b9-116">Section index:</span></span>  <br/> |<span data-ttu-id="ca4b9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca4b9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca4b9-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca4b9-118">Row index:</span></span>  <br/> |<span data-ttu-id="ca4b9-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="ca4b9-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="ca4b9-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ca4b9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ca4b9-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="ca4b9-121">**visQuickStyleFontColor**</span></span> <br/> |
   

