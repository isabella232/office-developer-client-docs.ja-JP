---
title: '[OutputFormat] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: 図面の出力形式を指定します。 図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413886"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="15205-104">[OutputFormat] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="15205-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="15205-105">図面の出力形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="15205-105">Determines the output format for a drawing.</span></span> <span data-ttu-id="15205-106">図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="15205-106">Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="15205-107">**値**</span><span class="sxs-lookup"><span data-stu-id="15205-107">**Value**</span></span>|<span data-ttu-id="15205-108">**出力形式**</span><span class="sxs-lookup"><span data-stu-id="15205-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="15205-109">.0</span><span class="sxs-lookup"><span data-stu-id="15205-109">0</span></span>  <br/> | <span data-ttu-id="15205-110">印刷 (既定値)</span><span class="sxs-lookup"><span data-stu-id="15205-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="15205-111">1 </span><span class="sxs-lookup"><span data-stu-id="15205-111">1</span></span>  <br/> | <span data-ttu-id="15205-112">PowerPoint スライド ショー</span><span class="sxs-lookup"><span data-stu-id="15205-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="15205-113">2 </span><span class="sxs-lookup"><span data-stu-id="15205-113">2</span></span>  <br/> | <span data-ttu-id="15205-114">HTML または GIF 出力</span><span class="sxs-lookup"><span data-stu-id="15205-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15205-115">注釈</span><span class="sxs-lookup"><span data-stu-id="15205-115">Remarks</span></span>

<span data-ttu-id="15205-116">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [OutputFormat] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="15205-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15205-117">セル名 :</span><span class="sxs-lookup"><span data-stu-id="15205-117">Cell name:</span></span>  <br/> | <span data-ttu-id="15205-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="15205-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="15205-119">プログラムから、インデックスによって [OutputFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="15205-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15205-120">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="15205-120">Section index:</span></span>  <br/> |<span data-ttu-id="15205-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15205-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="15205-122">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="15205-122">Row index:</span></span>  <br/> |<span data-ttu-id="15205-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="15205-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="15205-124">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="15205-124">Cell index:</span></span>  <br/> |<span data-ttu-id="15205-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="15205-125">**visDocOutputFormat**</span></span> <br/> |
   

