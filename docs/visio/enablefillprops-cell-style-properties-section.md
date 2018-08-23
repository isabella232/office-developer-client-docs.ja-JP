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
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="80220-103">[EnableFillProps] セル ([スタイルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="80220-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="80220-104">スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="80220-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="80220-105">**値**</span><span class="sxs-lookup"><span data-stu-id="80220-105">**Value**</span></span>|<span data-ttu-id="80220-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="80220-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80220-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="80220-107">TRUE</span></span>  <br/> |<span data-ttu-id="80220-108">塗りつぶしのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="80220-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="80220-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="80220-109">FALSE</span></span>  <br/> |<span data-ttu-id="80220-110">塗りつぶしのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="80220-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80220-111">注釈</span><span class="sxs-lookup"><span data-stu-id="80220-111">Remarks</span></span>

<span data-ttu-id="80220-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableFillProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="80220-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80220-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="80220-113">Cell name:</span></span>  <br/> |<span data-ttu-id="80220-114">EnableFillProps</span><span class="sxs-lookup"><span data-stu-id="80220-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="80220-115">プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="80220-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80220-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="80220-116">Section index:</span></span>  <br/> |<span data-ttu-id="80220-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="80220-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="80220-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="80220-118">Row index:</span></span>  <br/> |<span data-ttu-id="80220-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="80220-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="80220-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="80220-120">Cell index:</span></span>  <br/> |<span data-ttu-id="80220-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="80220-121">**visStyleIncludesFill**</span></span> <br/> |
   

