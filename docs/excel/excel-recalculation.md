---
title: Excel �̍Čv�Z
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798844"
---
# <a name="excel-recalculation"></a><span data-ttu-id="7f8ff-104">Excel �̍Čv�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-104">Excel Recalculation</span></span>

 <span data-ttu-id="7f8ff-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7f8ff-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7f8ff-106">Microsoft Excel �̍Čv�Z�́A�����̕��@�Ńg���K�[�ł��܂��B���ɁA���̗������܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="7f8ff-107">�V�����f�[�^����͂��� (Excel ���A���̃g�s�b�N�Ő�����鎩���v�Z���[�h�̏ꍇ)�B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="7f8ff-108">�u�b�N�̈ꕔ�܂��͂��ׂĂ̍Čv�Z�� Excel �ɖ����I�Ɏw������B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="7f8ff-109">�s�܂��͗��폜�܂��͑}������B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="7f8ff-110">**[�ۑ��O�ɍČv�Z]** �I�v�V������I���ɂ��Ă���Ƃ��Ƀu�b�N��ۑ�����B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="7f8ff-111">����� [�I�[�g�t�B���^] �̃A�N�V��������s����B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="7f8ff-112">�s�܂��͗�̋�؂����_�u���N���b�N���� (�����Čv�Z���[�h��)�B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="7f8ff-113">��\`���ꂽ���O��ǉ��A�ҏW�A�܂��͍폜����B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="7f8ff-114">���[�N�V�[�g�̖��O��ύX����B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="7f8ff-115">�ʂ̃��[�N�V�[�g�Ƃ̑��Έʒu��ύX����B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="7f8ff-116">��ł͂Ȃ��A�s���\���܂��͍ĕ\������B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7f8ff-p101">[!����] ���̃g�s�b�N�ł́A���[�U�[�����ڃL�[���������}�E�X��N���b�N�����肷�邱�ƂƁA�R�}���h��}�N���ɂ���ĊY������^�X�N�����s����邱�Ƃ��ʂ��܂���B���[�U�[�̓R�}���h����s���邩�A���炩�̑���ɂ���ăR�}���h�����s�����悤�ɂ��܂����A����̓��[�U�[ �A�N�V�����ƌ��Ȃ���܂��B���̂��߁A�u���[�U�[�v�Ƃ����t���[�Y�́A�u���[�U�[�A�܂��̓��[�U�[�ɂ���ĊJ�n���ꂽ�R�}���h�܂��̓v���Z�X�v�Ƃ����Ӗ��ɂ�Ȃ�܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p101">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro. The user runs the command, or does something to cause the command to run so that it is still considered a user action. Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="7f8ff-120">�ˑ��֌W�A�_�[�e�B �Z���A����эČv�Z�����Z��</span><span class="sxs-lookup"><span data-stu-id="7f8ff-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="7f8ff-121">Excel �̃��[�N�V�[�g�̌v�Z�́A3 �i�K�̃v���Z�X�ƌ��Ȃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="7f8ff-122">�ˑ��֌W�c���[�̍\�z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="7f8ff-123">�v�Z�\`�F�[���̍\�z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="7f8ff-124">�Z���̍Čv�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-124">Recalculation of cells</span></span>
    
<span data-ttu-id="7f8ff-p102">依存関係ツリーによって、Excel は、セル間の依存関係または同等性、セル間の参照関係についての情報を得ます。Excel は、このツリーから計算チェーンを構築します。計算チェーンは、数式を格納しているすべてのセルの一覧であり、計算される順序で並べられています。再計算時に、まだ計算されていないセルに依存する数式が見つかると、このチェーンは Excel によって改訂されます。この場合、計算されるセルとそのセルの参照先は、チェーンの末尾方向に移動されます。このため、開いた直後のワークシートでの最初の数回の計算サイクルは、多くの場合、計算時間が向上します。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p102">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others. From this tree, Excel constructs a calculation chain. The calculation chain lists all the cells that contain formulas in the order in which they should be calculated. During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated. In this case, the cell that is being calculated and its dependents are moved down the chain. For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="7f8ff-131">構造上の変更が行われたとき、ブックに、新しい数式が入力されると、Excel には、依存関係ツリーおよび計算チェーンが再構築します。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-131">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain.</span></span> <span data-ttu-id="7f8ff-132">新しいデータまたは新しく作成した数式が入力されると、Excel が再計算を必要とすると新しいデータに依存するすべてのセルをマークします。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-132">When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation.</span></span> <span data-ttu-id="7f8ff-133">この方法でマークされているセルは、*ダーティ*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-133">Cells that are marked in this way are known as  *dirty*  .</span></span> <span data-ttu-id="7f8ff-134">すべての直接的および間接的な依存関係はダーティとマークされては A1、B1、C1 は、A1 が変更されたとき、B1 とは異なります。 場合は、B1 と C1 の両方がダーティとして設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-134">All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="7f8ff-p104">あるセルがそのセル自体に直接的または間接的に依存している場合は、Excel によって循環参照が検出され、ユーザーに警告が示されます。これは、通常ユーザーが修正しなければならないエラー状態です。Excel には、ユーザーが循環依存の関係の原因を見つけられるようにする非常に役立つグラフィカルなナビゲーション ツールがあります。場合によっては、この状態を意図的に必要とすることもあります。たとえば、次の繰り返しの開始点が、前の繰り返しの結果になる反復計算の実行を必要とすることがあります。Excel は、[計算方法の設定] ダイアログ ボックスによる反復計算の制御をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p104">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user. This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency. In some cases, you might deliberately want this condition to exist. For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration. Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="7f8ff-p105">セルにダーティのマークを付けた後、次回の再計算が実行されるときに、Excel は、それぞれのダーティ セルの内容を計算チェーンで指定された順序で再評価します。前述の例では、最初に B1、次に C1 の順になります。この再計算は、再計算モードが自動になっている場合には、Excel がセルにダーティのマークを付け終わった直後に実行されます。それ以外の場合は、再計算は後で実行されます。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p105">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain. In the example given earlier, this means B1 is first, and then C1. This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="7f8ff-p106">Microsoft Excel 2002 �ȍ~�� Microsoft Visual Basic for Applications (VBA) �� **Range** �I�u�W�F�N�g�́A�Z���Ɍv�Z���K�v�Ƃ����}�[�N��t���� **Range.Dirty** ���\�b�h��T�|�[�g���Ă��܂��B���̃��\�b�h�� **Range.Calculate** ���\�b�h�ƕ��p����� (���̃Z�N�V������Q��)�A����͈͓̔�̃Z��������I�ɍČv�Z�ł���悤�ɂȂ�܂��B����́A�v�Z���[�h���蓮�ɐݒ肳��Ă���Ƃ��ɁA�}�N���Ō���I�Ȍv�Z����s����ۂɁA���̃}�N���֐��Ƃ͖��֌W�̃Z����v�Z����I�[�o�[�w�b�h������邽�߂ɖ𗧂��܂��B�͈͌v�Z�̃��\�b�h�́AC API �ł͎g�p�ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p106">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation. When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range. This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function. Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="7f8ff-p107">Excel 2002 �ȑO�̃o�[�W������ Excel �ł́A�J���Ă���e�u�b�N�̃��[�N�V�[�g���ƂɌv�Z�\`�F�[����\�z���Ă��܂����B���̂��߁A��������郏�[�N�V�[�g�Ԃ̃����N���@�͕��G�ɂȂ�A�����I�ȍČv�Z�̂��߂ɂ͒��ӂ��K�v�ł����B���� Excel 2000 �ł́A���[�N�V�[�g�Ԃ̈ˑ��֌W��ŏ����ɂ��āA���[�N�V�[�g�ɃA���t�@�x�b�g���̖��O��t����K�v������܂��B���̂悤�ɂ��āA���̃V�[�g�Ɉˑ�����V�[�g���A�ˑ���̃V�[�g�̌�� (�A���t�@�x�b�g��) �Ȃ�悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p107">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook. This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation. In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="7f8ff-150">Excel 2007 では、計算チェーンのセクションが相互に依存していないし、同時に計算することができますように、複数のスレッドで再計算を有効にするロジックが改良されました。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-150">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time.</span></span> <span data-ttu-id="7f8ff-151">マルチプロセッサまたはマルチコア コンピューターで、シングル プロセッサ コンピューター上の複数のスレッドまたは 1 つのスレッドを使用するを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-151">You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="7f8ff-152">�񓯊��̃��[�U�[��\`�֐� (UDF)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="7f8ff-p109">�v�Z���ɔ񓯊��� UDF �������ƁA���݂̐����̏�Ԃ��ۑ�����AUDF ���J�n����āA�c��̃Z���̕]�������s����܂��B�v�Z�ł��ׂẴZ���̕]�����I�������Ƃ��ɁA�܂����s���̔񓯊��֐�������ꍇ�AExcel �͔񓯊��֐�����������܂őҋ@���܂��B�e�񓯊��֐������ʂ�񍐂����Ƃ��ɁAExcel �͐�����I�����āA�񓯊��֐��ւ̎Q�Ƃ�܂ރZ����g�p���Ă���Z���̍Čv�Z�̂��߂ɐV�����v�Z�p�X����s���܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p109">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells. When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running. As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="7f8ff-156">�������֐��Ɣ�������֐�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="7f8ff-p110">Excel �ł́A�������֐��̊T�O��T�|�[�g���Ă��܂��B����́A���̊֐��̈������ύX����Ă��Ȃ��Ă� (�֐�����������ꍇ)�A����u�ԂƎ��̏u�Ԃł͒l���قȂ�\��������ƌ��Ȃ����֐��ł��BExcel �́A�Čv�Z�̂��тɁA�������֐����܂܂�Ă���Z������ׂĂ̎Q�Ɛ�Ƌ��ɍĕ]�����܂��B���̂��߁A�������֐��Ɉˑ��������Ă���ƁA�Čv�Z�ɂ����鎞�Ԃ������Ȃ�\��������܂��B�T���߂Ɏg�p����悤�ɂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p110">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed. Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates. For this reason, too much reliance on volatile functions can make recalculation times slow. Use them sparingly.</span></span>
  
<span data-ttu-id="7f8ff-161">���Ɏ��� Excel �֐��͊������ł��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="7f8ff-162">**NOW**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-162">**NOW**</span></span>
    
- <span data-ttu-id="7f8ff-163">**TODAY**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-163">**TODAY**</span></span>
    
- <span data-ttu-id="7f8ff-164">**乱数**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="7f8ff-165">**OFFSET**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-165">**OFFSET**</span></span>
    
- <span data-ttu-id="7f8ff-166">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="7f8ff-167">**INFO** (�����ɂ���ĈقȂ�܂�)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="7f8ff-168">**CELL** (�����ɂ���ĈقȂ�܂�)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="7f8ff-169">**SUMIF**(引数によって異なります)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="7f8ff-p111">VBA �� C API �́A�������Ƃ��ď�������K�v�̂��郆�[�U�[��\`�Ԑ� (UDF) �ɂ��� Excel �ɒʒm�����i��T�|�[�g���Ă��܂��BVBA ��g�p����ꍇ�́A���̂悤�ɂ���� UDF ���������Ƃ��Đ邳��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p111">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile. By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="7f8ff-p112">����ł́AExcel �� VBA �� UDF ���������ł���ƌ��Ȃ��܂��BExcel �́AUDF �̍ŏ��̌Ăяo�����ɁA���� UDF ���������ł��邱�Ƃ�F�����܂��B���̗�̂悤�ɁA������ UDF �͔�������ɖ߂����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p112">By default, Excel assumes that VBA UDFs are not volatile. Excel only learns that a UDF is volatile when it first calls it. A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="7f8ff-p113">C API ��g�p����ꍇ�́AXLL �֐���ŏ��̌Ăяo���O�Ɋ������Ƃ��ēo�^�ł��܂��B�܂��A���[�N�V�[�g�֐��̊�������Ԃ̃I��/�I�t��؂�ւ��邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p113">Using the C API, you can register an XLL function as volatile before its first call. It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="7f8ff-p114">����ł́AExcel �͔͈͈�����󂯎��A�}�N�� �V�[�g�Ɠ����̂�̂Ƃ��Đ錾���ꂽ XLL UDF ��������Ƃ��ď������܂��B���̊���̏�Ԃ́AUDF ���ŏ��ɌĂяo�����Ƃ��� **xlfVolatile** �֐���g�p���邱�ƂŃI�t�ɂł��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p114">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile. You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="7f8ff-179">�v�Z���[�h�A�R�}���h�A�I��I�ȍČv�Z�A����уf�[�^ �e�[�u��</span><span class="sxs-lookup"><span data-stu-id="7f8ff-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="7f8ff-180">Excel �ɂ� 3 �̌v�Z���[�h������܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="7f8ff-181">����</span><span class="sxs-lookup"><span data-stu-id="7f8ff-181">Automatic</span></span>
    
- <span data-ttu-id="7f8ff-182">�e�[�u���ȊO����</span><span class="sxs-lookup"><span data-stu-id="7f8ff-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="7f8ff-183">�蓮</span><span class="sxs-lookup"><span data-stu-id="7f8ff-183">Manual</span></span>
    
<span data-ttu-id="7f8ff-p115">�v�Z�������ɐݒ肳��Ă���ƁA�f�[�^���͂̌�ɍČv�Z��������s����܂��B�܂��A�O�̃Z�N�V�����ŗ��������悤�ɁA����̃C�x���g�̌�ɂ�Čv�Z���������܂��B���ɋ���ȃu�b�N�̏ꍇ�A�Čv�Z�ɒ������Ԃ�������悤�ɂȂ�A���̎��Ԃ����������ꍇ�̓��[�U�[�ɂ�鐧�����K�v�ɂȂ�܂��B�܂�A�Čv�Z�͕K�v�ȂƂ��ɂ̂ݍs���Ƃ������Ƃł��B�����\�ɂ��邽�߂ɁAExcel �ł͎蓮���[�h��T�|�[�g���Ă��܂��B���[�U�[�́AExcel �̃��j���[ �V�X�e�����烂�[�h��I����邱�Ƃ�AVBA�ACOM�A�܂��� C API ��g�p���邱�ƂŁA�v���O�����ɂ���ă��[�h��I����邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p115">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section. For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to. To enable this, Excel supports the manual mode. The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="7f8ff-p116">�f�[�^ �e�[�u���Ƃ́A���[�N�V�[�g��̓���ȍ\���̂��Ƃł��B�ŏ��ɁA���[�U�[�͌��ʂ̌v�Z����[�N�V�[�g�ɃZ�b�g �A�b�v���܂��B����́A1 �܂��� 2 �̃L�[�ɂȂ�ύX�\�ȓ��͂ƁA���̑��̃p�����[�^�[�ɂ���Č��܂�܂��B���ɁA���[�U�[�͈���܂��͗����̃L�[�ɂȂ���͂̒l�̃Z�b�g�ɑ΂��錋�ʂ̃e�[�u����쐬���܂��B�e�[�u���̍쐬�ɂ́A **�f�[�^ �e�[�u�� �E�B�U�[�h**��g�p���܂��B�e�[�u���̃Z�b�g �A�b�v��AExcel �͓��͂� 1 ���v�Z�ɑg�ݍ���ŁA���ʂ̒l��e�[�u���ɃR�s�[���܂��B1 �܂��� 2 �̓��͂��g�p�ł��邽�߁A�f�[�^ �e�[�u���� 1 �����܂��� 2 �����ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p116">Data tables are special structures in a worksheet. First, the user sets up the calculation of a result on a worksheet. This depends on one or two key changeable inputs and other parameters. The user can then create a table of results for a set of values for one or both of the key inputs. The table is created by using the **Data Table Wizard**. After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table. As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="7f8ff-195">�f�[�^ �e�[�u���̍Čv�Z�̏������@�͎኱�قȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="7f8ff-196">�Čv�Z�́A�ʏ�̃u�b�N�̍Čv�Z�Ƃ͔񓯊��ɏ�������܂��B����́A����ȃe�[�u���̍Čv�Z�ɂ́A�u�b�N�̎c��̕���������Ԃ������邱�Ƃ����邽�߂ł��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="7f8ff-p117">�z�Q�Ƃ����e����Ă��܂��B���ʂ𓾂邽�߂Ɏg�p�����v�Z���f�[�^ �e�[�u���� 1 �܂��� 2 �̒l�Ɉˑ�����ꍇ�AExcel �͏z�ˑ��̊֌W�Ɋւ���G���[��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p117">Circular references are tolerated. If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="7f8ff-p118">Excel ���f�[�^ �e�[�u���̍Čv�Z��ʂ̕��@�ŏ������邱�ƂƁA���G�Ȍv�Z�܂��͔��ɒ����v�Z�Ɉˑ����鋐��ȃe�[�u���̌v�Z�ɂ͎��Ԃ�������Ƃ�����������AExcel �ł̓f�[�^ �e�[�u���̎����v�Z�𖳌����ł���悤�ɂȂ��Ă��܂��B�����s���ɂ́A�v�Z���[�h�� [�f�[�^ �e�[�u���ȊO����] �ɐݒ肵�܂��B�v�Z�����̃��[�h�̂Ƃ��ɂ́A���[�U�[�� F9 ��������A����Ɠ����̃v���O�����ɂ�鑀�����s���邱�ƂŁA�f�[�^ �e�[�u�����Čv�Z����܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p118">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables. To do this, set the calculation mode to Automatic except Data Tables. When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="7f8ff-p119">Excel �́A�Čv�Z���[�h�̕ύX�ƍČv�Z�̐���ɗ��p�ł��郁�\�b�h����J���Ă��܂��B����ɊY�����郁�\�b�h�́A�o�[�W�������i�ނ��Ƃɉ��P����Ă��āA���ׂ������䂪�\�ɂȂ��Ă��܂��B����Ɋ֘A���� C API �̋@�\�́AExcel �o�[�W���� 5 �Ŏg�p�\��������̂𔽉f���Ă��邽�߁A�������V���� VBA ��g�p���邱�Ƃœ������̂Ɠ�������͓����܂���B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p119">Excel exposes methods through which you can alter the recalculation mode and control recalculation. These methods have been improved from version to version to allow for finer control. The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="7f8ff-205">Excel ���蓮�v�Z���[�h�̂Ƃ��ɍł�p�ɂɎg�p����郁�\�b�h�́A�u�b�N�A���[�N�V�[�g�A����є͈͂̑I��I�Ȍv�Z��\�ɂ��郁�\�b�h�A�J���Ă��邷�ׂẴu�b�N�̊��S�ȍČv�Z��\�ɂ��郁�\�b�h�A����Ɉˑ��֌W�c���[�ƌv�Z�\`�F�[���̊��S�ȍč\�z��\�ɂ��郁�\�b�h�ł��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="7f8ff-206">�͈͌v�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-206">Range Calculation</span></span>

<span data-ttu-id="7f8ff-207">�L�[�{�[�h����: �Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-207">Keystroke: None</span></span>
  
<span data-ttu-id="7f8ff-208">VBA: **Range.Calculate** (Excel 2000 �œ�������AExcel 2007 �ŕύX����Ă��܂�) ����� **Range.CalculateRowMajorOrder** (Excel 2007 �œ�������܂���)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="7f8ff-209">C API: �T�|�[�g�Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-209">C API: Not supported</span></span>
  
- <span data-ttu-id="7f8ff-210">**[�蓮] ���[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-210">**Manual mode**</span></span>
    
    <span data-ttu-id="7f8ff-p120">����͈͓̔�̃Z���݂̂�Čv�Z���܂� (�Z�����_�[�e�B���ǂ����͊֌W����܂���)�B **Range.Calculate** ���\�b�h�̓���� Excel 2007 �ŕύX����Ă��܂��B�������A�ȑO�̓���� **Range.CalculateRowMajorOrder** ���\�b�h�ŃT�|�[�g����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p120">Recalculates just the cells in the given range regardless of whether they are dirty or not. Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="7f8ff-213">**[����] �܂��� [�e�[�u���ȊO����] ���[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="7f8ff-214">�u�b�N��Čv�Z���܂����A�͈͂̍Čv�Z�܂��͔͈͂Ɋ܂܂��Z���̍Čv�Z��������܂���B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="7f8ff-215">�A�N�e�B�u�ȃ��[�N�V�[�g�̌v�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="7f8ff-216">�L�[�{�[�h����: SHIFT + F9</span><span class="sxs-lookup"><span data-stu-id="7f8ff-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="7f8ff-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="7f8ff-218">C API: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="7f8ff-219">**���ׂẴ��[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-219">**All modes**</span></span>
    
    <span data-ttu-id="7f8ff-220">�A�N�e�B�u�ȃ��[�N�V�[�g��ł̂݁A�v�Z�̃}�[�N���t�����Ă���Z����Čv�Z���܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="7f8ff-221">�w�肳�ꂽ���[�N�V�[�g�̌v�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="7f8ff-222">�L�[�{�[�h����: �Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-222">Keystroke: None</span></span>
  
<span data-ttu-id="7f8ff-223">VBA: **Worksheets(** �Q�� **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="7f8ff-224">C API: �T�|�[�g�Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-224">C API: Not supported</span></span>
  
- <span data-ttu-id="7f8ff-225">**���ׂẴ��[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-225">**All modes**</span></span>
    
    <span data-ttu-id="7f8ff-p121">�w�肳�ꂽ���[�N�V�[�g��ł̂݁A�_�[�e�B�ȃZ���Ƃ��̃Z���̎Q�Ɛ��Čv�Z���܂��B�Q�Ƃ͕�����Ƃ��Ẵ��[�N�V�[�g�̖��O�A�܂��͊֘A����u�b�N�̃C���f�b�N�X�ԍ��ł��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p121">Recalculates the dirty cells and their dependents within the specified worksheet only. Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="7f8ff-p122">Excel 2000 �ȍ~�̃o�[�W�����ł́A **Boolean** ���[�N�V�[�g �v���p�e�B�� **EnableCalculation** �v���p�e�B�����J����Ă��܂��B����� **False** ���� **True** �ɐݒ肷��ƁA�w�肳�ꂽ���[�N�V�[�g��̂��ׂẴZ�����_�[�e�B�ɂȂ�܂��B�������[�h�̏ꍇ�́A����ɂ��u�b�N�S�̂̍Čv�Z��g���K�[����܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p122">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property. Setting this to **True** from **False** dirties all cells in the specified worksheet. In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="7f8ff-231">�蓮���[�h�̏ꍇ�́A���̃R�[�h�ŃA�N�e�B�u �V�[�g�݂̂̍Čv�Z���s���܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="7f8ff-232">�u�b�N�̃c���[�̍č\�z�ƍČv�Z�̋���</span><span class="sxs-lookup"><span data-stu-id="7f8ff-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="7f8ff-233">�L�[�{�[�h����: CTRL + ALT + SHIFT + F9 (Excel 2002 �œ�������܂���)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="7f8ff-234">VBA: **Workbooks(** �Q�� **).ForceFullCalculation** (Excel 2007 �œ�������܂���)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="7f8ff-235">C API: �T�|�[�g�Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-235">C API: Not supported</span></span>
  
- <span data-ttu-id="7f8ff-236">**���ׂẴ��[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-236">**All modes**</span></span>
    
    <span data-ttu-id="7f8ff-237">Excel �ɂ���ē���̃u�b�N�̈ˑ��֌W�c���[�ƌv�Z�\`�F�[�����č\�z����A������܂�ł��邷�ׂẴZ���̍Čv�Z��������܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="7f8ff-238">�J���Ă��邷�ׂẴu�b�N</span><span class="sxs-lookup"><span data-stu-id="7f8ff-238">All Open Workbooks</span></span>

<span data-ttu-id="7f8ff-239">�L�[�{�[�h����: F9</span><span class="sxs-lookup"><span data-stu-id="7f8ff-239">Keystroke: F9</span></span>
  
<span data-ttu-id="7f8ff-240">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="7f8ff-241">C API: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="7f8ff-242">**���ׂẴ��[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-242">**All modes**</span></span>
    
    <span data-ttu-id="7f8ff-p123">Excel によってダーティのマークが付けられたすべてのセル (揮発性データと変更されたデータの参照先、およびプログラムによりダーティのマークが付けられたセル) を再計算します。計算モードが [テーブル以外自動] の場合は、更新を必要とするテーブルに加えて、すべての揮発性関数とその関数の参照先も生産します。</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p123">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty. If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="7f8ff-245">�J���Ă��邷�ׂẴu�b�N�̃c���[�̍č\�z�ƌv�Z�̋���</span><span class="sxs-lookup"><span data-stu-id="7f8ff-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="7f8ff-246">�L�[�{�[�h����: CTRL + ALT + F9</span><span class="sxs-lookup"><span data-stu-id="7f8ff-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="7f8ff-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="7f8ff-248">C API: �T�|�[�g�Ȃ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-248">C API: Not supported</span></span>
  
- <span data-ttu-id="7f8ff-249">**���ׂẴ��[�h**</span><span class="sxs-lookup"><span data-stu-id="7f8ff-249">**All modes**</span></span>
    
    <span data-ttu-id="7f8ff-p124">�J���Ă��邷�ׂẴu�b�N�Ɋ܂܂�邷�ׂẴZ����Čv�Z���܂��B�v�Z���[�h�� [�e�[�u���ȊO����] �̏ꍇ�́A�e�[�u���̍Čv�Z��������܂��B</span><span class="sxs-lookup"><span data-stu-id="7f8ff-p124">Recalculates all cells in all open workbooks. If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f8ff-252">�֘A����</span><span class="sxs-lookup"><span data-stu-id="7f8ff-252">See also</span></span>



[<span data-ttu-id="7f8ff-253">Excel �ł̃}���\`�X���b�h�Čv�Z</span><span class="sxs-lookup"><span data-stu-id="7f8ff-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
<span data-ttu-id="7f8ff-254">[Excel �Ŏg�p�����f�[�^�^](data-types-used-by-excel.md)</span><span class="sxs-lookup"><span data-stu-id="7f8ff-254">[Data Types Used by Excel](data-types-used-by-excel.md)</span></span>
  
[<span data-ttu-id="7f8ff-255">Excel �̃������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="7f8ff-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="7f8ff-256">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="7f8ff-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

