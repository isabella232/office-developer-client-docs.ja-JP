---
title: '[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 ReplaceLockShapeData は、マスター シェイプの図形データが置換される図形の図形データのすべてを上書きしているかどうかを決定します。
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806224"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="69575-104">[ReplaceLockShapeData] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="69575-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="69575-105">マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="69575-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="69575-106">**ReplaceLockShapeData**は、マスター シェイプの図形データが置換される図形の図形データのすべてを上書きしているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="69575-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="69575-107">**値**</span><span class="sxs-lookup"><span data-stu-id="69575-107">**Value**</span></span>|<span data-ttu-id="69575-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="69575-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69575-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="69575-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="69575-110">置換後の図形の上にすべての行と、マスター シェイプの**図形データ**セクションの値がコピーされ、古いに置き換えられた図形からすべてのローカル値が破棄されます。</span><span class="sxs-lookup"><span data-stu-id="69575-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="69575-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="69575-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="69575-112">行とマスター シェイプの**図形データ**セクションの値は、置換後の図形にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="69575-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="69575-113">置換後の図形には、ローカルの値を持つ古い図形の**図形データ**セクションの行が転送されます。</span><span class="sxs-lookup"><span data-stu-id="69575-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69575-114">備考</span><span class="sxs-lookup"><span data-stu-id="69575-114">Remarks</span></span>

<span data-ttu-id="69575-115">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockShapeData** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="69575-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69575-116">セル名:</span><span class="sxs-lookup"><span data-stu-id="69575-116">Cell name:</span></span>  <br/> | <span data-ttu-id="69575-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="69575-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="69575-118">プログラムから、インデックスによって [ **ReplaceLockShapeData** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="69575-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="69575-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="69575-119">Section index:</span></span>  <br/> |<span data-ttu-id="69575-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69575-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="69575-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="69575-121">Row index:</span></span>  <br/> |<span data-ttu-id="69575-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="69575-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="69575-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="69575-123">Cell index:</span></span>  <br/> |<span data-ttu-id="69575-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="69575-124">**visReplaceLockShapeData**</span></span> <br/> |
   

