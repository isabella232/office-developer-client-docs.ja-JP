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
description: 一致する接続ポイントに必要な配置ベクトルの y コンポーネントを指定します。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417092"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="06359-105">[DirY / B] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="06359-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="06359-106">一致する接続ポイントに必要な配置ベクトルの*y*コンポーネントを指定します。</span><span class="sxs-lookup"><span data-stu-id="06359-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="06359-107">動的コネクタに付いている脚の向きを揃える場合にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="06359-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="06359-108">このセルでは浮動小数点値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="06359-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="06359-109">注釈</span><span class="sxs-lookup"><span data-stu-id="06359-109">Remarks</span></span>

<span data-ttu-id="06359-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirY / B] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="06359-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06359-111">セル名 :</span><span class="sxs-lookup"><span data-stu-id="06359-111">Cell name:</span></span>  <br/> |<span data-ttu-id="06359-112">[diry [ *i* ] = <1>、 \*\* 2、3...</span><span class="sxs-lookup"><span data-stu-id="06359-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="06359-113">プログラムから、インデックスによって [DirY / B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="06359-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06359-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="06359-114">Section index:</span></span>  <br/> |<span data-ttu-id="06359-115">**持つ vissectionconnectionpts**</span><span class="sxs-lookup"><span data-stu-id="06359-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="06359-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="06359-116">Row index:</span></span>  <br/> |<span data-ttu-id="06359-117">**visRowConnectionPts** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="06359-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="06359-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="06359-118">Cell index:</span></span>  <br/> |<span data-ttu-id="06359-119">**visCnnctDirY**(非拡張行)          **viscnnctb**(拡張行)</span><span class="sxs-lookup"><span data-stu-id="06359-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="06359-120">拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06359-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

