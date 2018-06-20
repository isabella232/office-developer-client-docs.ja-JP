---
title: '[Height] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251195
localization_priority: Normal
ms.assetid: 194d5beb-c705-f567-84de-8305c41081a8
description: 図形の高さを図面単位で指定します。
ms.openlocfilehash: c9f6282e9a2be161a4338043925d88cee672d5ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805526"
---
# <a name="height-cell-shape-transform-section"></a><span data-ttu-id="a180b-103">[Height] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="a180b-103">Height Cell (Shape Transform Section)</span></span>

<span data-ttu-id="a180b-104">図形の高さを図面単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="a180b-104">Determines the height of the shape in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a180b-105">備考</span><span class="sxs-lookup"><span data-stu-id="a180b-105">Remarks</span></span>

<span data-ttu-id="a180b-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Height] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a180b-106">To get a reference to the Height cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a180b-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a180b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a180b-108">Height</span><span class="sxs-lookup"><span data-stu-id="a180b-108">Height</span></span>  <br/> |
   
<span data-ttu-id="a180b-109">プログラムから、インデックスによって [Height] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a180b-109">To get a reference to the Height cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a180b-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a180b-110">Section index:</span></span>  <br/> |<span data-ttu-id="a180b-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a180b-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a180b-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a180b-112">Row index:</span></span>  <br/> |<span data-ttu-id="a180b-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="a180b-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="a180b-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a180b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a180b-115">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="a180b-115">**visXFormHeight**</span></span> <br/> |
   

