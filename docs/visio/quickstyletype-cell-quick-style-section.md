---
title: '[QuickStyleType] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: クイック スタイルの種類を決定 (2 次元、1 次元、またはコネクタ)、図形を継承します。
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806137"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="f2c31-103">[QuickStyleType] セル ([クイック スタイル] セクション)</span><span class="sxs-lookup"><span data-stu-id="f2c31-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="f2c31-104">クイック スタイルの種類を決定 (2 次元、1 次元、またはコネクタ)、図形を継承します。</span><span class="sxs-lookup"><span data-stu-id="f2c31-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="f2c31-105">**値**</span><span class="sxs-lookup"><span data-stu-id="f2c31-105">**Value**</span></span>|<span data-ttu-id="f2c31-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="f2c31-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2c31-107">0</span><span class="sxs-lookup"><span data-stu-id="f2c31-107">0</span></span>  <br/> |<span data-ttu-id="f2c31-108">Visio が自動的に選択します。</span><span class="sxs-lookup"><span data-stu-id="f2c31-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="f2c31-109">1</span><span class="sxs-lookup"><span data-stu-id="f2c31-109">1</span></span>  <br/> |<span data-ttu-id="f2c31-110">1 次元</span><span class="sxs-lookup"><span data-stu-id="f2c31-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="f2c31-111">2</span><span class="sxs-lookup"><span data-stu-id="f2c31-111">2</span></span>  <br/> |<span data-ttu-id="f2c31-112">2 次元</span><span class="sxs-lookup"><span data-stu-id="f2c31-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="f2c31-113">3</span><span class="sxs-lookup"><span data-stu-id="f2c31-113">3</span></span>  <br/> |<span data-ttu-id="f2c31-114">コネクタ</span><span class="sxs-lookup"><span data-stu-id="f2c31-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2c31-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f2c31-115">Remarks</span></span>

<span data-ttu-id="f2c31-116">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleType** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="f2c31-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2c31-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="f2c31-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f2c31-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="f2c31-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="f2c31-119">プログラムから、インデックスによって [ **QuickStyleType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="f2c31-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2c31-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2c31-120">Section index:</span></span>  <br/> |<span data-ttu-id="f2c31-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f2c31-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f2c31-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2c31-122">Row index:</span></span>  <br/> |<span data-ttu-id="f2c31-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="f2c31-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="f2c31-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2c31-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f2c31-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="f2c31-125">**visQuickStyleType**</span></span> <br/> |
   

