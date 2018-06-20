---
title: '[EnableFillProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 399af4b9d1a2245ea7a9b91ebbf036eb122f15bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805312"
---
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="da34b-103">[EnableFillProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="da34b-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="da34b-104">スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="da34b-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="da34b-105">**値**</span><span class="sxs-lookup"><span data-stu-id="da34b-105">**Value**</span></span>|<span data-ttu-id="da34b-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="da34b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da34b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="da34b-107">TRUE</span></span>  <br/> |<span data-ttu-id="da34b-108">塗りつぶしのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="da34b-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="da34b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="da34b-109">FALSE</span></span>  <br/> |<span data-ttu-id="da34b-110">塗りつぶしのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="da34b-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da34b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="da34b-111">Remarks</span></span>

<span data-ttu-id="da34b-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[EnableFillProps] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="da34b-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da34b-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="da34b-113">Cell name:</span></span>  <br/> |<span data-ttu-id="da34b-114">EnableFillProps</span><span class="sxs-lookup"><span data-stu-id="da34b-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="da34b-115">プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="da34b-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da34b-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="da34b-116">Section index:</span></span>  <br/> |<span data-ttu-id="da34b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="da34b-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="da34b-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="da34b-118">Row index:</span></span>  <br/> |<span data-ttu-id="da34b-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="da34b-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="da34b-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="da34b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="da34b-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="da34b-121">**visStyleIncludesFill**</span></span> <br/> |
   

