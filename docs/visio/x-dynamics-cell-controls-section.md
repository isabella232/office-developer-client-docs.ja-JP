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
description: コントロール ハンドルのアンカー ポイントの x 座標をローカル座標で表します。
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432129"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="f2bfa-103">[X Dynamics] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="f2bfa-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="f2bfa-104">コントロール ハンドルのアンカー ポイントの  *x*  座標をローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f2bfa-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f2bfa-105">Remarks</span></span>

<span data-ttu-id="f2bfa-106">アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="f2bfa-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Dynamics] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2bfa-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="f2bfa-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f2bfa-109">コントロール。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-109">Controls.</span></span>  <span data-ttu-id="f2bfa-110">*name*  .XDynwhere コントロール。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="f2bfa-111">*name*  は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f2bfa-112">プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2bfa-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f2bfa-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2bfa-113">Section index:</span></span>  <br/> |<span data-ttu-id="f2bfa-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f2bfa-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f2bfa-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2bfa-115">Row index:</span></span>  <br/> |<span data-ttu-id="f2bfa-116">**visRowControl**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2bfa-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f2bfa-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f2bfa-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f2bfa-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="f2bfa-118">**visCtlXDyn**</span></span> <br/> |
   

