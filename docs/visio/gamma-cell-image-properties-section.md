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
ms.openlocfilehash: 060cb02aa8fd33e5a6c70a2c0236f16b9552aea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805456"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="75662-104">[Gamma] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="75662-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="75662-p102">モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。</span><span class="sxs-lookup"><span data-stu-id="75662-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75662-107">備考</span><span class="sxs-lookup"><span data-stu-id="75662-107">Remarks</span></span>

<span data-ttu-id="75662-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Gamma] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="75662-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75662-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="75662-109">Cell name:</span></span>  <br/> | <span data-ttu-id="75662-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="75662-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="75662-111">プログラムから、インデックスによって [Gamma] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="75662-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75662-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="75662-112">Section index:</span></span>  <br/> |<span data-ttu-id="75662-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75662-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="75662-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="75662-114">Row index:</span></span>  <br/> |<span data-ttu-id="75662-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="75662-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="75662-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="75662-116">Cell index:</span></span>  <br/> |<span data-ttu-id="75662-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="75662-117">**visImageGamma**</span></span> <br/> |
   

