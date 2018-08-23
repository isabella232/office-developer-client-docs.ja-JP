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
description: X を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806834"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="aec44-103">[X Dynamics] セル ([コントロール] セクション)</span><span class="sxs-lookup"><span data-stu-id="aec44-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="aec44-104">*X*を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="aec44-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aec44-105">備考</span><span class="sxs-lookup"><span data-stu-id="aec44-105">Remarks</span></span>

<span data-ttu-id="aec44-106">アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="aec44-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="aec44-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X Dynamics] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="aec44-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec44-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="aec44-108">Cell name:</span></span>  <br/> | <span data-ttu-id="aec44-109">制御します。</span><span class="sxs-lookup"><span data-stu-id="aec44-109">Controls.</span></span>  <span data-ttu-id="aec44-110">*名*です。XDynwhere を制御します。</span><span class="sxs-lookup"><span data-stu-id="aec44-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="aec44-111">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="aec44-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="aec44-112">プログラムから、インデックスによって [X Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="aec44-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aec44-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="aec44-113">Section index:</span></span>  <br/> |<span data-ttu-id="aec44-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="aec44-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="aec44-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="aec44-115">Row index:</span></span>  <br/> |<span data-ttu-id="aec44-116">**visRowControl** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="aec44-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="aec44-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="aec44-117">Cell index:</span></span>  <br/> |<span data-ttu-id="aec44-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="aec44-118">**visCtlXDyn**</span></span> <br/> |
   

