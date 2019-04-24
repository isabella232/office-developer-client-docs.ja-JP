---
title: '[TxtPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 図形の原点を基準にして、回転の中心となるテキストブロックの y 座標を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316423"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="e6b14-104">[TxtPinY] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="e6b14-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="e6b14-105">図形の原点を基準にして、回転の中心となるテキストブロックの*y*座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6b14-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="e6b14-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e6b14-106">The default formula is:</span></span> 
  
<span data-ttu-id="e6b14-107">= 高さ\* 0.5</span><span class="sxs-lookup"><span data-stu-id="e6b14-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6b14-108">解説</span><span class="sxs-lookup"><span data-stu-id="e6b14-108">Remarks</span></span>

<span data-ttu-id="e6b14-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e6b14-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6b14-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="e6b14-110">Cell name:</span></span>  <br/> | <span data-ttu-id="e6b14-111">[txtpiny]</span><span class="sxs-lookup"><span data-stu-id="e6b14-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="e6b14-112">プログラムから、インデックスによって [TxtPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6b14-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6b14-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6b14-113">Section index:</span></span>  <br/> |<span data-ttu-id="e6b14-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6b14-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e6b14-115">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="e6b14-115">Row index:</span></span>  <br/> |<span data-ttu-id="e6b14-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="e6b14-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="e6b14-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e6b14-117">Cell index:</span></span>  <br/> |<span data-ttu-id="e6b14-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="e6b14-118">**visXFormPinY**</span></span> <br/> |
   

