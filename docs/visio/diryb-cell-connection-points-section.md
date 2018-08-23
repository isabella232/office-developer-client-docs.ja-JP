---
title: '[DirY / B] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Y を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 動的コネクタに付いている足の向きにも使用します。 このセルでは浮動小数点値です。
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805217"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="68ef6-105">[DirY / B] セル ([接続ポイント] セクション)</span><span class="sxs-lookup"><span data-stu-id="68ef6-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="68ef6-106">*Y*を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="68ef6-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="68ef6-107">動的コネクタに付いている足の向きにも使用します。</span><span class="sxs-lookup"><span data-stu-id="68ef6-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="68ef6-108">このセルでは浮動小数点値です。</span><span class="sxs-lookup"><span data-stu-id="68ef6-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="68ef6-109">注釈</span><span class="sxs-lookup"><span data-stu-id="68ef6-109">Remarks</span></span>

<span data-ttu-id="68ef6-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirY / B] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="68ef6-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68ef6-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="68ef6-111">Cell name:</span></span>  <br/> |<span data-ttu-id="68ef6-112">Connections.DirY [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="68ef6-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="68ef6-113">プログラムから、インデックスによって [DirY / B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="68ef6-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68ef6-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="68ef6-114">Section index:</span></span>  <br/> |<span data-ttu-id="68ef6-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="68ef6-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="68ef6-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="68ef6-116">Row index:</span></span>  <br/> |<span data-ttu-id="68ef6-117">**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="68ef6-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="68ef6-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="68ef6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="68ef6-119">**visCnnctDirY**(拡張されていない行)          **visCnnctB**(拡張された行)</span><span class="sxs-lookup"><span data-stu-id="68ef6-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="68ef6-120">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68ef6-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

