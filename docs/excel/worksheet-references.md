---
title: ワークシートの参照
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798966"
---
# <a name="worksheet-references"></a><span data-ttu-id="fb303-104">ワークシートの参照</span><span class="sxs-lookup"><span data-stu-id="fb303-104">Worksheet References</span></span>

 <span data-ttu-id="fb303-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb303-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fb303-106">Microsoft Excel における参照とは、長方形のセル ブロック (1 セルのみの場合もある) を参照するデータ型を指します。または、複数の離散したセル ブロックを参照する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="fb303-106">A reference in Microsoft Excel is a data type that refers to a rectangular block of cells (which can be just one cell), or in some cases, a number of disjoint blocks of cells.</span></span> <span data-ttu-id="fb303-107">Excel 内部では、現在のシート上のセルに 1 つの参照型を使用します。これは内部参照として知られています。</span><span class="sxs-lookup"><span data-stu-id="fb303-107">Internally, Excel uses one reference type for cells on the current sheet, known as an internal reference.</span></span> <span data-ttu-id="fb303-108">現在のシートに含まれていないあらゆるセルは、外部参照とも呼ばれる、もう 1 つの参照型で表します。</span><span class="sxs-lookup"><span data-stu-id="fb303-108">Any cell that is not on the current sheet is described by another type of reference known as an external reference.</span></span> <span data-ttu-id="fb303-109">「作業中」と「現在」の定義については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb303-109">See the next section for the definition of active and current.</span></span>
  
## <a name="active-vs-current"></a><span data-ttu-id="fb303-110">作業中と現在</span><span class="sxs-lookup"><span data-stu-id="fb303-110">Active vs. Current</span></span>

<span data-ttu-id="fb303-p102">Excel での「作業中」という用語は、ユーザーが表示しているものを指しています。作業中のブックやシートは、ユーザーが現在閲覧中のブックやワークシート、または Excel から別アプリケーションにフォーカスが移った場合には、Excel で最後にフォーカスしていた際に表示していたブックやワークシートを指します。作業中のシートは、必ず作業中のブック内にあります。作業中のシート内で複数のセルが選択されている場合は、アクティブ セルとして認識されます。埋め込みオブジェクトにフォーカスされている場合は、最後に選択したセルが引き続きアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="fb303-p102">In Excel, the term active refers to what the user is viewing. The active workbook and worksheet are those that the user is currently looking at, or, if Excel has lost focus to another application, was looking at when Excel last had focus. The active sheet is always in the active workbook. The one or more cells that are selected in the active sheet are known as the active cells. If an embedded object has focus, the last-selected cells are still active.</span></span> 
  
<span data-ttu-id="fb303-p103">「現在」という用語は、Excel が計算しているものを指します。現在のブックとワークシートは、現在再計算を行っているブックやワークシートを指します。現在のシートは、必ず現在のブック内にあります。再計算されているセルは現在のセルと呼ばれます。また、配列数式が再計算されている場合も、現在のセルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="fb303-p103">The term current refers to what Excel is recalculating. The current workbook and worksheet are those that are currently being recalculated. The current sheet is always in the current workbook. The cell being recalculated is known as the current cell, or, in the case of an array formula being recalculated, the current cells.</span></span> 
  
<span data-ttu-id="fb303-120">覚えておくべき重要なポイントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fb303-120">The important points to remember are as follows:</span></span>
  
- <span data-ttu-id="fb303-121">作業中のブックやシート、セルが、必ずしも現在のブックやシート、セルになるわけではありません (現在のものである場合もあります)。</span><span class="sxs-lookup"><span data-stu-id="fb303-121">The active workbook/worksheet/cell is not generally the current one, although it can be.</span></span>
    
- <span data-ttu-id="fb303-122">Visual Basic for Applications (VBA) モジュールや 、DLL または XLL において、アドイン関数は、現在のシート上にある現在のセルから呼び出されます。マルチ スレッド再計算 (MTR) の場合は、それらのいずれかから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fb303-122">An add-in function, whether in a Visual Basic for Applications (VBA) module or a DLL or XLL, is always called from the current cell on the current sheet, or one of them in the case of multithreaded recalculation (MTR).</span></span>
    
