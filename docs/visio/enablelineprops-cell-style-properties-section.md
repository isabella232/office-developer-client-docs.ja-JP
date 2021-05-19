---
title: '[EnableLineProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: スタイルに線のプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410001"
---
# <a name="enablelineprops-cell-style-properties-section"></a><span data-ttu-id="d2366-103">[EnableLineProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="d2366-103">EnableLineProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="d2366-104">スタイルに線のプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d2366-104">Determines whether a style includes line properties.</span></span>
  
|<span data-ttu-id="d2366-105">**値**</span><span class="sxs-lookup"><span data-stu-id="d2366-105">**Value**</span></span>|<span data-ttu-id="d2366-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="d2366-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2366-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d2366-107">TRUE</span></span>  <br/> |<span data-ttu-id="d2366-108">線のプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="d2366-108">Include line properties.</span></span>  <br/> |
|<span data-ttu-id="d2366-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d2366-109">FALSE</span></span>  <br/> |<span data-ttu-id="d2366-110">線のプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="d2366-110">Exclude line properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2366-111">注釈</span><span class="sxs-lookup"><span data-stu-id="d2366-111">Remarks</span></span>

<span data-ttu-id="d2366-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableLineProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2366-112">To get a reference to the EnableLineProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2366-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="d2366-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d2366-114">EnableLineProps</span><span class="sxs-lookup"><span data-stu-id="d2366-114">EnableLineProps</span></span>  <br/> |
   
<span data-ttu-id="d2366-115">プログラムから、インデックスによって [EnableLineProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d2366-115">To get a reference to the EnableLineProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2366-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2366-116">Section index:</span></span>  <br/> |<span data-ttu-id="d2366-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2366-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d2366-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2366-118">Row index:</span></span>  <br/> |<span data-ttu-id="d2366-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="d2366-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="d2366-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d2366-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d2366-121">**visStyleIncludesLine**</span><span class="sxs-lookup"><span data-stu-id="d2366-121">**visStyleIncludesLine**</span></span> <br/> |
   

