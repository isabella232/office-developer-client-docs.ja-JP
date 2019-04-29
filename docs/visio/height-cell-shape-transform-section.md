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
ms.openlocfilehash: 1f08fec0ec09e4ba77296495defc91b0f1f3a4c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422867"
---
# <a name="height-cell-shape-transform-section"></a><span data-ttu-id="62b58-103">[Height] セル ([Shape Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="62b58-103">Height Cell (Shape Transform Section)</span></span>

<span data-ttu-id="62b58-104">図形の高さを図面単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="62b58-104">Determines the height of the shape in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62b58-105">注釈</span><span class="sxs-lookup"><span data-stu-id="62b58-105">Remarks</span></span>

<span data-ttu-id="62b58-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Height] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="62b58-106">To get a reference to the Height cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62b58-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="62b58-107">Cell name:</span></span>  <br/> | <span data-ttu-id="62b58-108">Height</span><span class="sxs-lookup"><span data-stu-id="62b58-108">Height</span></span>  <br/> |
   
<span data-ttu-id="62b58-109">プログラムから、インデックスによって [Height] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="62b58-109">To get a reference to the Height cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62b58-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="62b58-110">Section index:</span></span>  <br/> |<span data-ttu-id="62b58-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62b58-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62b58-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="62b58-112">Row index:</span></span>  <br/> |<span data-ttu-id="62b58-113">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="62b58-113">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="62b58-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="62b58-114">Cell index:</span></span>  <br/> |<span data-ttu-id="62b58-115">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="62b58-115">**visXFormHeight**</span></span> <br/> |
   

