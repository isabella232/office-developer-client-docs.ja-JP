---
title: '[LockCustProp] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: '[図形データの定義] ダイアログ ボックス、または [図形データ] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。'
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359607"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="bcd3d-103">[LockCustProp] セル ([Protection] セクション)</span><span class="sxs-lookup"><span data-stu-id="bcd3d-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="bcd3d-104">[**図形データの定義**] ダイアログ ボックス、または [**図形データ**] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="bcd3d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="bcd3d-105">**Value**</span></span>|<span data-ttu-id="bcd3d-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="bcd3d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bcd3d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bcd3d-107">TRUE</span></span>  <br/> |<span data-ttu-id="bcd3d-108">[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**] コマンドが無効になります。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="bcd3d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bcd3d-109">FALSE</span></span>  <br/> |<span data-ttu-id="bcd3d-110">[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**] コマンドが有効になります (既定値)。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcd3d-111">解説</span><span class="sxs-lookup"><span data-stu-id="bcd3d-111">Remarks</span></span>

<span data-ttu-id="bcd3d-112">この値が TRUE の場合でも、図形データ項目の値は変更できます。また、[シェイプシート] ウィンドウの [図形データ] セクションも変更できます。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="bcd3d-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCustProp] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcd3d-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="bcd3d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="bcd3d-115">[lockcustprop]</span><span class="sxs-lookup"><span data-stu-id="bcd3d-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="bcd3d-116">プログラムから、インデックスによって [LockCustProp] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcd3d-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcd3d-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcd3d-117">Section index:</span></span>  <br/> |<span data-ttu-id="bcd3d-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bcd3d-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bcd3d-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcd3d-119">Row index:</span></span>  <br/> |<span data-ttu-id="bcd3d-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bcd3d-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="bcd3d-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bcd3d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="bcd3d-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="bcd3d-122">**visLockCustProp**</span></span> <br/> |
   

