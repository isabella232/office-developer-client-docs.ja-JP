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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406011"
---
# <a name="enablefillprops-cell-style-properties-section"></a><span data-ttu-id="dfd3c-103">[EnableFillProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="dfd3c-103">EnableFillProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="dfd3c-104">スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dfd3c-104">Determines whether a style includes fill properties.</span></span>
  
|<span data-ttu-id="dfd3c-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dfd3c-105">**Value**</span></span>|<span data-ttu-id="dfd3c-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="dfd3c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dfd3c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dfd3c-107">TRUE</span></span>  <br/> |<span data-ttu-id="dfd3c-108">塗りつぶしのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="dfd3c-108">Include fill properties.</span></span>  <br/> |
|<span data-ttu-id="dfd3c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dfd3c-109">FALSE</span></span>  <br/> |<span data-ttu-id="dfd3c-110">塗りつぶしのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="dfd3c-110">Exclude fill properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfd3c-111">注釈</span><span class="sxs-lookup"><span data-stu-id="dfd3c-111">Remarks</span></span>

<span data-ttu-id="dfd3c-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableFillProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dfd3c-112">To get a reference to the EnableFillProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfd3c-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="dfd3c-113">Cell name:</span></span>  <br/> |<span data-ttu-id="dfd3c-114">EnableFillProps</span><span class="sxs-lookup"><span data-stu-id="dfd3c-114">EnableFillProps</span></span>  <br/> |
   
<span data-ttu-id="dfd3c-115">プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfd3c-115">To get a reference to the EnableFillProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfd3c-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfd3c-116">Section index:</span></span>  <br/> |<span data-ttu-id="dfd3c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfd3c-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dfd3c-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfd3c-118">Row index:</span></span>  <br/> |<span data-ttu-id="dfd3c-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="dfd3c-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="dfd3c-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dfd3c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dfd3c-121">**visStyleIncludesFill**</span><span class="sxs-lookup"><span data-stu-id="dfd3c-121">**visStyleIncludesFill**</span></span> <br/> |
   

