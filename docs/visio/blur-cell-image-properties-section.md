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
description: ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。
ms.openlocfilehash: 14a50f2015b2b24d7e41f5d11018a749d089fc37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804916"
---
# <a name="blur-cell-image-properties-section"></a><span data-ttu-id="9f54a-104">[Blur] セル ([Image Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="9f54a-104">Blur Cell (Image Properties Section)</span></span>

<span data-ttu-id="9f54a-p102">ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。</span><span class="sxs-lookup"><span data-stu-id="9f54a-p102">Blurs or softens a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f54a-107">備考</span><span class="sxs-lookup"><span data-stu-id="9f54a-107">Remarks</span></span>

<span data-ttu-id="9f54a-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [Blur] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9f54a-108">To get a reference to the Blur cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f54a-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="9f54a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9f54a-110">Blur</span><span class="sxs-lookup"><span data-stu-id="9f54a-110">Blur</span></span>  <br/> |
   
<span data-ttu-id="9f54a-111">プログラムから、インデックスによって [Blur] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9f54a-111">To get a reference to the Blur cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f54a-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f54a-112">Section index:</span></span>  <br/> |<span data-ttu-id="9f54a-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9f54a-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9f54a-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f54a-114">Row index:</span></span>  <br/> |<span data-ttu-id="9f54a-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="9f54a-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="9f54a-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9f54a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9f54a-117">**visImageBlur**</span><span class="sxs-lookup"><span data-stu-id="9f54a-117">**visImageBlur**</span></span> <br/> |
   

