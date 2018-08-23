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
ms.openlocfilehash: 0e1eb67528b3e87bcfff5281dd1e0b2db3a0a4d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805304"
---
# <a name="enablelineprops-cell-style-properties-section"></a><span data-ttu-id="5d647-103">[EnableLineProps] セル ([スタイルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="5d647-103">EnableLineProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="5d647-104">スタイルに線のプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d647-104">Determines whether a style includes line properties.</span></span>
  
|<span data-ttu-id="5d647-105">**値**</span><span class="sxs-lookup"><span data-stu-id="5d647-105">**Value**</span></span>|<span data-ttu-id="5d647-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="5d647-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d647-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5d647-107">TRUE</span></span>  <br/> |<span data-ttu-id="5d647-108">線のプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="5d647-108">Include line properties.</span></span>  <br/> |
|<span data-ttu-id="5d647-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5d647-109">FALSE</span></span>  <br/> |<span data-ttu-id="5d647-110">線のプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="5d647-110">Exclude line properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d647-111">注釈</span><span class="sxs-lookup"><span data-stu-id="5d647-111">Remarks</span></span>

<span data-ttu-id="5d647-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableLineProps] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5d647-112">To get a reference to the EnableLineProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d647-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="5d647-113">Cell name:</span></span>  <br/> |<span data-ttu-id="5d647-114">EnableLineProps</span><span class="sxs-lookup"><span data-stu-id="5d647-114">EnableLineProps</span></span>  <br/> |
   
<span data-ttu-id="5d647-115">プログラムから、インデックスによって [EnableLineProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5d647-115">To get a reference to the EnableLineProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d647-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5d647-116">Section index:</span></span>  <br/> |<span data-ttu-id="5d647-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d647-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5d647-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5d647-118">Row index:</span></span>  <br/> |<span data-ttu-id="5d647-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="5d647-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="5d647-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5d647-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5d647-121">**visStyleIncludesLine**</span><span class="sxs-lookup"><span data-stu-id="5d647-121">**visStyleIncludesLine**</span></span> <br/> |
   

