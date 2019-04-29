---
title: '[UICategory] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのカテゴリを指定します。
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434026"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="c1b6c-103">[UICategory] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="c1b6c-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="c1b6c-104">Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのカテゴリを指定します。</span><span class="sxs-lookup"><span data-stu-id="c1b6c-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1b6c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="c1b6c-105">Remarks</span></span>

<span data-ttu-id="c1b6c-p101">このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1b6c-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="c1b6c-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UICategory] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1b6c-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1b6c-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c1b6c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c1b6c-110">UICat [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="c1b6c-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c1b6c-111">プログラムから、インデックスによって [UICategory] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c1b6c-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1b6c-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c1b6c-112">Section index:</span></span>  <br/> |<span data-ttu-id="c1b6c-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="c1b6c-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="c1b6c-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c1b6c-114">Row index:</span></span>  <br/> |<span data-ttu-id="c1b6c-115">**visRowField** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="c1b6c-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c1b6c-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c1b6c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c1b6c-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="c1b6c-117">**visFieldUICategory**</span></span> <br/> |
   

