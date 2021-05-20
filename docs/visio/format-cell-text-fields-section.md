---
title: '[Format] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431520"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="b86c8-103">[Format] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="b86c8-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="b86c8-104">テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。</span><span class="sxs-lookup"><span data-stu-id="b86c8-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b86c8-105">注釈</span><span class="sxs-lookup"><span data-stu-id="b86c8-105">Remarks</span></span>

<span data-ttu-id="b86c8-p101">[Type] セルの値が 0、2、5、6、7 (文字列、数値、日付/時刻、期間、通貨を表します) の場合は、それぞれのデータの種類に適した書式形式を指定します。たとえば、"# #/4 UU" という書式形式では、「12.43 in」という数値を指定すると "12 2/4 インチ" と表示されます。書式形式の指定の詳細については、「[書式形式について](about-format-pictures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b86c8-p101">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type. For example, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="b86c8-p102">数値 ([Type] セル = 2) は寸法、スカラー、角度、日付、時刻、通貨を表現できます。入力した数値が常に日付、時刻、または通貨として評価されるようにするには、[Format] セルに、書式形式ではなく DATETIME 関数または CY 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="b86c8-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="b86c8-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Format] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b86c8-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b86c8-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="b86c8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b86c8-114">Fields.Format[  *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="b86c8-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b86c8-115">プログラムから、インデックスによって [Format] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b86c8-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b86c8-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b86c8-116">Section index:</span></span>  <br/> |<span data-ttu-id="b86c8-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b86c8-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b86c8-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b86c8-118">Row index:</span></span>  <br/> |<span data-ttu-id="b86c8-119">**visRowField**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b86c8-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b86c8-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b86c8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b86c8-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="b86c8-121">**visFieldFormat**</span></span> <br/> |
   

