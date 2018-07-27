---
title: Excel の再計算
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798844"
---
# <a name="excel-recalculation"></a><span data-ttu-id="c65ad-104">Excel の再計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-104">Excel Recalculation</span></span>

 <span data-ttu-id="c65ad-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c65ad-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c65ad-106">Microsoft Excel の再計算は、複数の方法でトリガーできます。次に、その例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="c65ad-107">新しいデータを入力する (Excel が、このトピックで説明する自動計算モードの場合)。</span><span class="sxs-lookup"><span data-stu-id="c65ad-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="c65ad-108">ブックの一部またはすべての再計算を Excel に明示的に指示する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="c65ad-109">行または列を削除または挿入する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="c65ad-110">**[保存前に再計算]** オプションをオンにしているときにブックを保存する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="c65ad-111">特定の [オートフィルタ] のアクションを実行する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="c65ad-112">行または列の区切り線をダブルクリックする (自動再計算モード時)。</span><span class="sxs-lookup"><span data-stu-id="c65ad-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="c65ad-113">定義された名前を追加、編集、または削除する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="c65ad-114">ワークシートの名前を変更する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="c65ad-115">別のワークシートとの相対位置を変更する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="c65ad-116">列ではなく、行を非表示または再表示する。</span><span class="sxs-lookup"><span data-stu-id="c65ad-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c65ad-p101">このトピックでは、ユーザーが直接キーを押したりマウスをクリックしたりすることと、コマンドやマクロによって該当するタスクが実行されることを区別しません。ユーザーはコマンドを実行するか、何らかの操作によってコマンドが実行されるようにしますが、これはユーザー アクションと見なされます。そのため、「ユーザー」というフレーズは、「ユーザー、またはユーザーによって開始されたコマンドまたはプロセス」という意味にもなります。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="c65ad-120">依存関係、ダーティ セル、および再計算されるセル</span><span class="sxs-lookup"><span data-stu-id="c65ad-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="c65ad-121">Excel のワークシートの計算は、3 段階のプロセスと見なせます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="c65ad-122">依存関係ツリーの構築</span><span class="sxs-lookup"><span data-stu-id="c65ad-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="c65ad-123">計算チェーンの構築</span><span class="sxs-lookup"><span data-stu-id="c65ad-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="c65ad-124">セルの再計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-124">Recalculation of cells</span></span>
    
