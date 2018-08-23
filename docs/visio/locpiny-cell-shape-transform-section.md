---
title: '[LocPinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: Y を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。 [Locpiny] を決定するための既定の数式は次のとおりです。
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805789"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="51593-104">[LocPinY] セル ([図形変換] セクション)</span><span class="sxs-lookup"><span data-stu-id="51593-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="51593-105">*Y*を表す-図形の原点を基準として、図形の pin (回転の中心) の座標。</span><span class="sxs-lookup"><span data-stu-id="51593-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="51593-106">[Locpiny] を決定するための既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="51593-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="51593-107">= 高さ\*0.5</span><span class="sxs-lookup"><span data-stu-id="51593-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51593-108">注釈</span><span class="sxs-lookup"><span data-stu-id="51593-108">Remarks</span></span>

<span data-ttu-id="51593-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocPinY] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="51593-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51593-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="51593-110">Cell name:</span></span>  <br/> | <span data-ttu-id="51593-111">[Locpiny]</span><span class="sxs-lookup"><span data-stu-id="51593-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="51593-112">プログラムから、インデックスによって [LocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="51593-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51593-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="51593-113">Section index:</span></span>  <br/> |<span data-ttu-id="51593-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51593-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51593-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="51593-115">Row index:</span></span>  <br/> |<span data-ttu-id="51593-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="51593-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="51593-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="51593-117">Cell index:</span></span>  <br/> |<span data-ttu-id="51593-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="51593-118">**visXFormLocPinY**</span></span> <br/> |
   

