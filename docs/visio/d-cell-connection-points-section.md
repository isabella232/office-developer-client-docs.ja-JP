---
title: '[D] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: 数式を入力またはテストするために使用できる、スクラッチ セルです。
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408174"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="86bdd-103">[D] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="86bdd-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="86bdd-104">数式を入力またはテストするために使用できる、スクラッチ セルです。</span><span class="sxs-lookup"><span data-stu-id="86bdd-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86bdd-105">注釈</span><span class="sxs-lookup"><span data-stu-id="86bdd-105">Remarks</span></span>

<span data-ttu-id="86bdd-106">[D] セルにアクセスするには、行を右クリックしてから、ショートカット メニューの [**図形要素の変更**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86bdd-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="86bdd-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="86bdd-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86bdd-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="86bdd-108">Cell name:</span></span>  <br/> | <span data-ttu-id="86bdd-109">Connections.D[  *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="86bdd-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="86bdd-110">プログラムから、インデックスによって [D] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="86bdd-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86bdd-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="86bdd-111">Section index:</span></span>  <br/> |<span data-ttu-id="86bdd-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="86bdd-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="86bdd-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="86bdd-113">Row index:</span></span>  <br/> |<span data-ttu-id="86bdd-114">**visRowConnectionPts**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="86bdd-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="86bdd-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="86bdd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="86bdd-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="86bdd-116">**visCnnctD**</span></span> <br/> |
   

