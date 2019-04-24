---
title: '[X Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: コントロールハンドルのアンカーポイントの x 座標を、ローカル座標で表します。
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322303"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="3db9b-103">[X Dynamics] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="3db9b-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="3db9b-104">コントロールハンドルのアンカーポイントの*x*座標を、ローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="3db9b-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3db9b-105">解説</span><span class="sxs-lookup"><span data-stu-id="3db9b-105">Remarks</span></span>

<span data-ttu-id="3db9b-106">アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="3db9b-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="3db9b-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Dynamics] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3db9b-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3db9b-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="3db9b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3db9b-109">管理.</span><span class="sxs-lookup"><span data-stu-id="3db9b-109">Controls.</span></span>  <span data-ttu-id="3db9b-110">*名前*です。XDynwhere コントロール</span><span class="sxs-lookup"><span data-stu-id="3db9b-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="3db9b-111">*name*は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="3db9b-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="3db9b-112">プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3db9b-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3db9b-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db9b-113">Section index:</span></span>  <br/> |<span data-ttu-id="3db9b-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="3db9b-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="3db9b-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db9b-115">Row index:</span></span>  <br/> |<span data-ttu-id="3db9b-116">**visRowControl** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="3db9b-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3db9b-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3db9b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3db9b-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="3db9b-118">**visCtlXDyn**</span></span> <br/> |
   

