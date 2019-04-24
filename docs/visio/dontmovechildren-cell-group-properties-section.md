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
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338585"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="3f2a4-103">[DontMoveChildren] セル ([Group Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="3f2a4-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="3f2a4-104">グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="3f2a4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-105">**Value**</span></span>|<span data-ttu-id="3f2a4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3f2a4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3f2a4-107">TRUE</span></span>  <br/> | <span data-ttu-id="3f2a4-108">グループ内の図形をマウスを使用してドラッグできません。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="3f2a4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3f2a4-109">FALSE</span></span>  <br/> | <span data-ttu-id="3f2a4-110">グループ内の図形をマウスを使用してドラッグできます。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f2a4-111">解説</span><span class="sxs-lookup"><span data-stu-id="3f2a4-111">Remarks</span></span>

<span data-ttu-id="3f2a4-112">このセルの値が TRUE の場合でも、別の方法を使用してグループ内の図形を反転、回転、サイズ変更、位置変更することはできます。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="3f2a4-113">Visio 2000 より前のバージョンの Visio で作成されたマスター シェイプのグループまたはマスター シェイプのインスタンスのグループの場合、このセルの値は TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="3f2a4-114">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DontMoveChildren] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f2a4-115">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3f2a4-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3f2a4-116">[dontmovechildren]</span><span class="sxs-lookup"><span data-stu-id="3f2a4-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="3f2a4-117">プログラムから、インデックスによって [DontMoveChildren] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f2a4-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f2a4-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f2a4-118">Section index:</span></span>  <br/> |<span data-ttu-id="3f2a4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f2a4-120">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="3f2a4-120">Row index:</span></span>  <br/> |<span data-ttu-id="3f2a4-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="3f2a4-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f2a4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3f2a4-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

