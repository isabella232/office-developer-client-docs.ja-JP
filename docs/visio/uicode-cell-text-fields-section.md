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
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422216"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="536b2-103">[UICode] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="536b2-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="536b2-104">Visio 2000 よりも前のバージョンの Visio に挿入するフィールドのコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="536b2-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="536b2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="536b2-105">Remarks</span></span>

<span data-ttu-id="536b2-p101">このセルは [シェイプシート] ウィンドウには表示されません。Visio バージョン 2000 の図面を Visio Version 5.0 ファイル形式で保存するなど、下位互換性の問題に対処する必要がある場合に、このセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="536b2-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="536b2-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [UICode] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="536b2-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="536b2-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="536b2-109">Cell name:</span></span>  <br/> | <span data-ttu-id="536b2-110">Fields.UICod[  *i*  ]  *ここで、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="536b2-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="536b2-111">プログラムから、インデックスによって [UICode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="536b2-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="536b2-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="536b2-112">Section index:</span></span>  <br/> |<span data-ttu-id="536b2-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="536b2-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="536b2-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="536b2-114">Row index:</span></span>  <br/> |<span data-ttu-id="536b2-115">**visRowField**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="536b2-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="536b2-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="536b2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="536b2-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="536b2-117">**visFieldUICode**</span></span> <br/> |
   

