---
title: '[Blur] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: ビットマップ イメージをぼかしたり、色をやわらげたりします。 既定値は 0% です。
ms.openlocfilehash: 599810d126c853e37552045d0ef83cb580606ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427907"
---
# <a name="blur-cell-image-properties-section"></a><span data-ttu-id="1450e-104">[Blur] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="1450e-104">Blur Cell (Image Properties Section)</span></span>

<span data-ttu-id="1450e-105">ビットマップ イメージをぼかしたり、色をやわらげたりします。</span><span class="sxs-lookup"><span data-stu-id="1450e-105">Blurs or softens a bitmap image.</span></span> <span data-ttu-id="1450e-106">既定値は 0% です。</span><span class="sxs-lookup"><span data-stu-id="1450e-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1450e-107">注釈</span><span class="sxs-lookup"><span data-stu-id="1450e-107">Remarks</span></span>

<span data-ttu-id="1450e-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Blur] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1450e-108">To get a reference to the Blur cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1450e-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="1450e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1450e-110">Blur</span><span class="sxs-lookup"><span data-stu-id="1450e-110">Blur</span></span>  <br/> |
   
<span data-ttu-id="1450e-111">プログラムから、インデックスによって [Blur] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1450e-111">To get a reference to the Blur cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1450e-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1450e-112">Section index:</span></span>  <br/> |<span data-ttu-id="1450e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1450e-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1450e-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1450e-114">Row index:</span></span>  <br/> |<span data-ttu-id="1450e-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="1450e-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="1450e-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1450e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1450e-117">**viシム ageブラー**</span><span class="sxs-lookup"><span data-stu-id="1450e-117">**visImageBlur**</span></span> <br/> |
   

