---
title: '[Type / C] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: 接続ポイントの種類を指定します。
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359585"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="d4179-103">[Type / C] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="d4179-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="d4179-104">接続ポイントの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4179-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="d4179-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d4179-105">**Value**</span></span>|<span data-ttu-id="d4179-106">**型**</span><span class="sxs-lookup"><span data-stu-id="d4179-106">**Type**</span></span>|<span data-ttu-id="d4179-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="d4179-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4179-108">.0</span><span class="sxs-lookup"><span data-stu-id="d4179-108">0</span></span>  <br/> |<span data-ttu-id="d4179-109">向き</span><span class="sxs-lookup"><span data-stu-id="d4179-109">Inward</span></span>  <br/> |<span data-ttu-id="d4179-110">**viscnncttypeinward**</span><span class="sxs-lookup"><span data-stu-id="d4179-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="d4179-111">1-d</span><span class="sxs-lookup"><span data-stu-id="d4179-111">1</span></span>  <br/> |<span data-ttu-id="d4179-112">ふき</span><span class="sxs-lookup"><span data-stu-id="d4179-112">Outward</span></span>  <br/> |<span data-ttu-id="d4179-113">**viscnncttypeoutward**</span><span class="sxs-lookup"><span data-stu-id="d4179-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="d4179-114">pbm-2</span><span class="sxs-lookup"><span data-stu-id="d4179-114">2</span></span>  <br/> |<span data-ttu-id="d4179-115">内側&amp;外側</span><span class="sxs-lookup"><span data-stu-id="d4179-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="d4179-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="d4179-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4179-117">解説</span><span class="sxs-lookup"><span data-stu-id="d4179-117">Remarks</span></span>

<span data-ttu-id="d4179-p101">接続ポイントの種類は、[**コネクタ**] ツールを選択し、図形を選択してから、接続ポイントを右クリックして設定することもできます。この操作は、[開発](run-in-developer-mode-display-the-developer-tab.md)モードで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4179-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="d4179-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type / C] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4179-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4179-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="d4179-121">Cell name:</span></span>  <br/> |<span data-ttu-id="d4179-122">接続を指定し\*\* ます。ここで、 *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d4179-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d4179-123">プログラムから、インデックスによって [Type / C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4179-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4179-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4179-124">Section index:</span></span>  <br/> |<span data-ttu-id="d4179-125">**持つ vissectionconnectionpts**</span><span class="sxs-lookup"><span data-stu-id="d4179-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="d4179-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4179-126">Row index:</span></span>  <br/> |<span data-ttu-id="d4179-127">**visRowConnectionPts** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="d4179-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d4179-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d4179-128">Cell index:</span></span>  <br/> |<span data-ttu-id="d4179-129">**viscnncttype**(非拡張行)**viscnnctc**(拡張行)</span><span class="sxs-lookup"><span data-stu-id="d4179-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="d4179-130">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4179-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