<span data-ttu-id="c65ad-p102">依存関係ツリーによって、Excel は、セル間の依存関係または同等性、セル間の参照関係についての情報を得ます。Excel は、このツリーから計算チェーンを構築します。計算チェーンは、数式を格納しているすべてのセルの一覧であり、計算される順序で並べられています。再計算時に、まだ計算されていないセルに依存する数式が見つかると、このチェーンは Excel によって改訂されます。この場合、計算されるセルとそのセルの参照先は、チェーンの末尾方向に移動されます。このため、開いた直後のワークシートでの最初の数回の計算サイクルは、多くの場合、計算時間が向上します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="c65ad-131">新しい数式が入力されるなど、ブックに構造上の変更が行われると、Excel は依存関係ツリーと計算チェーンを再構築します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-131">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain.</span></span> <span data-ttu-id="c65ad-132">新しいデータや新しい数式が入力されると、その新しいデータに依存するセルのすべてに、再計算が必要であるというマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-132">When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation.</span></span> <span data-ttu-id="c65ad-133">このようにマークが付けられたセルは、*ダーティ*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-133">Cells that are marked in this way are known as  *dirty*  .</span></span> <span data-ttu-id="c65ad-134">直接および間接のすべての参照先に、ダーティのマークが付きます。そのため、B1 が A1 に依存していて、C1 が B1 に依存している場合、A1 が変更されると、B1 と C1 の両方にダーティのマークが付きます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-134">All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="c65ad-p104">あるセルがそのセル自体に直接的または間接的に依存している場合は、Excel によって循環参照が検出され、ユーザーに警告が示されます。これは、通常ユーザーが修正しなければならないエラー状態です。Excel には、ユーザーが循環依存の関係の原因を見つけられるようにする非常に役立つグラフィカルなナビゲーション ツールがあります。場合によっては、この状態を意図的に必要とすることもあります。たとえば、次の繰り返しの開始点が、前の繰り返しの結果になる反復計算の実行を必要とすることがあります。Excel は、[計算方法の設定] ダイアログ ボックスによる反復計算の制御をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="c65ad-p105">セルにダーティのマークを付けた後、次回の再計算が実行されるときに、Excel は、それぞれのダーティ セルの内容を計算チェーンで指定された順序で再評価します。前述の例では、最初に B1、次に C1 の順になります。この再計算は、再計算モードが自動になっている場合には、Excel がセルにダーティのマークを付け終わった直後に実行されます。それ以外の場合は、再計算は後で実行されます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="c65ad-p106">Microsoft Excel 2002 以降の Microsoft Visual Basic for Applications (VBA) の **Range** オブジェクトは、セルに計算が必要というマークを付ける **Range.Dirty** メソッドをサポートしています。このメソッドを **Range.Calculate** メソッドと併用すると (次のセクションを参照)、特定の範囲内のセルを強制的に再計算できるようになります。これは、計算モードが手動に設定されているときに、マクロで限定的な計算を実行する際に、そのマクロ関数とは無関係のセルを計算するオーバーヘッドを回避するために役立ちます。範囲計算のメソッドは、C API では使用できません。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="c65ad-p107">Excel 2002 以前のバージョンの Excel では、開いている各ブックのワークシートごとに計算チェーンを構築していました。このため、処理されるワークシート間のリンク方法は複雑になり、効率的な再計算のためには注意が必要でした。特に Excel 2000 では、ワークシート間の依存関係を最小限にして、ワークシートにアルファベット順の名前を付ける必要があります。このようにして、他のシートに依存するシートが、依存先のシートの後に (アルファベット順) なるようにします。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="c65ad-150">Excel 2007 ではロジックが向上し、計算チェーンの各部分が相互依存しなくなり、同時に計算できるため、複数のスレッドでの再計算が可能です。</span><span class="sxs-lookup"><span data-stu-id="c65ad-150">In xlxlshort, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> <span data-ttu-id="c65ad-151">Excel は、単一プロセッサのコンピューターで複数のスレッドを使用するように構成することも、複数プロセッサやマルチコア プロセッサのコンピューターで単一のスレッドを使用するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-151">In xlxlshort, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time. You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="c65ad-152">非同期のユーザー定義関数 (UDF)</span><span class="sxs-lookup"><span data-stu-id="c65ad-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="c65ad-p109">計算中に非同期の UDF が現れると、現在の数式の状態が保存され、UDF が開始されて、残りのセルの評価が続行されます。計算ですべてのセルの評価が終了したときに、まだ実行中の非同期関数がある場合、Excel は非同期関数が完了するまで待機します。各非同期関数が結果を報告したときに、Excel は数式を終了して、非同期関数への参照を含むセルを使用しているセルの再計算のために新しい計算パスを実行します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="c65ad-156">揮発性関数と非揮発性関数</span><span class="sxs-lookup"><span data-stu-id="c65ad-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="c65ad-p110">Excel では、揮発性関数の概念をサポートしています。これは、その関数の引数が変更されていなくても (関数が引数を取る場合)、ある瞬間と次の瞬間では値が異なる可能性があると見なされる関数です。Excel は、再計算のたびに、揮発性関数が含まれているセルをすべての参照先と共に再評価します。このため、揮発性関数に依存しすぎていると、再計算にかかる時間が長くなる可能性があります。控えめに使用するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="c65ad-161">次に示す Excel 関数は揮発性です。</span><span class="sxs-lookup"><span data-stu-id="c65ad-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="c65ad-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="c65ad-162">**NOW**</span></span>
    
- <span data-ttu-id="c65ad-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="c65ad-163">**TODAY**</span></span>
    
