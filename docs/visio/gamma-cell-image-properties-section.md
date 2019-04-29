---
title: '[Gamma] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409014"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="d819c-104">[Gamma] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="d819c-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="d819c-p102">モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。</span><span class="sxs-lookup"><span data-stu-id="d819c-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d819c-107">注釈</span><span class="sxs-lookup"><span data-stu-id="d819c-107">Remarks</span></span>

<span data-ttu-id="d819c-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Gamma] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d819c-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d819c-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="d819c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d819c-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="d819c-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="d819c-111">プログラムから、インデックスによって [Gamma] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d819c-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d819c-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d819c-112">Section index:</span></span>  <br/> |<span data-ttu-id="d819c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d819c-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d819c-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d819c-114">Row index:</span></span>  <br/> |<span data-ttu-id="d819c-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="d819c-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="d819c-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d819c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d819c-117">**viシム agegamma**</span><span class="sxs-lookup"><span data-stu-id="d819c-117">**visImageGamma**</span></span> <br/> |
   

