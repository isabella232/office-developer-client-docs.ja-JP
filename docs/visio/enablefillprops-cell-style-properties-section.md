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
ms.openlocfilehash: 55191cb28d5777f7fb65a3a1e4be890e6dda4e8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345564"
---
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="138b4-103">[EnableFillProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="138b4-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="138b4-104">スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="138b4-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="138b4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="138b4-105">**Value**</span></span>|<span data-ttu-id="138b4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="138b4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="138b4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="138b4-107">TRUE</span></span>  <br/> |<span data-ttu-id="138b4-108">塗りつぶしのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="138b4-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="138b4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="138b4-109">FALSE</span></span>  <br/> |<span data-ttu-id="138b4-110">塗りつぶしのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="138b4-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="138b4-111">解説</span><span class="sxs-lookup"><span data-stu-id="138b4-111">Remarks</span></span>

<span data-ttu-id="138b4-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableFillProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="138b4-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="138b4-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="138b4-113">Cell name:</span></span>  <br/> |<span data-ttu-id="138b4-114">[enablefillprops]</span><span class="sxs-lookup"><span data-stu-id="138b4-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="138b4-115">プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="138b4-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="138b4-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="138b4-116">Section index:</span></span>  <br/> |<span data-ttu-id="138b4-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="138b4-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="138b4-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="138b4-118">Row index:</span></span>  <br/> |<span data-ttu-id="138b4-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="138b4-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="138b4-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="138b4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="138b4-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="138b4-121">**visStyleIncludesFill**</span></span> <br/> |
   