- <span data-ttu-id="c65ad-164">**RANDBETWEEN**</span><span class="sxs-lookup"><span data-stu-id="c65ad-164">**RandBetween**</span></span>
    
- <span data-ttu-id="c65ad-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="c65ad-165">**OFFSET**</span></span>
    
- <span data-ttu-id="c65ad-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="c65ad-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="c65ad-167">**INFO** (引数によって異なります)</span><span class="sxs-lookup"><span data-stu-id="c65ad-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="c65ad-168">**CELL** (引数によって異なります)</span><span class="sxs-lookup"><span data-stu-id="c65ad-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="c65ad-169">**SUMIF** (引数によって異なります)</span><span class="sxs-lookup"><span data-stu-id="c65ad-169">**CELL** (depending on its arguments)</span></span> 
    
<span data-ttu-id="c65ad-p111">VBA と C API は、揮発性として処理する必要のあるユーザー定義間数 (UDF) について Excel に通知する手段をサポートしています。VBA を使用する場合は、次のようにすると UDF が揮発性として宣されます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="c65ad-p112">既定では、Excel は VBA の UDF を非揮発性であると見なします。Excel は、UDF の最初の呼び出し時に、その UDF が揮発性であることを認識します。この例のように、揮発性 UDF は非揮発性に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="c65ad-p113">C API を使用する場合は、XLL 関数を最初の呼び出し前に揮発性として登録できます。また、ワークシート関数の揮発性状態のオン/オフを切り替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="c65ad-p114">既定では、Excel は範囲引数を受け取り、マクロ シートと同等のものとして宣言された XLL UDF を揮発性として処理します。この既定の状態は、UDF が最初に呼び出されるときに **xlfVolatile** 関数を使用することでオフにできます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="c65ad-179">計算モード、コマンド、選択的な再計算、およびデータ テーブル</span><span class="sxs-lookup"><span data-stu-id="c65ad-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="c65ad-180">Excel には 3 つの計算モードがあります。</span><span class="sxs-lookup"><span data-stu-id="c65ad-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="c65ad-181">自動</span><span class="sxs-lookup"><span data-stu-id="c65ad-181">Automatic</span></span>
    
- <span data-ttu-id="c65ad-182">テーブル以外自動</span><span class="sxs-lookup"><span data-stu-id="c65ad-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="c65ad-183">Manual</span><span class="sxs-lookup"><span data-stu-id="c65ad-183">Manual</span></span>
    
