---
title: Excel におけるマルチスレッド処理とメモリ競合
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading in excel,memory contention in Excel,functions [Excel 2007], thread-safe,thread-safe functions [Excel 2007],thread-local memory [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384424"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="171bb-104">Excel におけるマルチスレッド処理とメモリ競合</span><span class="sxs-lookup"><span data-stu-id="171bb-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="171bb-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="171bb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="171bb-106">Excel 2007 より前の バージョンの Microsoft Excel では、すべてのワークシートの計算に 1 つのスレッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="171bb-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="171bb-107">ただし、Excel 2007 以降の Excel は、ワークシートの計算に 1 から 1024 の同時実行スレッドを使用するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="171bb-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="171bb-108">マルチプロセッサまたはマルチコアのコンピューターでは、既定のスレッド数はプロセッサまたはコアの数と同じです。</span><span class="sxs-lookup"><span data-stu-id="171bb-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="171bb-109">したがって、スレッド セーフのセル、またはスレッド セーフの関数のみを含むセルは、同時実行スレッドに割り当てることができ、前回の計算と同様に計算する必要があるという通常の再計算ロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="171bb-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="171bb-110">スレッド セーフ関数</span><span class="sxs-lookup"><span data-stu-id="171bb-110">Thread-Safe Functions</span></span>

<span data-ttu-id="171bb-p102">Excel 2007 �ȍ~�̑g�ݍ��݂̃��[�N�V�[�g���̑����́A�X���b�h �Z�[�t�ł��BXLL ����X���b�h �Z�[�t�Ƃ��ċL�q���ēo�^���邱�Ƃ�ł��܂��BExcel �́A1 �̃X���b�h (���C�� �X���b�h) ��g�p���āA���ׂẴR�}���h�A�X���b�h �A���Z�[�t���A **xlAuto** �� ( [xlAutoFree](xlautofree-xlautofree12.md) �� **xlAutoFree12** �����)�A����� COM ���� Visual Basic for Applications (VBA) ����Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p102">Most of the built-in worksheet functions starting in Excel 2007 are thread safe. You can also write and register XLL functions as being thread safe. Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="171bb-p103">XLL ���� **xlbitDLLFree** ���ݒ肳�ꂽ **XLOPER** �܂��� **XLOPER12** ��Ԃ��ꍇ�́AExcel �͂��̊��̌Ăяo�������s���ꂽ�̂Ɠ����X���b�h��g�p���� **xlAutoFree** �܂��� **xlAutoFree12** ��Ăяo���܂��B **xlAutoFree** �܂��� **xlAutoFree12** �̌Ăяo���́A���̃X���b�h�Ŏ��̊��̌Ăяo�����s����O�ɍs���܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p103">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**. The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="171bb-116">XLL 開発者にとって、スレッド セーフ関数を作成することは利点があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="171bb-117">そうすることにより、Excel でマルチプロセッサまたはマルチコア のコンピューターを最大限に活用することができます。</span><span class="sxs-lookup"><span data-stu-id="171bb-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="171bb-118">1 つのスレッドを使用して行うよりも効果的にリモート サーバーを使用できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="171bb-p104">���Ƃ��A *N*  �̃X���b�h��g�p����悤�ɍ\������Ă���V���O�� �v���Z�b�T�̃R���s���[�^�[��g�p���Ă���Ɖ��肵�܂��B���� XLL ��������Ăяo���X�v���b�h�V�[�g����s���Ă���Ɖ��肵�܂��B���� XLL ���͌Ăяo�����ƃf�[�^�̗v���܂��͌v�Z���s�̗v��������[�g �T�[�o�[�܂��̓T�[�o�[�̃N���X�^�[�ɑ��M�����̂ł��B�ˑ��W�c���[�̃g�|���W�Ɉˑ����� Excel �́A����قړ����� N ���Ăяo�����Ƃ��ł����̂Ƃ��܂��B1 �܂��͕����̃T�[�o�[���\���ɍ����܂��͕��񂵂Ď��s����Ă���ꍇ�A�X�v���b�h�V�[�g�̍Čv�Z�Ɋ|���鎞�Ԃ� N ���� 1 ��Z�k����܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p104">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads. Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers. Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously. Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="171bb-p105">�X���b�h �Z�[�t����L�q����ۂɏd�v�Ȃ��Ƃ́A���\�[�X�̋����𐳂����������邱�Ƃł��B�ʏ�A����̓������̋�����Ӗ����A���� 2 �̓_�ɕ����邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p105">The key issue in writing thread-safe functions is handling contention for resources correctly. This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="171bb-125">このスレッドでのみ使用されることが分かっているメモリの作成方法。</span><span class="sxs-lookup"><span data-stu-id="171bb-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="171bb-126">共有メモリが複数のスレッドによって必ず安全にアクセスされるようにする方法。</span><span class="sxs-lookup"><span data-stu-id="171bb-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="171bb-127">まず注意すべき点は、XLL ですべてのスレッドによってアクセス可能であるメモリと、現在実行中のスレッドによってのみアクセス可能なメモリです。</span><span class="sxs-lookup"><span data-stu-id="171bb-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="171bb-128">**���ׂẴX���b�h�ɂ���ăA�N�Z�X�\�Ȃ��**</span><span class="sxs-lookup"><span data-stu-id="171bb-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="171bb-129">関数の本体の外部にある、宣言されている変数、構造体、およびクラス。</span><span class="sxs-lookup"><span data-stu-id="171bb-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="171bb-130">関数の本体内で宣言された静的変数。</span><span class="sxs-lookup"><span data-stu-id="171bb-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="171bb-p106">������ 2 �̏ꍇ�A�������́ADLL �̂��̃C���X�^���X�p�ɍ쐬���ꂽ DLL �̃����� �u���b�N�Ɋm�ۂ���Ă��܂��B�ʂ̃A�v���P�[�V���� �C���X�^���X�� DLL ��ǂݍ��ޏꍇ�́ADLL �̂��̃C���X�^���X�̊O���ł����̃��\�[�X�̋������N���Ȃ��悤�ɁA���̃������̓Ǝ��̃R�s�[��擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p106">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL. If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="171bb-133">**���݂̃X���b�h�ɂ���Ă̂݃A�N�Z�X�\�Ȃ��**</span><span class="sxs-lookup"><span data-stu-id="171bb-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="171bb-134">関数のコード内の自動変数 (関数の引数を含む)。</span><span class="sxs-lookup"><span data-stu-id="171bb-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="171bb-135">この場合、メモリは関数呼び出しのインスタンスごとにスタックに確保されています。</span><span class="sxs-lookup"><span data-stu-id="171bb-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="171bb-p107">[!����] ���I�Ɋ��蓖�Ă�ꂽ�������͈̔͂́A�����w���|�C���^�[�͈̔͂ɂ���ĈقȂ�܂��B�|�C���^�[�����ׂẴX���b�h�ɂ���ăA�N�Z�X�\�ȏꍇ�́A����������l�ł��B�|�C���^�[�����̎����ϐ��ł���ꍇ�́A���蓖�Ă�ꂽ�������͂��̃X���b�h�ɑ��Č��ʓI�ɔ���J�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p107">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also. If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="171bb-138">1 �̃X���b�h�ɂ���Ă̂݃A�N�Z�X�\�ȃ�����:�X���b�h ���[�J�� ������</span><span class="sxs-lookup"><span data-stu-id="171bb-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="171bb-p108">���̖{����̐ÓI�ϐ������ׂẴX���b�h�ɂ���ăA�N�Z�X�\�ł���ꍇ�A������g�p������͖��炩�ɃX���b�h �Z�[�t�ł͂���܂���B1 �̃X���b�h��ɂ������ 1 �̃C���X�^���X���l��ύX���Ă���\��������A�ʂ̃X���b�h��ɂ���ʂ̃C���X�^���X�͂����܂������قȂ��̂ł���Ɖ��肵�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p108">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe. One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="171bb-141">関数内で静的変数を宣言することには 2 つの理由があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="171bb-142">静的データは、1 つの呼び出しから次の呼び出しまで維持されます。</span><span class="sxs-lookup"><span data-stu-id="171bb-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="171bb-143">静的データへのポインターは、関数によって安全に返されます。</span><span class="sxs-lookup"><span data-stu-id="171bb-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="171bb-p109">1 �ڂ̗��R�̏ꍇ�A���̂��ׂĂ̌Ăяo���ňێ�����A�Ȃ����L���ȃf�[�^ (�����炭�A�����X���b�h�ɌĂяo����邽�т� 1 ����������P���ȃJ�E���^�[�A�܂��͂��ׂĂ̌Ăяo���Ŏg�p���ƃp�t�H�[�}���X�f�[�^����W����\��) ��ێ����邱�Ƃ��ł��܂��B���́A���L�f�[�^�܂��̓f�[�^�\����ی삷����@�ł��B�����s���ɂ́A���̃Z�N�V�����Ő������N���e�B�J�� �Z�N�V������g�p���邱�Ƃ��őP�̕��@�ł��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p109">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call. The question is how to protect the shared data or data structure. This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="171bb-p110">�f�[�^�����̃X���b�h�ł̂ݎg�p�����悤�Ӑ}����Ă���ꍇ (����͗��R �P�ɊY������ꍇ������܂��B���R 2 �ɂ͏�ɊY�����܂�)�A�������Ȃ������̃X���b�h����̂݃A�N�Z�X�ł��郁������ǂ�����č쐬���邩�����ɂȂ�܂��B1 �̉����Ƃ��āA�X���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p���邱�Ƃ��������܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p110">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread. One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="171bb-149">���Ƃ��A **XLOPER** �ւ̃|�C���^�[��Ԃ�����l���Ă݂܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="171bb-p111">1 �̃X���b�h�͐ÓI **XLOPER12** ��Ԃ����Ƃ��ł��A�ʂ̃X���b�h�����̃X���b�h��㏑�����Ă��邽�߁A���̊��̓X���b�h �Z�[�t�ł͂���܂���B **XLOPER12** �� **xlAutoFree12** �ɓn�����K�v������ꍇ�A���̂悤�Ȏ��Ԃ���������\�����傫���Ȃ�܂��B1 �̉����́A **XLOPER12** ����蓖�ĂāA����ɑ���|�C���^�[��Ԃ��A **XLOPER12** ���������̂���������悤�� **xlAutoFree12** ��������邱�Ƃł��B���̃A�v���[�\`�́A�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v�Ɏ�����Ă��鑽���̊���Ŏg�p����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p111">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it. The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**. One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed. This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

<span data-ttu-id="171bb-154">このアプローチは、次のセクションで説明するアプローチよりも簡単に実装できます。次のセクションで説明するアプローチは TLS API に依存する一方でいくつかのデメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="171bb-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="171bb-155">まず、どの種類の **XLOPER**/ **XLOPER12** が返される場合でも、Excel は **xlAutoFree**/ **xlAutoFree12** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="171bb-156">次に、C API コールバック関数の呼び出しの戻り値である **XLOPER**/ **XLOPER12** を返す際に問題があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="171bb-157">**XLOPER**/ **XLOPER12** は、Excel によって解放される必要のあるメモリを指す場合がありますが、**XLOPER**/ **XLOPER12** そのものが割り当てられたのと同じ方法で解放される必要があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="171bb-158">このような **XLOPER**/ **XLOPER12** を XLL ワークシート関数の戻り値として使用する場合は、両方のポインターを適切な方法で開放する必要があることを **xlAutoFree**/ **xlAutoFree12** に通知する簡単な方法がありません。</span><span class="sxs-lookup"><span data-stu-id="171bb-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="171bb-159">(**xlbitXLFree** と **xlbitDLLFree** の両方を設定しても問題は解決されません。両方が設定された Excel での **XLOPER/XLOPER12s** の処理は定義されておらず、バージョンによって異なる可能性があるためです。) この問題は、XLL がワークシートに返す、Excel によって割り当てられたすべての **XLOPER/XLOPER12s** のディープ コピーを作成することで回避できます。</span><span class="sxs-lookup"><span data-stu-id="171bb-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="171bb-160">これらの制限を回避する解決策として、スレッド ローカル **XLOPER/XLOPER12** を設定して返すアプローチがあります。このアプローチでは、 **xlAutoFree/xlAutoFree12** が **XLOPER/XLOPER12** ポインターそのものを開放しないことが要件となります。</span><span class="sxs-lookup"><span data-stu-id="171bb-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

<span data-ttu-id="171bb-p113">���̖��́A�ǂ̂悤�ɃX���b�h ���[�J�� ��������Z�b�g�A�b�v���Ď擾���邩�ł��B�܂�A�O�̗�̊� **get_thread_local_xloper12** ��ǂ̂悤�Ɏ������邩�Ƃ������Ƃł��B����́A�X���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p���čs���܂��B�ŏ��̎菇�Ƃ��āATLS �C���f�b�N�X�� **TlsAlloc** ��g�p���� �擾���܂��B����́A�ŏI�I�� **TlsFree** �ɂ���ĉ�������K�v������܂��B�����Ƃ� **DllMain** ����ȒP�Ɏ��s�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p113">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example. This is done using the Thread Local Storage (TLS) API. The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**. Both are best accomplished from **DllMain**.</span></span>
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

<span data-ttu-id="171bb-p114">�C���f�b�N�X��擾������A���ɍs���菇�̓X���b�h���ƂɃ����� �u���b�N����蓖�Ă邱�Ƃł��B[Windows �J���̃h�L�������g](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx)�ł́A����� **DllMain** �R�[���o�b�N���� **DLL_THREAD_ATTACH** �C�x���g�ŌĂяo����邽�тɍs���A���ׂĂ� **DLL_THREAD_DETACH** ��̃�������J�����邱�Ƃ𐄏����Ă��܂��B�������A���̃A�h�o�C�X�ɏ]���ƁADLL �͍Čv�Z�Ɏg�p����Ȃ��X���b�h�ɑ��ĕs�v�ȍ�Ƃ�s�����ƂɂȂ�\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p114">After you obtain the index, the next step is to allocate a block of memory for each thread. The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**. However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="171bb-p115">���̕��@����A�ŏ��Ɏg�p����Ƃ��Ɋ��蓖�Ă���@��g�p���邱�Ƃ�����߂��܂��B�܂��A�X���b�h���ƂɊ��蓖�Ă�\�����\`����K�v������܂��B **XLOPERs** �܂��� **XLOPER12s** ��Ԃ��O�q�̗�̏ꍇ�́A���̂Ƃ���ŏ\���ł����A���ł���j�[�Y�𖞂����\����쐬���邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p115">Instead, it is better to use an allocate-on-first-use strategy. First, you need to define a structure that you want to allocate for each thread. For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="171bb-171">次の関数は、スレッド ローカル インスタンスへのポインターを取得するか、またはこれが最初の呼び出しである場合は1 つを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="171bb-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

<span data-ttu-id="171bb-172">����ŁA�X���b�h ���[�J�� **XLOPER/XLOPER12** ��������擾������@���킩��͂��ł��B�܂��A�X���b�h�� **TLS_data** �̃C���X�^���X�ւ̃|�C���^�[��擾���Ă���A���̂悤�ɂ��̓���Ɋ܂܂�Ă��� **XLOPER/XLOPER12** �ւ̃|�C���^�[��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

<span data-ttu-id="171bb-p116">Excel を実行している場合、**mtr_safe_example_1** 関数と **mtr_safe_example_2** 関数をスレッド セーフなワークシート関数として登録できます。ただし、1 つの XLL で 2 つのアプローチを組み合わせることはできません。XLL がエクスポートできるのは、**xlAutoFree** と **xlAutoFree12** のうち 1 つの実装のみです。また各メモリの戦略には異なるアプローチが必要です。**mtr_safe_example_1** の場合、**xlAutoFree/xlAutoFree12** に渡されたポインターは、そのポインターが指すデータと共に解放する必要があります。**mtr_safe_example_2** の場合は、ポインターが示すデータのみを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="171bb-p116">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel. However, you cannot mix the two approaches in one XLL. Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach. With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to. With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="171bb-p117">Windows �ɂ́A���݂̃X���b�h�̃V�X�e�����C�h�̈�ӂ� ID ��Ԃ��� **GetCurrentThreadId** �����܂��B�����A�R�[�h��X���b�h �Z�[�t�ɂ�����R�[�h�̓����X���b�h�ŗL�ɂ����肷�邽�߂̎�i�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p117">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID. This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="171bb-180">�����̃X���b�h�ɂ���ăA�N�Z�X�\�ȃ�����:�N���e�B�J�� �Z�N�V����</span><span class="sxs-lookup"><span data-stu-id="171bb-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="171bb-p118">�N���e�B�J�� �Z�N�V������g�p���ĕ����̃X���b�h���A�N�Z�X�ł���ǂݎ��/�������݃�������ی삷��K�v������܂��B�ی삷�郁�����̃u���b�N���ƂɎw�肳�ꂽ�N���e�B�J�� �Z�N�V�������K�v�ƂȂ�܂��B������ **xlAutoOpen** ���̌Ăяo�����ɏ������ł��A�܂� **xlAutoClose** ���̌Ăяo�����ɁA���������Anull �ɐݒ肵���肷�邱�Ƃ��ł��܂��B **EnterCriticalSection** �� **LeaveCriticalSection** �̌Ăяo���̃y�A��ɕی삳�ꂽ�u���b�N�ւ̊e�A�N�Z�X��܂߂�K�v������܂��B�N���e�B�J�� �Z�N�V�����ւ̃A�N�Z�X��������̂́A��� 1 �̃X���b�h�݂̂ł��B�ȉ��ɁA **g_csSharedTable** �ƌĂ��Z�N�V�����̏������A����������A����юg�p�̗������܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p118">You should protect read/write memory that can be accessed by more than one thread using critical sections. You need a named critical section for each block of memory you want to protect. You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function. You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**. Only one thread is permitted into the critical section at any time. Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

<span data-ttu-id="171bb-p119">�������̃u���b�N��ی삷��A�����S�ȕʂ̕��@�͂����炭�A�Ǝ��� **CRITICAL_SECTION** �ƁA�����g�p���邽�߂̂��̃R���X�g���N�^�[�A�f�X�g���N�^�[�A����уA�N�Z�T�[�̃��\�b�h��܂ރN���X��쐬���邱�Ƃł��B���̃A�v���[�\`�ɂ́A **xlAutoOpen** �̎��s�̑O�ɏ��������ꂽ�� **xlAutoClose** �̌Ăяo�����ێ����ꂽ�肷��\���̂���I�u�W�F�N�g���ی삳���Ƃ������_���ǉ�����Ă��܂��B�������A���܂�ɑ����̃N���e�B�J�� �Z�N�V�������쐬����邱�Ƃ�A����ɂ�萶����I�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�ɒ��ӂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p119">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use. This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="171bb-p120">�ی삳�ꂽ�������̕����̃u���b�N�ɓ����ɃA�N�Z�X����K�v������R�[�h������ꍇ�́A�N���e�B�J�� �Z�N�V�����̊J�n�ƏI���̏�������ɐT�d�Ɍ�������K�v������܂��B���Ƃ��A���� 2 �̊��̓f�b�h���b�N��쐬����\��������܂��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p120">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited. For example, the following two functions could create a deadlock.</span></span>
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="171bb-p121">1 �̃X���b�h�̍ŏ��̊��� **g_csSharedTableA** ��J�n���A�ʂ̃X���b�h��2 �Ԗڂ̊��� **g_csSharedTableB** ��J�n����ƁA�����̃X���b�h���n���O���܂��B���̂悤�ɁA��т��������ŊJ�n���āA���̋t�̏����ŏI������̂��������A�v���[�\`�ł��B</span><span class="sxs-lookup"><span data-stu-id="171bb-p121">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang. The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="171bb-193">可能であれば、スレッド連携の観点から、次に示すように、個別のブロックにアクセスを分離することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="171bb-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="171bb-p122">�Z���Ԃ̃A�N�Z�X�v�����p�ɂɍs����ȂǁA���L���\�[�X�̋����������������Ă���ꍇ�́A�N���e�B�J�� �Z�N�V�����̃X�s���@�\�̗��p���������K�v������܂��B����́A���\�[�X�̑ҋ@�ɂ��v���Z�b�T�ւ̕��ׂ�Ȃ�ׂ����������邽�߂̎�@�ł��B�����s�����߂ɂ́A�Z�N�V�����̏��������� **InitializeCriticalSectionAndSpinCount**�A������͏���������Ă���� **SetCriticalSectionSpinCount** ��g�p���āA���\�[�X���g�p�\�ɂȂ�̂�ҋ@����O�ɃX���b�h�����[�v����񐔂�ݒ�ł��܂��B�@�@�@�@�@�@�@�@�ҋ@����ɂ̓R�X�g�������邽�߁A���̊ԂɃ��\�[�X����������ƁA�X�s���ɂ���đҋ@����͉�����܂��B�V���O�� �v���Z�b�T �V�X�e���ł́A�X�s�����͌��ʓI�ɖ�������܂����A�X�s������w�肵�Ă��Ă���ɂȂ邱�Ƃ͂���܂���B������ �q�[�v �}�l�[�W���[�Ŏg�p����X�s������ 4000 �ł��B�N���e�B�J�� �Z�N�V�����̎g�p�Ɋւ���ڍׂɂ��ẮAWindows SDK �̃h�L�������g����Q�Ƃ��������B</span><span class="sxs-lookup"><span data-stu-id="171bb-p122">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin. This is a technique that makes waiting for the resource less processor-intensive. To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available. The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime. On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm. The memory heap manager uses a spin count of 4000. For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="171bb-201">関連項目</span><span class="sxs-lookup"><span data-stu-id="171bb-201">See also</span></span>



[<span data-ttu-id="171bb-202">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="171bb-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="171bb-203">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="171bb-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="171bb-204">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="171bb-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

