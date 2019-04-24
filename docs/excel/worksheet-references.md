---
title: ���[�N�V�[�g�̎Q��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304026"
---
# <a name="worksheet-references"></a><span data-ttu-id="ba5bd-104">ワークシートの参照</span><span class="sxs-lookup"><span data-stu-id="ba5bd-104">Worksheet References</span></span>

 <span data-ttu-id="ba5bd-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ba5bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ba5bd-p101">A reference in Microsoft Excel is a data type that refers to a rectangular block of cells (which can be just one cell), or in some cases, a number of disjoint blocks of cells. Internally, Excel uses one reference type for cells on the current sheet, known as an internal reference. Any cell that is not on the current sheet is described by another type of reference known as an external reference. See the next section for the definition of active and current.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p101">A reference in Microsoft Excel is a data type that refers to a rectangular block of cells (which can be just one cell), or in some cases, a number of disjoint blocks of cells. Internally, Excel uses one reference type for cells on the current sheet, known as an internal reference. Any cell that is not on the current sheet is described by another type of reference known as an external reference. See the next section for the definition of active and current.</span></span>
  
## <a name="active-vs-current"></a><span data-ttu-id="ba5bd-110">作業中と現在</span><span class="sxs-lookup"><span data-stu-id="ba5bd-110">Active vs. Current</span></span>

<span data-ttu-id="ba5bd-p102">Excel での「作業中」という用語は、ユーザーが表示しているものを指しています。作業中のブックやシートは、ユーザーが現在閲覧中のブックやワークシート、または Excel から別アプリケーションにフォーカスが移った場合には、Excel で最後にフォーカスしていた際に表示していたブックやワークシートを指します。作業中のシートは、必ず作業中のブック内にあります。作業中のシート内で複数のセルが選択されている場合は、アクティブ セルとして認識されます。埋め込みオブジェクトにフォーカスされている場合は、最後に選択したセルが引き続きアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p102">In Excel, the term active refers to what the user is viewing. The active workbook and worksheet are those that the user is currently looking at, or, if Excel has lost focus to another application, was looking at when Excel last had focus. The active sheet is always in the active workbook. The one or more cells that are selected in the active sheet are known as the active cells. If an embedded object has focus, the last-selected cells are still active.</span></span> 
  
<span data-ttu-id="ba5bd-p103">「現在」という用語は、Excel が計算しているものを指します。現在のブックとワークシートは、現在再計算を行っているブックやワークシートを指します。現在のシートは、必ず現在のブック内にあります。再計算されているセルは現在のセルと呼ばれます。また、配列数式が再計算されている場合も、現在のセルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p103">The term current refers to what Excel is recalculating. The current workbook and worksheet are those that are currently being recalculated. The current sheet is always in the current workbook. The cell being recalculated is known as the current cell, or, in the case of an array formula being recalculated, the current cells.</span></span> 
  
<span data-ttu-id="ba5bd-120">覚えておくべき重要なポイントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-120">The important points to remember are as follows:</span></span>
  
- <span data-ttu-id="ba5bd-121">作業中のブックやシート、セルが、必ずしも現在のブックやシート、セルになるわけではありません (現在のものである場合もあります)。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-121">The active workbook/worksheet/cell is not generally the current one, although it can be.</span></span>
    
- <span data-ttu-id="ba5bd-122">Visual Basic for Applications (VBA) モジュールや 、DLL または XLL において、アドイン関数は、現在のシート上にある現在のセルから呼び出されます。マルチ スレッド再計算 (MTR) の場合は、それらのいずれかから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-122">An add-in function, whether in a Visual Basic for Applications (VBA) module or a DLL or XLL, is always called from the current cell on the current sheet, or one of them in the case of multithreaded recalculation (MTR).</span></span>
    
<span data-ttu-id="ba5bd-p104">ブック内のセル、セル範囲、シートについての情報を提供する多くの Excel の関数は、作業中のブック、シート、セルと、現在のブック、シート、セルとを区別します。これらの相違点は、次のセクションに記載されているとおり、セル ブロックの参照を表すために使用するデータ型にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p104">Many Excel functions that provide information about a cell, a range of cells, or a sheet in a workbook distinguish between the active workbook, sheet, or cell and the current workbook, sheet, or cell. This difference is reflected in the data types used to describe references to blocks of cells, as described in the following section.</span></span>
  
## <a name="internal-and-external-worksheet-references"></a><span data-ttu-id="ba5bd-125">内部ワークシートおよび外部ワークシートの参照</span><span class="sxs-lookup"><span data-stu-id="ba5bd-125">Internal and External Worksheet References</span></span>

<span data-ttu-id="ba5bd-p105">内部参照と外部参照の主な違いは、外部参照のデータ型には、ワークシート ID に加えて、参照先セルの記述が含まれていることです。内部参照にはシートへの参照が含まれていません。シートが現在のシートであることを暗黙的に示します。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p105">The key difference between internal and external references is that the external reference data type contains an ID for the worksheet and also a description of which cells are referred to. An internal reference contains no reference to the sheet—it is implicit that the sheet is the current sheet.</span></span> 
  
<span data-ttu-id="ba5bd-p106">Many C API functions return references or take reference arguments. Any C API function that takes reference arguments accepts either internal or external references, except the **xlSheetNm** function, which requires an external reference. Some functions only return either internal or external references. For example, the C API function [xlfCaller](xlfcaller.md) returns a reference to the calling cells, by definition, on the current sheet. The returned reference is always an internal reference, although the function can return non-reference types where the function is not called from a worksheet cell. The C API function [xlSheetId](xlsheetid.md) always returns the ID of a worksheet contained within an external reference data type.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p106">Many C API functions return references or take reference arguments. Any C API function that takes reference arguments accepts either internal or external references, except the **xlSheetNm** function, which requires an external reference. Some functions only return either internal or external references. For example, the C API function [xlfCaller](xlfcaller.md) returns a reference to the calling cells, by definition, on the current sheet. The returned reference is always an internal reference, although the function can return non-reference types where the function is not called from a worksheet cell. The C API function [xlSheetId](xlsheetid.md) always returns the ID of a worksheet contained within an external reference data type.</span></span> 
  
<span data-ttu-id="ba5bd-p107">内部参照型と外部参照型の、もう一つの主な違いは、外部参照のデータ型は同じシート上の複数の離散したセル ブロックを表すことができるという点です。内部参照では、現在のシートの 1 ブロックのみを表すことができます。離散した参照は、範囲の引数を取る任意の関数に渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ba5bd-p107">The other key difference between the internal and external reference types is that the external reference data type can describe multiple disjoint blocks of cells on the same sheet. Internal references can describe only a single block on the current sheet. Disjoint references can be passed to any function that takes a range argument.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba5bd-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba5bd-137">See also</span></span>



[<span data-ttu-id="ba5bd-138">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="ba5bd-138">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="ba5bd-139">名前と他のワークシートの数式を評価する</span><span class="sxs-lookup"><span data-stu-id="ba5bd-139">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[<span data-ttu-id="ba5bd-140">Excel ワークシートと式の評価</span><span class="sxs-lookup"><span data-stu-id="ba5bd-140">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)

