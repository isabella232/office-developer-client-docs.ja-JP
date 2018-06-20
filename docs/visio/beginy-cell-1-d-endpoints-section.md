---
title: '[BeginY] セル ([1-D Endpoints] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm95
localization_priority: Normal
ms.assetid: b2518a70-5755-a15a-a238-bac2ae64a75a
description: Y を表しますが、親の原点を基準として、1 次元図形の始点の座標です。
ms.openlocfilehash: aa45b7bf366a4e8091546963968d8930f21100e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804801"
---
# <a name="beginy-cell-1-d-endpoints-section"></a><span data-ttu-id="ff72c-103">[BeginY] セル ([1-D Endpoints] セクション)</span><span class="sxs-lookup"><span data-stu-id="ff72c-103">BeginY Cell (1-D Endpoints Section)</span></span>

<span data-ttu-id="ff72c-104">*Y*を表すが、親の原点を基準として、1 次元図形の始点の座標です。</span><span class="sxs-lookup"><span data-stu-id="ff72c-104">Represents the  *y*  -coordinate of the begin point of the 1-D shape, in relation to the origin of its parent.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff72c-105">備考</span><span class="sxs-lookup"><span data-stu-id="ff72c-105">Remarks</span></span>

<span data-ttu-id="ff72c-106">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [beginy] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ff72c-106">To get a reference to the BeginY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff72c-107">セル名 :</span><span class="sxs-lookup"><span data-stu-id="ff72c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="ff72c-108">[Beginy]</span><span class="sxs-lookup"><span data-stu-id="ff72c-108">BeginY</span></span>  <br/> |
   
<span data-ttu-id="ff72c-109">プログラムから、インデックスによって [beginy] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ff72c-109">To get a reference to the BeginY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff72c-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff72c-110">Section index:</span></span>  <br/> |<span data-ttu-id="ff72c-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ff72c-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ff72c-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff72c-112">Row index:</span></span>  <br/> |<span data-ttu-id="ff72c-113">**visRowXForm1D**</span><span class="sxs-lookup"><span data-stu-id="ff72c-113">**visRowXForm1D**</span></span> <br/> |
| <span data-ttu-id="ff72c-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ff72c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="ff72c-115">**vis1DBeginY**</span><span class="sxs-lookup"><span data-stu-id="ff72c-115">**vis1DBeginY**</span></span> <br/> |
   

