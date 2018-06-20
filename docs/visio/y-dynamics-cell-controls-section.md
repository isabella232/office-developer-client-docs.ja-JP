---
title: '[Y Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Y を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806864"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="8cfbf-104">[Y Dynamics] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="8cfbf-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="8cfbf-105">*Y*を表す-ローカル座標でのコントロール ハンドルのアンカー ポイントの座標です。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="8cfbf-106">アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8cfbf-107">備考</span><span class="sxs-lookup"><span data-stu-id="8cfbf-107">Remarks</span></span>

<span data-ttu-id="8cfbf-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Y Dynamics] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cfbf-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="8cfbf-109">Cell name:</span></span>  <br/> | <span data-ttu-id="8cfbf-110">制御します。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-110">Controls.</span></span>  <span data-ttu-id="8cfbf-111">*名*です。YDynwhere を制御します。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="8cfbf-112">*名*は、コントロールの行の名前です。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="8cfbf-113">プログラムから、インデックスによって [Y Dynamics] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8cfbf-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cfbf-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8cfbf-114">Section index:</span></span>  <br/> |<span data-ttu-id="8cfbf-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="8cfbf-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="8cfbf-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8cfbf-116">Row index:</span></span>  <br/> |<span data-ttu-id="8cfbf-117">**visRowControl** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="8cfbf-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8cfbf-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8cfbf-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8cfbf-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="8cfbf-119">**visCtlYDyn**</span></span> <br/> |
   

