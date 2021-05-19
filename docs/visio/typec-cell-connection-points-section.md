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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415237"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="508a6-103">[Type / C] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="508a6-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="508a6-104">接続ポイントの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="508a6-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="508a6-105">**値**</span><span class="sxs-lookup"><span data-stu-id="508a6-105">**Value**</span></span>|<span data-ttu-id="508a6-106">**型**</span><span class="sxs-lookup"><span data-stu-id="508a6-106">**Type**</span></span>|<span data-ttu-id="508a6-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="508a6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="508a6-108">0</span><span class="sxs-lookup"><span data-stu-id="508a6-108">0</span></span>  <br/> |<span data-ttu-id="508a6-109">Inward</span><span class="sxs-lookup"><span data-stu-id="508a6-109">Inward</span></span>  <br/> |<span data-ttu-id="508a6-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="508a6-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="508a6-111">1</span><span class="sxs-lookup"><span data-stu-id="508a6-111">1</span></span>  <br/> |<span data-ttu-id="508a6-112">外向き</span><span class="sxs-lookup"><span data-stu-id="508a6-112">Outward</span></span>  <br/> |<span data-ttu-id="508a6-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="508a6-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="508a6-114">2</span><span class="sxs-lookup"><span data-stu-id="508a6-114">2</span></span>  <br/> |<span data-ttu-id="508a6-115">内側外側 &amp;</span><span class="sxs-lookup"><span data-stu-id="508a6-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="508a6-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="508a6-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="508a6-117">注釈</span><span class="sxs-lookup"><span data-stu-id="508a6-117">Remarks</span></span>

<span data-ttu-id="508a6-p101">接続ポイントの種類は、[**コネクタ**] ツールを選択し、図形を選択してから、接続ポイントを右クリックして設定することもできます。この操作は、[開発](run-in-developer-mode-display-the-developer-tab.md)モードで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="508a6-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="508a6-120">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type / C] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="508a6-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="508a6-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="508a6-121">Cell name:</span></span>  <br/> |<span data-ttu-id="508a6-122">Connections.Type[  *i*  ] where i =  *<*  1> 2, 3...</span><span class="sxs-lookup"><span data-stu-id="508a6-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="508a6-123">プログラムから、インデックスによって [Type / C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="508a6-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="508a6-124">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="508a6-124">Section index:</span></span>  <br/> |<span data-ttu-id="508a6-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="508a6-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="508a6-126">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="508a6-126">Row index:</span></span>  <br/> |<span data-ttu-id="508a6-127">**visRowConnectionPts**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="508a6-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="508a6-128">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="508a6-128">Cell index:</span></span>  <br/> |<span data-ttu-id="508a6-129">**visCnnctType** (拡張されていない行) **visCnnctC** (拡張行)</span><span class="sxs-lookup"><span data-stu-id="508a6-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="508a6-130">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="508a6-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

