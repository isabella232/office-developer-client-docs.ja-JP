---
title: '[LockReplace] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: 図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805761"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="12818-103">[LockReplace] セル ([保護] セクション)</span><span class="sxs-lookup"><span data-stu-id="12818-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="12818-104">図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。</span><span class="sxs-lookup"><span data-stu-id="12818-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="12818-105">**値**</span><span class="sxs-lookup"><span data-stu-id="12818-105">**Value**</span></span>|<span data-ttu-id="12818-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="12818-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12818-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="12818-107">TRUE</span></span>  <br/> |<span data-ttu-id="12818-108">図形は置換できません。または、置換後の図形として使用できません。</span><span class="sxs-lookup"><span data-stu-id="12818-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="12818-109">キャンバス上の図形では、図形を選択すると [**図形の変更**] ボタンが無効化されています。</span><span class="sxs-lookup"><span data-stu-id="12818-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="12818-110">ステンシル上の図形の場合、[**図形の変更**] ボタンをクリックすると、その図形は置換後の図形として表示されません。</span><span class="sxs-lookup"><span data-stu-id="12818-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="12818-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="12818-111">FALSE</span></span>  <br/> |<span data-ttu-id="12818-112">図形は置換できます。または置換後の図形として使用できます。</span><span class="sxs-lookup"><span data-stu-id="12818-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12818-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="12818-113">Remarks</span></span>

<span data-ttu-id="12818-114">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockReplace**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="12818-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12818-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="12818-115">Cell name:</span></span>  <br/> | <span data-ttu-id="12818-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="12818-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="12818-117">プログラムから、インデックスによって [**LockReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="12818-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12818-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="12818-118">Section index:</span></span>  <br/> |<span data-ttu-id="12818-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="12818-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="12818-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="12818-120">Row index:</span></span>  <br/> |<span data-ttu-id="12818-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="12818-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="12818-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="12818-122">Cell index:</span></span>  <br/> |<span data-ttu-id="12818-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="12818-123">**visLockReplace**</span></span> <br/> |
   

