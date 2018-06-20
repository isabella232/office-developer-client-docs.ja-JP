---
title: '[UICode] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのコードを指定します。
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806717"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="0c647-103">[UICode] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="0c647-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="0c647-104">Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="0c647-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c647-105">備考</span><span class="sxs-lookup"><span data-stu-id="0c647-105">Remarks</span></span>

<span data-ttu-id="0c647-p101">このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0c647-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="0c647-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [uicode] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="0c647-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c647-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="0c647-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0c647-110">Fields.UICod [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="0c647-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0c647-111">プログラムから、インデックスによって [uicode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="0c647-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c647-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c647-112">Section index:</span></span>  <br/> |<span data-ttu-id="0c647-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0c647-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="0c647-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c647-114">Row index:</span></span>  <br/> |<span data-ttu-id="0c647-115">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="0c647-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0c647-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c647-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0c647-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="0c647-117">**visFieldUICode**</span></span> <br/> |
   

