---
title: Excel でのマルチスレッド再計算
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310506"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="11e4e-104">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="11e4e-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="11e4e-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="11e4e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="11e4e-p101">Microsoft Office Excel 2007は、ワークシートのマルチスレッド再計算（MTR）を使用した最初のバージョンのExcelです。コンピューター上のプロセッサまたはプロセッサコアの数に関係なく、再計算時に最大1024の同時スレッドを使用するようにExcelを構成できます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p101">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets. You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="11e4e-108">それぞれのスレッドには関連するオペレーティング システムのオーバーヘッドがあるため、必要以上に多くのスレッドを使用するように Excel を構成してはいけません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="11e4e-109">コンピューターに複数のプロセッサまたはプロセッサのコアが搭載されている場合は、オペレーティング システムが、最適な方法でプロセッサにスレッドを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="11e4e-110">Excel の MTR の概要</span><span class="sxs-lookup"><span data-stu-id="11e4e-110">Excel MTR overview</span></span>

<span data-ttu-id="11e4e-p102">Excelは、別々のスレッドで同時に再計算できる計算チェーンの部位の認識を試みます。以下のごく単純化されたツリー（x←yはyがxにのみ依存することを意味）はこの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p102">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads. The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="11e4e-113">**図 1. 別々のスレッドでの同時並行計算**</span><span class="sxs-lookup"><span data-stu-id="11e4e-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="11e4e-114">![複数のスレッドでの同時並行計算](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "複数のスレッドでの同時並行計算")</span><span class="sxs-lookup"><span data-stu-id="11e4e-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="11e4e-115">A1 の計算が済むと、一方のスレッドでは A2、A3 の順に計算ができるようになり、同時に、もう一方のスレッドでは B1、C1 の順に計算ができるようになります (すべてのセルがスレッド セーフであると仮定しています)。</span><span class="sxs-lookup"><span data-stu-id="11e4e-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="11e4e-p103">スレッドセーフセルとは、スレッドセーフ関数のみを含むセルを意味します。スレッドセーフとは何か、スレッドセーフでないものとは、については、[エクセルがスレッドセーフとみなすもの・みなさないもの](#xl2007xllsdk_threadsafe)に記載されています。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p103">The term thread-safe cell means a cell that only contains thread-safe functions. What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="11e4e-p104">ほとんどの実用的なワークブックには、この例よりはるかに複雑な依存関係ツリーが含まれています。さらに、セルの再計算時間は計算が完了するまで知ることができず、関数の引数によって大きく異なります。最良の結果を得るために、Excelは最適化がそれ以上不可能になるまで各計算の計算順序を改善しようとします。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p104">Most practical workbooks contain far more complex dependency trees than this example. Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments. To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="11e4e-121">Excel は、次の項目の実行に単一のメイン スレッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="11e4e-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="11e4e-122">組み込みコマンド</span><span class="sxs-lookup"><span data-stu-id="11e4e-122">Built-in commands</span></span>
    
- <span data-ttu-id="11e4e-123">XLL コマンド</span><span class="sxs-lookup"><span data-stu-id="11e4e-123">XLL commands</span></span>
    
- <span data-ttu-id="11e4e-124">アドイン マネージャー インターフェイス関数 (**xlAutoOpen** 関数など)</span><span class="sxs-lookup"><span data-stu-id="11e4e-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="11e4e-125">Microsoft Visual Basic for Applications (VBA) のユーザー定義コマンド (通常はマクロと呼ばれます)</span><span class="sxs-lookup"><span data-stu-id="11e4e-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="11e4e-126">VBA のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="11e4e-127">組み込みのスレッド セーフではないワークシート関数 (次のセクションに一覧を示します)</span><span class="sxs-lookup"><span data-stu-id="11e4e-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="11e4e-128">XLM マクロ シートのユーザー定義コマンドとユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="11e4e-129">COM アドインのコマンドと関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="11e4e-130">条件付きフォーマット式内の関数と演算子</span><span class="sxs-lookup"><span data-stu-id="11e4e-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="11e4e-131">ワークシートの式で使用された定義済みの名前定義内の関数と演算子</span><span class="sxs-lookup"><span data-stu-id="11e4e-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="11e4e-132">数式編集ボックス内の式の強制的な評価 (**F9** キーを使用)</span><span class="sxs-lookup"><span data-stu-id="11e4e-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="11e4e-p105">関数がスレッドセーフかどうかにかかわらず、すべてのワークシートの数式は、Excelが複数のスレッドを使用するように構成されていない限り、メインスレッドで判断されます。ユーザーが複数のスレッドを使用するように指定した場合、追加のスレッドがスレッドセーフセルに使用されます。メインスレッドは、負荷分散の観点上有用な場合でも、スレッドセーフセルに使用されることがあります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p105">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread. When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells. Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="11e4e-136">ここでもう一度強調すべきこととして、Excel は一度に複数のコマンドを実行しません。そのため、スレッド ローカル メモリとクリティカル セクションの使用など、スレッド セーフな関数を記述するときと同様の注意を払う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="11e4e-137">Excel でスレッド セーフと見なされるもの (見なされないもの)</span><span class="sxs-lookup"><span data-stu-id="11e4e-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="11e4e-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="11e4e-138"></span></span>

<span data-ttu-id="11e4e-139">Excel では、次のものだけがスレッド セーフと見なされます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="11e4e-140">Excel の単項演算子と二項演算子のすべて</span><span class="sxs-lookup"><span data-stu-id="11e4e-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="11e4e-141">Excel 2007以降のほぼすべての組み込みワークシート関数（例外リストを参照）</span><span class="sxs-lookup"><span data-stu-id="11e4e-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="11e4e-142">スレッド セーフとして明示的に登録されている XLL アドイン関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="11e4e-143">次の組み込みワークシート関数は、スレッド セーフではありません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="11e4e-144">**PHONETIC**</span><span class="sxs-lookup"><span data-stu-id="11e4e-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="11e4e-145">"format"または "address"引数が使用されている場合は**CELL**</span><span class="sxs-lookup"><span data-stu-id="11e4e-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="11e4e-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="11e4e-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="11e4e-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="11e4e-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="11e4e-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="11e4e-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="11e4e-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="11e4e-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="11e4e-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="11e4e-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="11e4e-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="11e4e-151">**CUBESET**</span></span>
    
- <span data-ttu-id="11e4e-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="11e4e-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="11e4e-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="11e4e-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="11e4e-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="11e4e-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="11e4e-155">**ADDRESS** (5 番目のパラメーター "sheet_name" が指定されている場合)</span><span class="sxs-lookup"><span data-stu-id="11e4e-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="11e4e-156">ピボットテーブルを参照するデータベース関数 (**DSUM**、**DAVERAGE** など)</span><span class="sxs-lookup"><span data-stu-id="11e4e-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="11e4e-157">**ERROR.TYPE**</span><span class="sxs-lookup"><span data-stu-id="11e4e-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="11e4e-158">**HYPERLINK**</span><span class="sxs-lookup"><span data-stu-id="11e4e-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="11e4e-159">明確にするために、スレッド セーフと見なされないものを挙げます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="11e4e-160">VBA のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="11e4e-161">COM アドインのユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="11e4e-162">XLM マクロ シートのユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="11e4e-163">明示的にスレッド セーフとして登録されていない XLL アドイン関数</span><span class="sxs-lookup"><span data-stu-id="11e4e-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="11e4e-164">次の操作と関数はスレッド セーフとは見なされません。また、スレッド セーフとして登録した XLL 関数から呼び出されると失敗します。</span><span class="sxs-lookup"><span data-stu-id="11e4e-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="11e4e-165">XLM 情報関数 (**xlfGetCell** (**GET.CELL**) など) の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="11e4e-166">XLL 内部名の定義または削除のための **xlfSetName** (**SET.NAME**) の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="11e4e-167">スレッド セーフではないユーザー定義関数の **xlUDF** を使用した呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="11e4e-168">スレッド セーフではない関数を含む式、またはスレッド セーフではない関数を含む定義によって定義された名前を含む式に対する [xlfEvaluate](xlfevaluate.md) 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="11e4e-169">ブレーク条件をクリアする [xlAbort](xlabort.md) 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="11e4e-170">計算されていないセルの参照の値を取得する [xlCoerce](xlcoerce.md) 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="11e4e-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="11e4e-171">XLLワークシート関数は、スレッドセーフとして登録されているかどうかにかかわらず、**xlcSave**などのC APIコマンドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="11e4e-p106">スレッドセーフとして宣言されたXLL関数がXLM情報関数を呼び出したり、未計算のセルを参照したりすることはできないため、Excelでは、マクロシートに相当するものとして登録されているXLL関数をスレッドセーフとして登録することはできません。したがって、**xlCoerce**を使用して未計算のセル参照の値を取得しようとすると、**xlretUncalced**エラーとなります。 XLM情報関数を呼び出すと、**xlretFailed**エラーとなります。上記のその他の地点では、Excel C APIで導入されたエラーコード**xlretNotThreadSafe**エラーとなります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p106">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe. Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error. Calling an XLM information function fails with an **xlretFailed** error. The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="11e4e-176">C API 専用のコールバック関数は、すべてスレッド セーフです。</span><span class="sxs-lookup"><span data-stu-id="11e4e-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="11e4e-177">**xlCoerce**（未計算のセル参照の強制が失敗した場合を除く）</span><span class="sxs-lookup"><span data-stu-id="11e4e-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="11e4e-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="11e4e-178">**xlFree**</span></span>
    
- <span data-ttu-id="11e4e-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="11e4e-179">**xlStack**</span></span>
    
- <span data-ttu-id="11e4e-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="11e4e-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="11e4e-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="11e4e-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="11e4e-182">**xlAbort**（中断条件をクリアするために使用される場合を除く）</span><span class="sxs-lookup"><span data-stu-id="11e4e-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="11e4e-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="11e4e-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="11e4e-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="11e4e-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="11e4e-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="11e4e-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="11e4e-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="11e4e-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="11e4e-187">1つの例外は**xlSet**関数です。これは、いずれにせよ、コマンドと同等であるため、どのワークシート関数からも呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="11e4e-p107">XLLワークシート関数はスレッドセーフとしてExcelに登録できます。これはExcelに、その関数が安全かつ同時に複数のスレッドで呼び出されることができると伝達します。ただし、関数の動作を必ずご確認ください。スレッドセーフとして登録された関数が安全に動作しない場合、Excelを不安定にする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p107">An XLL worksheet function can be registered with Excel as thread safe. This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case. You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="11e4e-191">XLL 関数をスレッド セーフとして登録する</span><span class="sxs-lookup"><span data-stu-id="11e4e-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="11e4e-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="11e4e-192"></span></span>

<span data-ttu-id="11e4e-193">スレッド セーフな関数を記述するときに、開発者が従う必要のあるルールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="11e4e-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="11e4e-194">スレッド セーフではない可能性のある別の DLL 内のリソースを呼び出さない。</span><span class="sxs-lookup"><span data-stu-id="11e4e-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="11e4e-195">C API または COM を通じてスレッド セーフでない呼び出しを行わない。</span><span class="sxs-lookup"><span data-stu-id="11e4e-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="11e4e-196">クリティカル セクションを使用して、複数のスレッドで同時に使用される可能性のあるリソースを保護する。</span><span class="sxs-lookup"><span data-stu-id="11e4e-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="11e4e-197">スレッド固有のストレージにはスレッド ローカル メモリを使用して、関数内の静的変数はスレッド ローカル変数に置き換える。</span><span class="sxs-lookup"><span data-stu-id="11e4e-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="11e4e-198">Excel には、もう 1 つの制限が課せられます。スレッド セーフな関数をマクロ シートと同等なものとして登録することはできません。そのため、XLM 情報関数を呼び出すことや、再計算されていないセルの値を取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="11e4e-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="11e4e-199">メモリの競合</span><span class="sxs-lookup"><span data-stu-id="11e4e-199">Memory contention</span></span>
<span data-ttu-id="11e4e-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="11e4e-200"></span></span>

<span data-ttu-id="11e4e-201">マルチスレッド システムは、2 つの基本的な問題に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="11e4e-202">複数のスレッドが読み書きするメモリの保護方法。</span><span class="sxs-lookup"><span data-stu-id="11e4e-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="11e4e-203">実行中のスレッドに関連付けられてプライベートになるメモリの作成方法とアクセス方法。</span><span class="sxs-lookup"><span data-stu-id="11e4e-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="11e4e-p108">WindowsオペレーティングシステムとWindowsソフトウェア開発キット（SDK）には、それぞれ主要領域、およびスレッドローカルストレージ（TLS）APIの両方へのツールが用意されています。詳しくは、[Excelのメモリー管理](memory-management-in-excel.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p108">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="11e4e-p109">まず問題が発生しうる事例として、2つのワークシート関数（または同じ関数を同時に実行している2つのインスタンス）がDLLプロジェクトのグローバル変数にアクセスまたは変更する必要がある場合があります。このようなグローバル変数は、クラスオブジェクトの包括的にアクセス可能なインスタンスに隠される可能性があることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p109">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project. Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="11e4e-p110">2つ目の問題が発生する事例として、ワークシート関数が関数本体コード内で静的変数またはオブジェクトを宣言する場合があります。 C / C ++コンパイラは、すべてのスレッドが使用する単一のコピーのみを作成します。これは、関数の1つのインスタンスが値を変更できる一方で、別のスレッド上の別のインスタンスがその値が以前に設定されたものであると想定している可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p110">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code. The C/C++ compiler only creates a single copy that all threads use. This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="11e4e-211">MTR のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="11e4e-211">Example applications of MTR</span></span>
<span data-ttu-id="11e4e-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="11e4e-212"></span></span>

<span data-ttu-id="11e4e-p111">ワークシート関数をエクスポートするすべてのXLLは、Excelのマルチスレッド再計算（MTR）を利用できます。ただし、それらの関数がスレッドセーフでないアクションを実行する必要がない場合です。これにより、Excelはそれらに依存しているワークブックをできるだけ早く再計算することができます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p111">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions. This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="11e4e-p112">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result. In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function. If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made. This wastes the server's ability to process many calls at once. If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span><span class="sxs-lookup"><span data-stu-id="11e4e-p112">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result. In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function. If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made. This wastes the server's ability to process many calls at once. If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="11e4e-p113">Excelがサーバーと同じ数のスレッド（Nと呼称）を使用するように構成されていて、ブックの依存関係ツリーのトポロジーで許可されている場合、合計再計算時間はシングルスレッドの1 / Nにまで減少できる可能性があります。これは、（ワークブックが実行されている）クライアントコンピュータにプロセッサが1つしかない場合、特にサーバーへの呼び出しにかかる時間が、サーバーが呼び出しを処理するのにかかる時間と比べて短い場合でも同様です。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p113">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time. This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="11e4e-p114">追加スレッドごとにオペレーティングシステムの処理時間があります。そのため、特定のワークブック、特定のサーバーおよびクライアントコンピューターで、Excelに使用するスレッドの最適数を見つけるためには、ある程度の試験が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p114">There is operating system overhead for each additional thread. Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="11e4e-p115">たとえば、Excelを実行しているシングルプロセッサコンピューターと、1,000個のセルを含むブックを考えてみましょう。 UDFを呼び出し、次に1つ以上のリモートサーバーを呼び出します。 Excelが1つ1つの呼び出しが完了するのを待つ必要がないように、1,000のセルが互いに依存していないと仮定します（影響が出ない程度にこの制約から外れる例もあります）。 サーバーが100個の要求を同時に処理でき、Excelが100個のスレッドを使用するように構成されている場合、実行時間は1つのスレッドのみで稼動している場合の100分の1に短縮できます。 各スレッドにコールを割り当てる分の処理時間、および100個のスレッドを管理するオペレーティングシステムというものは、実際には、それほど大きい削減は起きません。ここには、サーバーが適切に拡張され、100個のタスクを同時に処理するように要求しても個々のタスクの完了時間に大きな影響はないという暗黙の前提もあります。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p115">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells. It calls a UDF, which in turn calls one or more remote servers. Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next. (Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used. The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great. There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="11e4e-230">この技法が大きなメリットになる実用的アプリケーションとして、モンテカルロ法など、小さなタスクに分割して複数のサーバーに依頼できる数値集約型のタスクが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="11e4e-231">Excel Services の考慮事項</span><span class="sxs-lookup"><span data-stu-id="11e4e-231">Excel Services considerations</span></span>
<span data-ttu-id="11e4e-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="11e4e-232"></span></span>

<span data-ttu-id="11e4e-p116">Excel Servicesは、サーバー上のExcelスプレッドシートの読み込み、計算、および表示をサポートしています。その後、ユーザーは標準のブラウザツールを使用して、スプレッドシートにアクセスして運用することができます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p116">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server. Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="11e4e-p117">Excel ServicesのUDFは、Microsoft .NET Frameworkマネージコードを使用して作成され、.NETアセンブリを通じて使用可能になります。 XLLはExcel Servicesではサポートされていません。マネージコードサーバーのUDFリソースは、その機能にアクセスするためにXLLを呼び出すことができます。そのため、ユーザーは、サーバーで読み込んだワークブックでもクライアントで読み込んだワークブックと同じ機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p117">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly. XLLs are not supported by Excel Services. A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="11e4e-p118">したがって、XLLの関数をこのように使用できるようにするには、引数と戻り値をネイティブデータ型から.NET Framework管理データ型に変換し、XLL関数を呼び出す.NETアセンブリでそれらを整形する必要があります。 .NETラッパーは、アクセスされているXLL関数ごとに1つのサーバーUDFをエクスポートします。追加の要件は、この方法で呼び出されるXLL関数はすべてスレッドセーフでなければならないということです。 XLL関数はクライアントExcelと同じ方法で登録されていないため、サーバーと.NETラッパーにはスレッドセーフであることを強制する方法がありません。これを確保するのはXLL開発者の管轄です。</span><span class="sxs-lookup"><span data-stu-id="11e4e-p118">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions. The .NET wrapper would export one server UDF for each XLL function being accessed. An additional requirement is that any XLL functions called in this way must be thread safe. Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe. It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11e4e-243">関連項目</span><span class="sxs-lookup"><span data-stu-id="11e4e-243">See also</span></span>

- [<span data-ttu-id="11e4e-244">Excel の再計算</span><span class="sxs-lookup"><span data-stu-id="11e4e-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="11e4e-245">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="11e4e-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="11e4e-246">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="11e4e-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="11e4e-247">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="11e4e-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="11e4e-248">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="11e4e-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

