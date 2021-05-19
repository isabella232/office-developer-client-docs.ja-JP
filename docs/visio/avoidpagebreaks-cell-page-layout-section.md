---
title: '[AvoidPageBreaks] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80000
localization_priority: Normal
ms.assetid: 7d2ec869-7ffa-3b41-8126-3f4889501e0c
description: 図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。
ms.openlocfilehash: 5ff5a31e26cc1ab9415eb69b76fc9f64ccd1ae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416315"
---
# <a name="avoidpagebreaks-cell-page-layout-section"></a><span data-ttu-id="b7e57-103">[AvoidPageBreaks] セル ([Page Layout] セクション)</span><span class="sxs-lookup"><span data-stu-id="b7e57-103">AvoidPageBreaks Cell (Page Layout Section)</span></span>

<span data-ttu-id="b7e57-104">図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b7e57-104">Determines whether shapes can be placed over page breaks when the shapes are incrementally aligned, incrementally spaced, or both.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7e57-105">注釈</span><span class="sxs-lookup"><span data-stu-id="b7e57-105">Remarks</span></span>

<span data-ttu-id="b7e57-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvoidPageBreaks] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7e57-106">To get a reference to the AvoidPageBreaks cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7e57-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="b7e57-107">Cell name:</span></span>  <br/> |<span data-ttu-id="b7e57-108">AvoidPageBreaks</span><span class="sxs-lookup"><span data-stu-id="b7e57-108">AvoidPageBreaks</span></span>  <br/> |
   
<span data-ttu-id="b7e57-109">プログラムから、インデックスによって [AvoidPageBreaks] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7e57-109">To get a reference to the AvoidPageBreaks cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7e57-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7e57-110">Section index:</span></span>  <br/> |<span data-ttu-id="b7e57-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b7e57-111">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b7e57-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7e57-112">Row index:</span></span>  <br/> |<span data-ttu-id="b7e57-113">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b7e57-113">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b7e57-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7e57-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b7e57-115">**visPLOAvoidPageBreaks**</span><span class="sxs-lookup"><span data-stu-id="b7e57-115">**visPLOAvoidPageBreaks**</span></span> <br/> |
   