<span data-ttu-id="fb303-p104">ブック内のセル、セル範囲、シートについての情報を提供する多くの Excel の関数は、作業中のブック、シート、セルと、現在のブック、シート、セルとを区別します。これらの相違点は、次のセクションに記載されているとおり、セル ブロックの参照を表すために使用するデータ型にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="fb303-p104">Many Excel functions that provide information about a cell, a range of cells, or a sheet in a workbook distinguish between the active workbook, sheet, or cell and the current workbook, sheet, or cell. This difference is reflected in the data types used to describe references to blocks of cells, as described in the following section.</span></span>
  
## <a name="internal-and-external-worksheet-references"></a><span data-ttu-id="fb303-125">内部ワークシートおよび外部ワークシートの参照</span><span class="sxs-lookup"><span data-stu-id="fb303-125">Internal and External Worksheet References</span></span>

<span data-ttu-id="fb303-p105">内部参照と外部参照の主な違いは、外部参照のデータ型には、ワークシート ID に加えて、参照先セルの記述が含まれていることです。内部参照にはシートへの参照が含まれていません。シートが現在のシートであることを暗黙的に示します。</span><span class="sxs-lookup"><span data-stu-id="fb303-p105">The key difference between internal and external references is that the external reference data type contains an ID for the worksheet and also a description of which cells are referred to. An internal reference contains no reference to the sheet—it is implicit that the sheet is the current sheet.</span></span> 
  
<span data-ttu-id="fb303-128">多くの C API 関数は、参照を返すか、参照引数を取ります。</span><span class="sxs-lookup"><span data-stu-id="fb303-128">Many C API functions return references or take reference arguments.</span></span> <span data-ttu-id="fb303-129">参照引数を取る C API 関数は、いずれも内部参照または外部参照のどちらも受け入れます。ただし、**xlSheetNm** 関数は例外であり、外部参照が必要です。</span><span class="sxs-lookup"><span data-stu-id="fb303-129">Any C API function that takes reference arguments accepts either internal or external references, except the **xlSheetNm** function, which requires an external reference.</span></span> <span data-ttu-id="fb303-130">関数によっては、内部参照または外部参照のいずれか一方のみを返します。</span><span class="sxs-lookup"><span data-stu-id="fb303-130">Some functions only return either internal or external references.</span></span> <span data-ttu-id="fb303-131">たとえば、C API 関数 [xlfCaller](xlfcaller.md) は、定義により、現在のシート上の呼び出し元のセルへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="fb303-131">For example, the C API function [xlfCaller](xlfcaller.md) returns a reference to the calling cells, by definition, on the current sheet.</span></span> <span data-ttu-id="fb303-132">返される参照は常に内部参照になります。ただし、関数がワークシートのセルから呼び出されたのでない場合、非参照型を返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fb303-132">The returned reference is always an internal reference, although the function can return non-reference types where the function is not called from a worksheet cell.</span></span> <span data-ttu-id="fb303-133">C API 関数 [xlSheetId](xlsheetid.md) は、必ず外部参照データ型に含まれるワークシート ID を返します。</span><span class="sxs-lookup"><span data-stu-id="fb303-133">The C API function [xlSheetId](xlsheetid.md) always returns the ID of a worksheet contained within an external reference data type.</span></span> 
  
<span data-ttu-id="fb303-p107">内部参照型と外部参照型の、もう一つの主な違いは、外部参照のデータ型は同じシート上の複数の離散したセル ブロックを表すことができるという点です。内部参照では、現在のシートの 1 ブロックのみを表すことができます。離散した参照は、範囲の引数を取る任意の関数に渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="fb303-p107">The other key difference between the internal and external reference types is that the external reference data type can describe multiple disjoint blocks of cells on the same sheet. Internal references can describe only a single block on the current sheet. Disjoint references can be passed to any function that takes a range argument.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb303-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb303-137">See also</span></span>



[<span data-ttu-id="fb303-138">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="fb303-138">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="fb303-139">名前と他のワークシートの数式を評価する</span><span class="sxs-lookup"><span data-stu-id="fb303-139">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[<span data-ttu-id="fb303-140">Excel ワークシートと式の評価</span><span class="sxs-lookup"><span data-stu-id="fb303-140">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)

