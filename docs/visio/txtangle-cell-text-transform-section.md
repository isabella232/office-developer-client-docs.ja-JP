---
title: '[TxtAngle] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251272
localization_priority: Normal
ms.assetid: b8482cd8-5205-40ef-b4e1-4ceb197ac80f
description: 図形の x 軸に対するテキスト ブロックの現在の回転角度を決定します。 既定値は 0°です。
ms.openlocfilehash: 701a2b0ce5fccb29cc61309de1d1768a96d92c99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432171"
---
# <a name="txtangle-cell-text-transform-section"></a><span data-ttu-id="30162-104">[TxtAngle] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="30162-104">TxtAngle Cell (Text Transform Section)</span></span>

<span data-ttu-id="30162-105">図形の x 軸に対するテキスト ブロックの現在の回転角度を決定します。</span><span class="sxs-lookup"><span data-stu-id="30162-105">Determines the text block's current angle of rotation in relation to the  *x*  -axis of the shape.</span></span> <span data-ttu-id="30162-106">既定値は 0°です。</span><span class="sxs-lookup"><span data-stu-id="30162-106">The default is 0 degrees.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30162-107">注釈</span><span class="sxs-lookup"><span data-stu-id="30162-107">Remarks</span></span>

<span data-ttu-id="30162-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtAngle] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="30162-108">To get a reference to the TxtAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30162-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="30162-109">Cell name:</span></span>  <br/> | <span data-ttu-id="30162-110">TxtAngle</span><span class="sxs-lookup"><span data-stu-id="30162-110">TxtAngle</span></span>  <br/> |
   
<span data-ttu-id="30162-111">プログラムから、インデックスによって [TxtAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="30162-111">To get a reference to the TxtAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30162-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="30162-112">Section index:</span></span>  <br/> |<span data-ttu-id="30162-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30162-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30162-114">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="30162-114">Row index:</span></span>  <br/> |<span data-ttu-id="30162-115">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="30162-115">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="30162-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="30162-116">Cell index:</span></span>  <br/> |<span data-ttu-id="30162-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="30162-117">**visXFormAngle**</span></span> <br/> |
   