<span data-ttu-id="c65ad-p115">計算が自動に設定されていると、データ入力の後に再計算が毎回実行されます。また、前のセクションで例を示したように、特定のイベントの後にも再計算が発生します。非常に巨大なブックの場合、再計算に長い時間がかかるようになり、この事態が発生した場合はユーザーによる制限が必要になります。つまり、再計算は必要なときにのみ行うということです。これを可能にするために、Excel では手動モードをサポートしています。ユーザーは、Excel のメニュー システムからモードを選択することも、VBA、COM、または C API を使用することで、プログラムによってモードを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="c65ad-p116">データ テーブルとは、ワークシート内の特殊な構造のことです。最初に、ユーザーは結果の計算をワークシートにセット アップします。これは、1 つまたは 2 つのキーになる変更可能な入力と、その他のパラメーターによって決まります。次に、ユーザーは一方または両方のキーになる入力の値のセットに対する結果のテーブルを作成します。テーブルの作成には、**データ テーブル ウィザード**を使用します。テーブルのセット アップ後、Excel は入力を 1 つずつ計算に組み込んで、結果の値をテーブルにコピーします。1 つまたは 2 つの入力が使用できるため、データ テーブルは 1 次元または 2 次元になります。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="c65ad-195">データ テーブルの再計算の処理方法は若干異なります。</span><span class="sxs-lookup"><span data-stu-id="c65ad-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="c65ad-196">再計算は、通常のブックの再計算とは非同期に処理されます。これは、巨大なテーブルの再計算には、ブックの残りの部分よりも時間がかかることがあるためです。</span><span class="sxs-lookup"><span data-stu-id="c65ad-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="c65ad-p117">循環参照が許容されています。結果を得るために使用される計算がデータ テーブルの 1 つまたは 2 つの値に依存する場合、Excel は循環依存の関係に関するエラーを返しません。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="c65ad-p118">Excel がデータ テーブルの再計算を別の方法で処理することと、複雑な計算または非常に長い計算に依存する巨大なテーブルの計算には時間がかかるという事実から、Excel ではデータ テーブルの自動計算を無効化できるようになっています。これを行うには、計算モードを [データ テーブル以外自動] に設定します。計算がこのモードのときには、ユーザーが F9 を押すか、それと同等のプログラムによる操作を実行することで、データ テーブルが再計算されます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="c65ad-p119">Excel は、再計算モードの変更と再計算の制御に利用できるメソッドを公開しています。これに該当するメソッドは、バージョンが進むごとに改善されていて、より細かい制御が可能になっています。これに関連する C API の機能は、Excel バージョン 5 で使用可能だったものを反映しているため、それよりも新しい VBA を使用することで得られるものと同じ制御は得られません。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="c65ad-205">Excel が手動計算モードのときに最も頻繁に使用されるメソッドは、ブック、ワークシート、および範囲の選択的な計算を可能にするメソッド、開いているすべてのブックの完全な再計算を可能にするメソッド、さらに依存関係ツリーと計算チェーンの完全な再構築を可能にするメソッドです。</span><span class="sxs-lookup"><span data-stu-id="c65ad-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="c65ad-206">範囲計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-206">Range Calculation</span></span>

<span data-ttu-id="c65ad-207">キーボード操作: なし</span><span class="sxs-lookup"><span data-stu-id="c65ad-207">Keystroke: None</span></span>
  
<span data-ttu-id="c65ad-208">VBA: **Range.Calculate** (Excel 2000 で導入、Excel 2007 で変更) および **Range.CalculateRowMajorOrder** (Excel 2007 で導入)</span><span class="sxs-lookup"><span data-stu-id="c65ad-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="c65ad-209">C API: サポートなし</span><span class="sxs-lookup"><span data-stu-id="c65ad-209">C API: Not supported</span></span>
  
- <span data-ttu-id="c65ad-210">**[手動] モード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-210">**Manual mode**</span></span>
    
    <span data-ttu-id="c65ad-p120">特定の範囲内のセルのみを再計算します (セルがダーティかどうかは関係ありません)。**Range.Calculate** メソッドの動作は Excel 2007 で変更されています。ただし、以前の動作も **Range.CalculateRowMajorOrder** メソッドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="c65ad-213">**[自動] または [テーブル以外自動] モード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="c65ad-214">ブックを再計算しますが、範囲の再計算または範囲に含まれるセルの再計算を強制しません。</span><span class="sxs-lookup"><span data-stu-id="c65ad-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="c65ad-215">アクティブなワークシートの計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="c65ad-216">キーボード操作: SHIFT + F9</span><span class="sxs-lookup"><span data-stu-id="c65ad-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="c65ad-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="c65ad-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="c65ad-218">C API: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="c65ad-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="c65ad-219">**すべてのモード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-219">**All modes**</span></span>
    
    <span data-ttu-id="c65ad-220">アクティブなワークシート内でのみ、計算のマークが付けられているセルを再計算します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="c65ad-221">指定されたワークシートの計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="c65ad-222">キーボード操作: なし</span><span class="sxs-lookup"><span data-stu-id="c65ad-222">Keystroke: None</span></span>
  
