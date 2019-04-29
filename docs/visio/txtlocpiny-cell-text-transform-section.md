---
title: '[TxtLocPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: テキストブロックの回転中心の y 座標を、テキストブロックの原点を基準にして指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414061"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="71c15-104">[TxtLocPinY] セル ([Text Transform] セクション)</span><span class="sxs-lookup"><span data-stu-id="71c15-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="71c15-105">テキストブロックの回転中心の*y*座標を、テキストブロックの原点を基準にして指定します。</span><span class="sxs-lookup"><span data-stu-id="71c15-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="71c15-106">既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71c15-106">The default formula is:</span></span> 
  
<span data-ttu-id="71c15-107">= [txtheight] \* 0.5</span><span class="sxs-lookup"><span data-stu-id="71c15-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71c15-108">注釈</span><span class="sxs-lookup"><span data-stu-id="71c15-108">Remarks</span></span>

<span data-ttu-id="71c15-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtLocPinY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="71c15-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71c15-110">セル名 :</span><span class="sxs-lookup"><span data-stu-id="71c15-110">Cell name:</span></span>  <br/> | <span data-ttu-id="71c15-111">[txtlocpiny]</span><span class="sxs-lookup"><span data-stu-id="71c15-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="71c15-112">プログラムから、インデックスによって [TxtLocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="71c15-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71c15-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="71c15-113">Section index:</span></span>  <br/> |<span data-ttu-id="71c15-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71c15-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="71c15-115">行インデックス :</span><span class="sxs-lookup"><span data-stu-id="71c15-115">Row index:</span></span>  <br/> |<span data-ttu-id="71c15-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="71c15-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="71c15-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="71c15-117">Cell index:</span></span>  <br/> |<span data-ttu-id="71c15-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="71c15-118">**visXFormLocPinY**</span></span> <br/> |
   

