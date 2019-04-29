---
title: '[NoLiveDynamics] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: 図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421481"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="202b3-103">[NoLiveDynamics] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="202b3-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="202b3-104">図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="202b3-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="202b3-105">**値**</span><span class="sxs-lookup"><span data-stu-id="202b3-105">**Value**</span></span>|<span data-ttu-id="202b3-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="202b3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="202b3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="202b3-107">TRUE</span></span>  <br/> | <span data-ttu-id="202b3-108">操作中に図形は動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="202b3-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="202b3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="202b3-109">FALSE</span></span>  <br/> | <span data-ttu-id="202b3-110">操作中に図形は動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="202b3-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="202b3-111">注釈</span><span class="sxs-lookup"><span data-stu-id="202b3-111">Remarks</span></span>

<span data-ttu-id="202b3-p101">ライブ ダイナミクスを無効にして、2 次元 (2-D) 図形をサイズ変更または回転すると、選択ボックスが表示されます。図形が 1 次元 (1-D) の場合は、ビジュアル フィードバックは [DynFeedback] セルの値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="202b3-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="202b3-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoLiveDynamics] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="202b3-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="202b3-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="202b3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="202b3-116">[nolivedynamics]</span><span class="sxs-lookup"><span data-stu-id="202b3-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="202b3-117">プログラムから、インデックスによって [NoLiveDynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="202b3-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="202b3-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="202b3-118">Section index:</span></span>  <br/> |<span data-ttu-id="202b3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="202b3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="202b3-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="202b3-120">Row index:</span></span>  <br/> |<span data-ttu-id="202b3-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="202b3-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="202b3-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="202b3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="202b3-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="202b3-123">**visNoLiveDynamics**</span></span> <br/> |
   