<span data-ttu-id="c65ad-223">VBA: **Worksheets(** reference **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="c65ad-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="c65ad-224">C API: サポートなし</span><span class="sxs-lookup"><span data-stu-id="c65ad-224">C API: Not supported</span></span>
  
- <span data-ttu-id="c65ad-225">**すべてのモード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-225">**All modes**</span></span>
    
    <span data-ttu-id="c65ad-p121">指定されたワークシート内でのみ、ダーティなセルとそのセルの参照先を再計算します。参照は文字列としてのワークシートの名前、または関連するブックのインデックス番号です。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="c65ad-p122">Excel 2000 以降のバージョンでは、**Boolean** ワークシート プロパティである **EnableCalculation** プロパティが公開されています。これを **False** から **True** に設定すると、指定されたワークシート内のすべてのセルがダーティになります。自動モードの場合は、これによりブック全体の再計算もトリガーされます。 </span><span class="sxs-lookup"><span data-stu-id="c65ad-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="c65ad-231">手動モードの場合は、次のコードでアクティブ シートのみの再計算が行われます。</span><span class="sxs-lookup"><span data-stu-id="c65ad-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="c65ad-232">ブックのツリーの再構築と再計算の強制</span><span class="sxs-lookup"><span data-stu-id="c65ad-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="c65ad-233">キーボード操作: CTRL + ALT + SHIFT + F9 (Excel 2002 で導入されました)</span><span class="sxs-lookup"><span data-stu-id="c65ad-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="c65ad-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (Excel 2007 で導入)</span><span class="sxs-lookup"><span data-stu-id="c65ad-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="c65ad-235">C API: サポートなし</span><span class="sxs-lookup"><span data-stu-id="c65ad-235">C API: Not supported</span></span>
  
- <span data-ttu-id="c65ad-236">**すべてのモード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-236">**All modes**</span></span>
    
    <span data-ttu-id="c65ad-237">Excel によって特定のブックの依存関係ツリーと計算チェーンが再構築され、数式を含んでいるすべてのセルの再計算を強制します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="c65ad-238">開いているすべてのブック</span><span class="sxs-lookup"><span data-stu-id="c65ad-238">All Open Workbooks</span></span>

<span data-ttu-id="c65ad-239">キーボード操作: F9</span><span class="sxs-lookup"><span data-stu-id="c65ad-239">Keystroke: F9</span></span>
  
<span data-ttu-id="c65ad-240">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="c65ad-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="c65ad-241">C API: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="c65ad-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="c65ad-242">**すべてのモード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-242">**All modes**</span></span>
    
    <span data-ttu-id="c65ad-p123">Excel によってダーティのマークが付けられたすべてのセル (揮発性データと変更されたデータの参照先、およびプログラムによりダーティのマークが付けられたセル) を再計算します。計算モードが [テーブル以外自動] の場合は、更新を必要とするテーブルに加えて、すべての揮発性関数とその関数の参照先も生産します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="c65ad-245">開いているすべてのブックのツリーの再構築と計算の強制</span><span class="sxs-lookup"><span data-stu-id="c65ad-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="c65ad-246">キーボード操作: CTRL + ALT + F9</span><span class="sxs-lookup"><span data-stu-id="c65ad-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="c65ad-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="c65ad-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="c65ad-248">C API: サポートなし</span><span class="sxs-lookup"><span data-stu-id="c65ad-248">C API: Not supported</span></span>
  
- <span data-ttu-id="c65ad-249">**すべてのモード**</span><span class="sxs-lookup"><span data-stu-id="c65ad-249">**All modes**</span></span>
    
    <span data-ttu-id="c65ad-p124">開いているすべてのブックに含まれるすべてのセルを再計算します。計算モードが [テーブル以外自動] の場合は、テーブルの再計算を強制します。</span><span class="sxs-lookup"><span data-stu-id="c65ad-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c65ad-252">関連項目</span><span class="sxs-lookup"><span data-stu-id="c65ad-252">See also</span></span>



[<span data-ttu-id="c65ad-253">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="c65ad-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="c65ad-254">Excel で使用されるデータ型</span><span class="sxs-lookup"><span data-stu-id="c65ad-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="c65ad-255">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="c65ad-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="c65ad-256">Excel プログラミングの概念</span><span class="sxs-lookup"><span data-stu-id="c65ad-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

