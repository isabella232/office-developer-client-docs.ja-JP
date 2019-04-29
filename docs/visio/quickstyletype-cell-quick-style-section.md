---
title: '[QuickStyleType] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: 図形が継承するクイックスタイルの種類 (2 次元、1次元、またはコネクタ) を指定します。
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410505"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="709ba-103">[QuickStyleType] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="709ba-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="709ba-104">図形が継承するクイックスタイルの種類 (2 次元、1次元、またはコネクタ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="709ba-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="709ba-105">**値**</span><span class="sxs-lookup"><span data-stu-id="709ba-105">**Value**</span></span>|<span data-ttu-id="709ba-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="709ba-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="709ba-107">.0</span><span class="sxs-lookup"><span data-stu-id="709ba-107">0</span></span>  <br/> |<span data-ttu-id="709ba-108">Visio が自動的に選択する</span><span class="sxs-lookup"><span data-stu-id="709ba-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="709ba-109">1 </span><span class="sxs-lookup"><span data-stu-id="709ba-109">1</span></span>  <br/> |<span data-ttu-id="709ba-110">1次元</span><span class="sxs-lookup"><span data-stu-id="709ba-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="709ba-111">2 </span><span class="sxs-lookup"><span data-stu-id="709ba-111">2</span></span>  <br/> |<span data-ttu-id="709ba-112">2次元</span><span class="sxs-lookup"><span data-stu-id="709ba-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="709ba-113">3 </span><span class="sxs-lookup"><span data-stu-id="709ba-113">3</span></span>  <br/> |<span data-ttu-id="709ba-114">Connector</span><span class="sxs-lookup"><span data-stu-id="709ba-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="709ba-115">注釈</span><span class="sxs-lookup"><span data-stu-id="709ba-115">Remarks</span></span>

<span data-ttu-id="709ba-116">別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [**クイックスタイルの種類**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="709ba-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="709ba-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="709ba-117">Cell name:</span></span>  <br/> | <span data-ttu-id="709ba-118">[quickstyletype]</span><span class="sxs-lookup"><span data-stu-id="709ba-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="709ba-119">プログラムから、インデックスによって [**クイックスタイルの種類**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="709ba-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="709ba-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="709ba-120">Section index:</span></span>  <br/> |<span data-ttu-id="709ba-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="709ba-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="709ba-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="709ba-122">Row index:</span></span>  <br/> |<span data-ttu-id="709ba-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="709ba-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="709ba-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="709ba-124">Cell index:</span></span>  <br/> |<span data-ttu-id="709ba-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="709ba-125">**visQuickStyleType**</span></span> <br/> |
   

