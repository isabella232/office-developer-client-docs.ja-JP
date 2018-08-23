---
title: '[UIFormat] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドの書式を指定します。
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806740"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="9c15a-103">[UIFormat] セル ([テキスト フィールド] セクション)</span><span class="sxs-lookup"><span data-stu-id="9c15a-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="9c15a-104">Visio 2000 よりも前のバージョンの Visio に挿入するフィールドの書式を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c15a-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c15a-105">備考</span><span class="sxs-lookup"><span data-stu-id="9c15a-105">Remarks</span></span>

<span data-ttu-id="9c15a-p101">このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="9c15a-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="9c15a-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UIFormat] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c15a-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c15a-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="9c15a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9c15a-110">Fields.UIFmt [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="9c15a-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9c15a-111">プログラムから、インデックスによって [UIFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9c15a-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9c15a-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c15a-112">Section index:</span></span>  <br/> |<span data-ttu-id="9c15a-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="9c15a-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="9c15a-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c15a-114">Row index:</span></span>  <br/> |<span data-ttu-id="9c15a-115">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="9c15a-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9c15a-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9c15a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9c15a-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="9c15a-117">**visFieldUIFormat**</span></span> <br/> |
   

