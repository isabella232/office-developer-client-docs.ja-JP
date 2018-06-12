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
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805920"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="7fb39-103">[NoLiveDynamics] セル ([Miscellaneous] セクション)</span><span class="sxs-lookup"><span data-stu-id="7fb39-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="7fb39-104">図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7fb39-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="7fb39-105">**値**</span><span class="sxs-lookup"><span data-stu-id="7fb39-105">**Value**</span></span>|<span data-ttu-id="7fb39-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="7fb39-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7fb39-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7fb39-107">TRUE</span></span>  <br/> | <span data-ttu-id="7fb39-108">操作中に図形は動的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="7fb39-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="7fb39-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7fb39-109">FALSE</span></span>  <br/> | <span data-ttu-id="7fb39-110">操作中に図形は動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7fb39-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fb39-111">備考</span><span class="sxs-lookup"><span data-stu-id="7fb39-111">Remarks</span></span>

<span data-ttu-id="7fb39-p101">ライブ ダイナミクスを無効にして、2 次元 (2-D) 図形をサイズ変更または回転すると、選択ボックスが表示されます。図形が 1 次元 (1-D) の場合は、ビジュアル フィードバックは [DynFeedback] セルの値に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="7fb39-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="7fb39-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NoLiveDynamics] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7fb39-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7fb39-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7fb39-115">Cell name:</span></span>  <br/> | <span data-ttu-id="7fb39-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="7fb39-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="7fb39-117">プログラムから、インデックスによって [NoLiveDynamics] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7fb39-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7fb39-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7fb39-118">Section index:</span></span>  <br/> |<span data-ttu-id="7fb39-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7fb39-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7fb39-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7fb39-120">Row index:</span></span>  <br/> |<span data-ttu-id="7fb39-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="7fb39-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="7fb39-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7fb39-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7fb39-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="7fb39-123">**visNoLiveDynamics**</span></span> <br/> |
   

