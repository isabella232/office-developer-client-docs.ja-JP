---
title: '[TxtLocPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: テキストブロックの回転中心の x 座標を、テキストブロックの原点を基準にして指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316451"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="12a89-104">[TxtLocPinX] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="12a89-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="12a89-105">テキストブロックの回転中心の*x*座標を、テキストブロックの原点を基準にして指定します。</span><span class="sxs-lookup"><span data-stu-id="12a89-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="12a89-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="12a89-106">The default formula is:</span></span> 
  
<span data-ttu-id="12a89-107">= txtwidth \* 0.5</span><span class="sxs-lookup"><span data-stu-id="12a89-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="12a89-108">この数式では、テキスト ブロックの水平方向の中心が回転の中心になります。</span><span class="sxs-lookup"><span data-stu-id="12a89-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12a89-109">解説</span><span class="sxs-lookup"><span data-stu-id="12a89-109">Remarks</span></span>

<span data-ttu-id="12a89-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtLocPinX] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="12a89-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12a89-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="12a89-111">Cell name:</span></span>  <br/> | <span data-ttu-id="12a89-112">[txtlocpinx]</span><span class="sxs-lookup"><span data-stu-id="12a89-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="12a89-113">プログラムから、インデックスによって [TxtLocPinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="12a89-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12a89-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="12a89-114">Section index:</span></span>  <br/> |<span data-ttu-id="12a89-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="12a89-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="12a89-116">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="12a89-116">Row index:</span></span>  <br/> |<span data-ttu-id="12a89-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="12a89-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="12a89-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="12a89-118">Cell index:</span></span>  <br/> |<span data-ttu-id="12a89-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="12a89-119">**visXFormLocPinX**</span></span> <br/> |
   

