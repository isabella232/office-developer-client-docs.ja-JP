---
title: '[DontMoveChildren] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805257"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="db23a-103">[DontMoveChildren] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="db23a-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="db23a-104">グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="db23a-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="db23a-105">**値**</span><span class="sxs-lookup"><span data-stu-id="db23a-105">**Value**</span></span>|<span data-ttu-id="db23a-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="db23a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="db23a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="db23a-107">TRUE</span></span>  <br/> | <span data-ttu-id="db23a-108">グループ内の図形をマウスを使用してドラッグできません。</span><span class="sxs-lookup"><span data-stu-id="db23a-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="db23a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="db23a-109">FALSE</span></span>  <br/> | <span data-ttu-id="db23a-110">グループ内の図形をマウスを使用してドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="db23a-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db23a-111">備考</span><span class="sxs-lookup"><span data-stu-id="db23a-111">Remarks</span></span>

<span data-ttu-id="db23a-112">このセルの値が TRUE の場合でも、別の方法を使用してグループ内の図形を反転、回転、サイズ変更、位置変更することはできます。</span><span class="sxs-lookup"><span data-stu-id="db23a-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="db23a-113">Visio 2000 より前のバージョンの Visio で作成されたマスター シェイプのグループまたはマスター シェイプのインスタンスのグループの場合、このセルの値は TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="db23a-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="db23a-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DontMoveChildren] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="db23a-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db23a-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="db23a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="db23a-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="db23a-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="db23a-117">プログラムから、インデックスによって [DontMoveChildren] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="db23a-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db23a-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="db23a-118">Section index:</span></span>  <br/> |<span data-ttu-id="db23a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db23a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db23a-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="db23a-120">Row index:</span></span>  <br/> |<span data-ttu-id="db23a-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="db23a-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="db23a-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="db23a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="db23a-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="db23a-123">**visGroupDontMoveChildren**</span></span> <br/> |
   
