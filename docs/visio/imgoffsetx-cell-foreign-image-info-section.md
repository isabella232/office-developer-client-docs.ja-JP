---
title: '[ImgOffsetX] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251308
localization_priority: Normal
ms.assetid: c079fb10-4db7-4657-75d2-2fb953c86670
description: オブジェクトの距離は、オブジェクトの枠の原点から水平方向にオフセットを決定します。 既定値は 0 です。 トリミング ツールの変更をオブジェクトにこの値をパンします。
ms.openlocfilehash: dda385b2157e48baec2b21c6da741b31d05c3291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805573"
---
# <a name="imgoffsetx-cell-foreign-image-info-section"></a><span data-ttu-id="9aaf9-105">[ImgOffsetX] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="9aaf9-105">ImgOffsetX Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="9aaf9-106">オブジェクトの距離は、オブジェクトの枠の原点から水平方向にオフセットを決定します。</span><span class="sxs-lookup"><span data-stu-id="9aaf9-106">Determines the distance the object is offset horizontally from the origin of the object's border.</span></span> <span data-ttu-id="9aaf9-107">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="9aaf9-107">The default is 0.</span></span> <span data-ttu-id="9aaf9-108">**トリミング**ツールの変更をオブジェクトにこの値をパンします。</span><span class="sxs-lookup"><span data-stu-id="9aaf9-108">Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9aaf9-109">備考</span><span class="sxs-lookup"><span data-stu-id="9aaf9-109">Remarks</span></span>

<span data-ttu-id="9aaf9-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ImgOffsetX] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="9aaf9-110">To get a reference to the ImgOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9aaf9-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="9aaf9-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9aaf9-112">ImgOffsetX</span><span class="sxs-lookup"><span data-stu-id="9aaf9-112">ImgOffsetX</span></span>  <br/> |
   
<span data-ttu-id="9aaf9-113">プログラムから、インデックスによって [ImgOffsetX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9aaf9-113">To get a reference to the ImgOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9aaf9-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9aaf9-114">Section index:</span></span>  <br/> |<span data-ttu-id="9aaf9-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9aaf9-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9aaf9-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9aaf9-116">Row index:</span></span>  <br/> |<span data-ttu-id="9aaf9-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="9aaf9-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="9aaf9-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9aaf9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9aaf9-119">**visFrgnImgOffsetX**</span><span class="sxs-lookup"><span data-stu-id="9aaf9-119">**visFrgnImgOffsetX**</span></span> <br/> |
   

