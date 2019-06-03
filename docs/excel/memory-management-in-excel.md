---
title: Excel のメモリ管理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 メモリ[Excel 2007]、Excel によるメモリ管理、Excel スタック、文字列[Excel 2007]、メモリ管理、Excel によるメモリ管理、XLOPER メモリ[Excel 2007]、メモリ[Excel 2007]、管理ガイドライン
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419542"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="e17d7-104">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="e17d7-104">Memory Management in Excel</span></span>

 <span data-ttu-id="e17d7-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e17d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e17d7-p101">効率的で安定した XLL を作成する場合には、メモリ管理が最も重要な課題となります。メモリを管理できないと Microsoft Excel で様々な問題が生じる可能性があります。たとえば、メモリ割り当てや初期化の効率が悪くなったり、小規模なメモリ リークが生じたりするといった比較的小さな問題から、Excel が不安定になるといった大きな問題などが起こる原因となります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="e17d7-p102">メモリの管理ミスは、アドイン関連の深刻な問題の最も一般的な原因です。したがって、メモリ管理に関して一貫性のあるよく考え抜かれた戦略でプロジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="e17d7-p103">Microsoft Office Excel 2007 では、マルチスレッドでのワークブック再計算が導入され、メモリ管理がより複雑になりました。スレッドセーフワークシート関数を作成、エクスポートする場合は、複数のスレッドのアクセスが集中したときに発生する可能性がある競合を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="e17d7-112">次の 3 つのデータ構造型に関してメモリの留意事項があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="e17d7-113">**XLOPER**および**XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="e17d7-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="e17d7-114">**XLOPER**または**XLOPER12**にない文字列</span><span class="sxs-lookup"><span data-stu-id="e17d7-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="e17d7-115">**FP**および**FP12**配列</span><span class="sxs-lookup"><span data-stu-id="e17d7-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="e17d7-116">XLOPER/XLOPER12 メモリ</span><span class="sxs-lookup"><span data-stu-id="e17d7-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="e17d7-117">**XLOPER**/ **XLOPER12**データ構造には、メモリブロックへのポインタを含むサブタイプ、つまり文字列（**xltypeStr**）、配列（**xltypeMulti**）、 および外部参照（**xltypeRef**）があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-117">The XLOPER/XLOPER12 data structure has a few sub-types that contain pointers to blocks of memory, namely strings (xltypeStr), arrays (xltypeMulti) and external references (xltypeRef).</span></span> <span data-ttu-id="e17d7-118">**xltypeMulti**配列には、文字列\*\*XLOPER \*\*/ **XLOPER12s**を含めることができ、これがさらに他のメモリブロックを指すこともできます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-118">Note also that xltypeMulti arrays can contain string XLOPER/XLOPER12s that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="e17d7-119">**XLOPER**/ **XLOPER12**は、いくつかの方法によって作成できます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="e17d7-120">Excel によって。XLL 関数に渡される引数を準備するとき</span><span class="sxs-lookup"><span data-stu-id="e17d7-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="e17d7-121">Excel によって。C API 呼び出しで**XLOPER**または**XLOPER12**を返すとき</span><span class="sxs-lookup"><span data-stu-id="e17d7-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="e17d7-122">DLL によって。C API 呼び出しに渡される引数を作成するとき</span><span class="sxs-lookup"><span data-stu-id="e17d7-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="e17d7-123">DLL によって。XLL 関数の戻り値を作成するとき</span><span class="sxs-lookup"><span data-stu-id="e17d7-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="e17d7-124">いずれかのメモリ ポイント型のメモリ ブロックは、次のいくつかの方法で割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="e17d7-125">関数コード外の DLL で静的ブロックとすることができます。この場合、メモリを割り当てたり解放したりする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="e17d7-126">関数コード内の DLL で静的ブロックとすることができます。この場合、メモリを割り当てたり解放したりする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="e17d7-127">DLLによって動的に割り当てられ、解放される方法はいくつかあります。**malloc**と\*\* free**、**new**と**delete\*\*などです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="e17d7-128">Excel で動的に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="e17d7-p105">考えうる**XLOPER**/ **XLOPER12**メモリーの起点数、および**XLOPER**/ \*\* XLOPER12\*\*がそのメモリーが割り当てている状況の数を踏まえれば、この問題が非常に難しいであろうことに驚きはありません。しかしながら、いくつかの規則やガイドラインに従えば、複雑さは大幅に軽減されます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p105">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="e17d7-131">XLOPER/XLOPER12 を扱うときの規則</span><span class="sxs-lookup"><span data-stu-id="e17d7-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="e17d7-p106">XLL 関数に引数として渡される**XLOPER**/ **XLOPER12**のメモリを解放したり、上書きしたりしないでください。そのような引数は読み取り専用として扱います。詳しくは、「[Excel XLL 開発における既知の問題](known-issues-in-excel-xll-development.md)」の「引数をそのまま変更して**XLOPER**または**XLOPER12**を返す」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p106">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="e17d7-135">C API の呼び出しでDLL に返された**XLOPER**/ **XLOPER12**にExcelがメモリを割り当てた場合：</span><span class="sxs-lookup"><span data-stu-id="e17d7-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="e17d7-p107">[xlFree](xlfree.md)への呼び出しを使用して、**XLOPER**/ **XLOPER12**が不要になったら、メモリーを解放する必要があります。メモリを解放するのに、freeやdeleteなど他の方法を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p107">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="e17d7-138">返された型が**xltypeMulti**の場合、文字列が含まれていたり、また文字列で上書きしようとしている際は特に、配列内の**XLOPER**/ **XLOPER12**を上書きしないでください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="e17d7-139">DLL 関数の戻り値として**XLOPER**/ **XLOPER12**をExcel に返す場合は、完了時に解放する必要があるメモリがあることをExcel に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="e17d7-140">C API 呼び出しへの戻り値として作成された**XLOPER**/ **XLOPER12**に対してのみ、**xlFree**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-140">You must only call xlFree on an XLOPER/XLOPER12 that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="e17d7-141">DLL が、DLL 関数の戻り値としてExcel に返したい**XLOPER**/ **XLOPER12**にメモリを割り当てている場合は、そのDLL が解放すべきメモリーがあることをExcel に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="e17d7-142">メモリ管理のガイドライン</span><span class="sxs-lookup"><span data-stu-id="e17d7-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="e17d7-p108">メモリを割り当てて解放するために使用するメソッドを DLL 内で一貫させます。異なるメソッドが混在しないようにします。メモリ クラスまたは構造体で使用するメソッドをラップし、対象メソッドが使用されている多くの場所でコードを変えなくても変更できるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="e17d7-p109">DLL 内に**xltypeMulti**配列を作成するときは、文字列へのメモリ割り当て方法の一貫性を保ってください。常に動的にメモリに割り当てるか、常に静的メモリを使用してください。これによって、メモリを解放するときに、文字列を常に解放する必要があるか、あるいは解放しないべきかがわかります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="e17d7-148">Excel が作成した**XLOPER**/ **XLOPER12**をコピーするときは、Excel に割り当てられたメモリのディープコピーを作成してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="e17d7-p110">Excel が割り当てた文字列**XLOPER**/ **XLOPER12**を\*\*xltypeMulti \*\*配列内に配置しないでください。該当の文字列のディープコピーを作成し、そのコピーへのポインタを配列に格納してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p110">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="e17d7-151">Excel が割り当てた XLOPER/XLOPER12 メモリを解放する</span><span class="sxs-lookup"><span data-stu-id="e17d7-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="e17d7-152">次のXLL コマンドを考えてみましょう。これは**xlGetName**を使用してDLL のパスとファイル名を含む文字列を取得し、**xlcAlert**を使用して警告ダイアログボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="e17d7-153">関数が**xDllName**が指すメモリーを必要としなくなった場合、DLL専用のC API 関数の1つである[xlFree関数](xlfree.md)への呼び出しを使用して解放できます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="e17d7-154">**xlFree**関数は関数参照セクションに全て記述されています（[DLL、またはXLL からのみ呼び出すことができる C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)を参照）が、以下の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="e17d7-155">**xlFree**への1回の呼び出しで、複数の**XLOPER**/ **XLOPER12**へのポインタを渡すことができます。ただし、実行中のExcelバージョン（Excel 2003では30、Excel 2007以降は255）でサポートされる関数引数の数によってのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-155">You can pass pointers to more than one XLOPER/XLOPER12s in a single call to xlFree, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in xlxlshort).</span></span>
    
- <span data-ttu-id="e17d7-p111">**xlFree**は、既に解放されている**XLOPER**/ **XLOPER12**の解放試行が安全か確かめるため、含まれているポインターを**NULL**に設定します。**xlFree**は、その引数を変更する唯一のC API 関数です。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p111">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="e17d7-158">C API への呼び出しの戻り値に使用される**XLOPER**/ **XLOPER12**の上には、メモリーへのポインターが含まれているかどうかに関係なく、**xlFree**を安全に呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-158">You can safely call xlFree on any XLOPER/XLOPER12 used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="e17d7-159">Excel で解放される XLOPER/XLOPER12 を返す</span><span class="sxs-lookup"><span data-stu-id="e17d7-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="e17d7-p112">事前のセクションのコマンド例を変更し、**Boolean\*\*\*\*true**引数、および **#N/A**その他を渡すとDLLパスとファイル名を返すワークシート関数に変更したいとします。 文字列メモリを解放するため、Excel関数に**xlFree**を呼び出すことは明らかにできません。ただし、それがある時点で解放されていない場合、アドインは関数が呼び出されるたびにメモリをリークします。この問題を回避するには、 **XLOPER**/ **XLOPER12**の**xltype**フィールドにxcall.h の**xlbitXLFree**と定義してビットを設定します。 これを設定すると、値のコピーが終了したら、返されたメモリを解放する必要があることがExcelに伝えられます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="e17d7-165">例</span><span class="sxs-lookup"><span data-stu-id="e17d7-165">Example</span></span>

<span data-ttu-id="e17d7-166">次のコード例は、XLL ワークシート関数に変換された、前のセクションの XLL コマンドを示しています。</span><span class="sxs-lookup"><span data-stu-id="e17d7-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="e17d7-p113">**XLOPER**/ **XLOPER12**を使用するXLL 関数は、**XLOPER**/ \*\* XLOPER12**へのポインタを取得して返すものとして宣言する必要があります。この例の関数内での静的**XLOPER12**の使用は、スレッドセーフではありません。この関数をスレッドセーフとして誤って登録することはできますが、**xRtnValue\*\*が別のスレッドで終了する前に1つのスレッドによって上書きされる危険があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p113">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="e17d7-p114">それを割り当てるExcel コールバックへの呼び出しの後に**xlbitXLFree**を設定する必要があります。これより前に設定した場合は、上書きされ、必要な効果を発揮しません。ワークシートに返す前に別のC API 関数の呼び出しで引数として値を使用する予定の場合は、そのような呼び出しの後にこのビットを設定する必要があります。そうしないと、**XLOPER**/ **XLLOPER12**型をチェックする前に、このビットをマスクしない関数を混同してしまうでしょう。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p114">You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="e17d7-174">DLL で解放される XLOPER/XLOPER12 を返す</span><span class="sxs-lookup"><span data-stu-id="e17d7-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="e17d7-p115">これと同様の問題は、XLL が**XLOPER**/ **XLOPER12**にメモリを割り当て、それをExcel に返したい場合に発生します。 Excel は、xlcall.hの**xlbitDLLFree**として定義される**XLOPER**/ **XLOPER12**の**xltype**フィールドに設定できる別のビットを認識します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p115">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="e17d7-p116">このビットが設定された**1 XLOPER**/ **XLOPER12**を受け取ると、Excelは[xlAutoFree](xlautofree-xlautofree12.md)という名前の、XLL によってエクスポートされるであろう関数を呼び出そうとします。  （ **XLOPER**） や **xlAutoFree12**の場合、 （**XLOPER12** の場合）。この機能については、関数リファレンス（[アドインマネージャおよびXLL インタフェース関数](add-in-manager-and-xll-interface-functions.md)を参照）で詳細に記載されていますが、ここでは最小限の実装例を示します。その目的は、 **XLOPER**/ **XLOPER12**メモリを、元々割り当てられていた方法と一致する方法で解放することです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p116">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="e17d7-180">例</span><span class="sxs-lookup"><span data-stu-id="e17d7-180">Examples</span></span>

<span data-ttu-id="e17d7-181">次の関数例は、DLL名の前に「このDLLのフルパス名は」というテキストが含まれている点を除けば、この前の関数と同じです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="e17d7-182">前の関数をエクスポートしたXLLでの**xlAutoFree12**の最低限の実装は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="e17d7-p117">この実装は、XLL が**XLOPER12**文字列のみを返し、それらの文字列が**malloc**を使用してのみ割り当てられる場合にのみ満たされます。テストは</span><span class="sxs-lookup"><span data-stu-id="e17d7-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="e17d7-185">**xlbitDLLFree**が設定されている場合、失敗することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="e17d7-186">一般に、**xlAutoFree**および**xlAutoFree12**は、XLL で作成された\*\* xltypeMulti**配列および**xltypeRef\*\*外部参照に関連付けられているメモリを解放するように実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="e17d7-187">動的に割り当てられた**XLOPER**および**XLOPER12**を返すように、XLL 関数を実装するということもできます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-187">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s.</span></span> <span data-ttu-id="e17d7-188">この場合、サブタイプに関係なく、**xlbitDLLFree**をそのような**XLOPER**および**XLOPER12**すべてに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-188">In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type.</span></span> <span data-ttu-id="e17d7-189">また、**xlAutoFree**および**xlAutoFree12**を実装して、このメモリーが解放され、**XLOPER**/ **XLOPER12**内で指定されているすべてのメモリーを解放する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-189">You would also need to implement xlAutoFree and xlAutoFree12 so that this memory was freed and also any memory pointed to within the XLOPER/XLOPER12.</span></span> <span data-ttu-id="e17d7-190">これは、戻り値をスレッド セーフにする 1 つの方法です。</span><span class="sxs-lookup"><span data-stu-id="e17d7-190">This approach is one way to make the return value thread safe.</span></span> <span data-ttu-id="e17d7-191">たとえば、前述の関数を次のように書き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-191">For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="e17d7-192">**xlAutoFree**および**xlAutoFree12**について詳しくは、[xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="e17d7-193">変更インプレース引数を返す</span><span class="sxs-lookup"><span data-stu-id="e17d7-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="e17d7-p119">Excel では、XLL 関数はインプレースで引数を変更して値を返すことができます。この操作は、ポインターとして渡された引数でのみ行うことができます。このような処理を行うには、関数を登録するときに、変更対象の引数を Excel に通知しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="e17d7-197">この方法で値を返すことは、ポインターで渡すことができるすべてのデータ型でサポートされていますが、特に以下の型で便利です。</span><span class="sxs-lookup"><span data-stu-id="e17d7-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="e17d7-198">長さが計測され、null で終了する ASCII バイト文字列</span><span class="sxs-lookup"><span data-stu-id="e17d7-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="e17d7-199">長さが計測され、null で終了する Unicode ワイド文字列（Excel 2007以降）</span><span class="sxs-lookup"><span data-stu-id="e17d7-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="e17d7-200">**FP** 浮動小数点配列</span><span class="sxs-lookup"><span data-stu-id="e17d7-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="e17d7-201">**FP12** 浮動小数点配列（Excel 2007以降）</span><span class="sxs-lookup"><span data-stu-id="e17d7-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e17d7-p120">この方法で**XLOPER**または**XLOPER12**を返さないでください。詳しくは、[Excel XLL開発における既知の問題](known-issues-in-excel-xll-development.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="e17d7-p121">単にreturn 文を使用するのではなく、この手法を使用する利点は、Excel が戻り値にメモリを割り当てることです。 Excel が返されたデータの読み取りを終了すると、メモリを解放します。これはXLL の機能からメモリ管理作業を取り除きます。この手法はスレッドセーフです。Excel によって異なるスレッドで同時に呼び出された場合、各スレッドの各関数呼び出しにはそれぞれでバッファーがあります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="e17d7-p122">**XLOPER**/ **XLOPER12**に対して存在するメモリの追返還を解放するためDLL に呼び戻すメカニズムは、単純な文字列および**FP**/ **FP12**配列には存在しないため、特に上記のデータ型の場合に役立ちます。したがって、DLL で作成された文字列または浮動小数点配列を返すときは、次の選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p122">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="e17d7-p123">永続的ポインタを動的に割り当てられたバッファに設定し、ポインタを返します。次の関数呼び出しでは、（1）ポインタがnull でないことを確認し、（2）事前の呼び出しで割り当てられたリソースを解放し、ポインタをnull にリセットし、（3）新しく割り当てられたメモリブロックへのポインタを再利用します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="e17d7-212">文字列と配列を、解放する必要がない静的バッファーに作成し、そのバッファーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="e17d7-213">引数をインプレースで変更します。その際、文字列または配列を Excel 外の領域に直接書き込みます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="e17d7-214">それ以外の場合は、**XLOPER**/ **XLOPER12**を作成し、リソースを解放するため**xlbitDLLFree**および**xlAutoFree** / \*\*xlAutoFree12 \*\*を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e17d7-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="e17d7-p124">最後の選択肢は、戻り値と同じ型の引数が渡される場合には最も簡単な方法です。覚えておきたい重要な点はバッファサイズが限られていることで、オーバーランさせないよう非常に注意しなければなりません。これを誤ると、Excelがクラッシュする可能性があります。文字列と**FP**/ **FP12**配列のバッファサイズについては次に説明します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p124">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="e17d7-219">文字列</span><span class="sxs-lookup"><span data-stu-id="e17d7-219">Strings</span></span>

<span data-ttu-id="e17d7-220">文字列のメモリ管理に関する問題が、アプリケーションとアドインが不安定になる最も一般的な原因です。文字列を処理する方法 (null 終了または長さカウント (あるいはその両方)、静的バッファーまたは動的バッファー、固定長またはほぼ無制限の長さ、オペレーティング システム管理メモリ (たとえば、OLE Bstr など)、アンマネージ文字列など) が多様なことを考慮すると、これは理解できないことではありません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="e17d7-p125">C/C++ プログラマは、null で終わる文字列には馴染みが深いです。標準Cライブラリは、そのような文字列を扱うように設計されています。コード内の静的文字列リテラルは、null で終わる文字列にコンパイルされます。別の方法として、Excelは一般的にnull で終了しない長さを数えた文字列を扱います。これらの諸事実から、文字列と文字列メモリの処理方法に関して、DLL / XLL内では明確で一貫したアプローチが必要です。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="e17d7-226">最も一般的な問題を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="e17d7-227">有効なポインターを予期し、ポインター自体の妥当性自体を検査しない、または検査できない関数に、null または無効なポインターを渡すこと。</span><span class="sxs-lookup"><span data-stu-id="e17d7-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="e17d7-228">書き込まれる文字列の長さに対してバッファーの長さをチェックしないまたはできない関数が、文字列バッファーの境界をオーバーランする。</span><span class="sxs-lookup"><span data-stu-id="e17d7-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="e17d7-229">静的文字列バッファー メモリ、または既に解放された文字列バッファー メモリ、解放する方法と一貫しない方法で割り当てられた文字列バッファー メモリを解放しようとしている。</span><span class="sxs-lookup"><span data-stu-id="e17d7-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="e17d7-230">割り当てられたものの解放されいない文字列から生じるメモリ リーク。通常、頻繁に呼び出される関数で生じます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="e17d7-231">文字列の規則</span><span class="sxs-lookup"><span data-stu-id="e17d7-231">Rules for Strings</span></span>

<span data-ttu-id="e17d7-p126">**XLOPER**/ **XLOPER**と同様に、従う規則とガイドラインがあります。ガイドラインは前のセクションで示したものと同じです。ここでの規則は、特に文字列に関する規則の拡張です。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p126">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="e17d7-235">**規則:**</span><span class="sxs-lookup"><span data-stu-id="e17d7-235">**Rules:**</span></span>
  
- <span data-ttu-id="e17d7-p127">XLL関数に引数として渡された文字列**XLOPER**/ **XLOPER12**、単純な長さ計測済み文字列またはnull で終わる文字列を、メモリーを解放したり上書きしたりしないでください。そのような引数は読み取り専用として扱います。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p127">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="e17d7-238">ExcelがC API コールバック関数の戻り値に文字列**XLOPER**/ \*\* XLOPER12**にメモリを割り当てる場合は、**xlFree**を使用して解放するか、XLL関数からExcelに返す場合は**xlbitXLFree\*\*を設定します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="e17d7-239">DLL が**XLOPER**/ **XLOPER12**に文字列バッファを動的に割り当てる場合は、終了時に割り当てた方法と一致する方法で解放するか、XLL関数からExcelに返すならば**xlbitDLLFree**を設定し**xlAutoFree**/ **xlAutoFree12**を開放します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="e17d7-p128">Excel がC API の呼び出しでDLL に返された**xltypeMulti**配列にメモリを割り当てている場合は、配列内で文字列**XLOPER**/ **XLOPER12**を上書きしないでください。そのような配列は、**xlFree**を使用して解放、またはXLL関数によって返されるならは**xlbitXLFree**を設定することによってのみ解放しなくてはいけません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p128">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="e17d7-242">サポートされる文字列型</span><span class="sxs-lookup"><span data-stu-id="e17d7-242">String Types Supported</span></span>

<span data-ttu-id="e17d7-243">**C API xltypeStr XLOPER/XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="e17d7-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="e17d7-244">**バイト文字列：** XLOPER \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e17d7-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="e17d7-245">**ワイド文字列：** XLOPER12 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e17d7-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="e17d7-246">すべてのバージョンの Excel</span><span class="sxs-lookup"><span data-stu-id="e17d7-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="e17d7-247">Excel 2007 以降</span><span class="sxs-lookup"><span data-stu-id="e17d7-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="e17d7-248">最大長：255拡張ASCIIバイト</span><span class="sxs-lookup"><span data-stu-id="e17d7-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="e17d7-249">最大長: 32,767 Unicode 文字</span><span class="sxs-lookup"><span data-stu-id="e17d7-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="e17d7-250">最初の (符号なし) バイト = 長さ</span><span class="sxs-lookup"><span data-stu-id="e17d7-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="e17d7-251">最初の Unicode 文字 = 長さ</span><span class="sxs-lookup"><span data-stu-id="e17d7-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="e17d7-252">**XLOPER**または**XLOPER12**文字列のnull 終了を想定しないでください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="e17d7-253">**C / C ++文字列**</span><span class="sxs-lookup"><span data-stu-id="e17d7-253">**C/C++ strings**</span></span>

|<span data-ttu-id="e17d7-254">**バイト文字列**</span><span class="sxs-lookup"><span data-stu-id="e17d7-254">**Byte strings**</span></span>|<span data-ttu-id="e17d7-255">**ワイド文字列**</span><span class="sxs-lookup"><span data-stu-id="e17d7-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e17d7-256">null 終了（**char** \*） "C"最大長：255拡張ASCIIバイト</span><span class="sxs-lookup"><span data-stu-id="e17d7-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="e17d7-257">null 終了（**wchar_t** \*） "C％"最大長32,767のUnicode文字</span><span class="sxs-lookup"><span data-stu-id="e17d7-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="e17d7-258">長さ計測済（**unsigned char** \*） "D"</span><span class="sxs-lookup"><span data-stu-id="e17d7-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="e17d7-259">長さ計測済（\*\*wchar_t \*\* \*） "D％"</span><span class="sxs-lookup"><span data-stu-id="e17d7-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="e17d7-260">xltypeMulti XLOPER/XLOPER12 配列内の文字列</span><span class="sxs-lookup"><span data-stu-id="e17d7-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="e17d7-p129">場合によっては、Excel はDLL / XLL で使用するための**xltypeMulti**配列を作成します。いくつかのXLM 情報関数はそのような配列を返します。たとえば、C API 関数**xlfGetWorkspace**は、引数*44*を渡されると、現在登録されているすべてのDLLプロシージャを記述する文字列を含む配列を返します。C API 関数**xlfDialogBox**は、文字列のディープコピーを含む配列引数の修正コピーを返します。おそらく、XLL で**xltypeMulti**配列に遭遇する最も一般的な状況は、配列がXLL 関数への引数として渡されたか、または範囲参照から強制された場所がこの型となっているかです。後者の場合、Excelはソースセル内の文字列のディープコピーを作成し、配列内でこれらを指します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="e17d7-p130">DLL 内の文字列を変更したい場合は、そのディープコピーを作成してください。独自の**xltypeMulti**配列を作成しているときは、その中にExcel 割り当て文字列**XLOPER**/ **XLOPER12**を配置しないでください。後でそれらが正しく解放されない、またはまったく解放されないという危険性があります。やはり、文字列のディープコピーを作成し、そのコピーへのポインタを配列に格納してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p130">Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="e17d7-271">**例**</span><span class="sxs-lookup"><span data-stu-id="e17d7-271">**Examples**</span></span>
  
<span data-ttu-id="e17d7-p131">次の関数例は、長さ計測済のUnicode 文字列の動的に割り当てられたコピーを作成します。呼び出し側は、この例で割り当てられたメモリを**delete**[]を使用して最終的に解放する必要があります。また、ソース文字列はnull で終了するとは見なされません。安全のために必要であればコピー文字列は切り捨てられ、それはnull で終了しません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="e17d7-p132">引数が文字列の場合、引数のコピーを返す次のエクスポート可能なXLL 関数に示すように、この関数は**XLOPER12**のコピーに安全に使用できます。他のすべての型は長さゼロの文字列として返されます。領域は処理されないことに注意してください 。**#VALUE!** の関数が返されます。この関数は、参照が値として渡されるように、U型の引数を取るものとして登録する必要があります。これは組み込みワークシート関数 **T()** と同じですが、**AsText**もエラーを長さゼロの文字列に変換します。このコード例では、**delete**を使用して、**xlAutoFree12**が渡されたポインターとその内容を解放すると想定しています。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p132">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="e17d7-281">変更インプレース文字列引数を返す</span><span class="sxs-lookup"><span data-stu-id="e17d7-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="e17d7-p133">型**F**、**G**、**F％**、および**G％** として登録された引数は、その場で変更ができます。Excelがこれらの型の文字列引数を準備しているとき、最大長バッファを作成します。その後、たとえこの文字列が非常に短くても、引数文字列をその中にコピーします。これにより、XLL関数はその戻り値を同じメモリに直接書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="e17d7-286">こうした型のために取り分けられるバッファー サイズは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="e17d7-287">**バイト文字列:** 256 バイト (長さカウンター (G 型) または null 終端 (F 型) を含みます)。</span><span class="sxs-lookup"><span data-stu-id="e17d7-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="e17d7-288">**Unicode 文字列:** 32,768 ワイド文字 (65,536 バイト)(長さカウンター (G% 型) または null 終端 (F% 型) を含みます)。</span><span class="sxs-lookup"><span data-stu-id="e17d7-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e17d7-p134">バッファが十分な大きさで割り当てられていることは確認できないため、そのような関数をVisual Basic for Applications（VBA）から直接呼び出すことはできません。十分に大きいバッファを明示的に渡した場合にのみ、他のDLLから安全にそのような関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="e17d7-p135">これは、標準ライブラリー関数**wcsrev**を使用して、渡されたnull で終わるワイド文字列を元に戻すXLL 関数の例です。この場合の引数は、タイプ{3 F％\*\* として登録されます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="e17d7-293">永続記憶 (バイナリ名)</span><span class="sxs-lookup"><span data-stu-id="e17d7-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="e17d7-p136">バイナリ名は定義され、バイナリのブロック、つまりワークブックと一緒に格納されている非構造化データに関連付けられます。これらは関数[xlDefineBinaryName](xldefinebinaryname.md)を使用して作成され、データは関数[xlGetBinaryName](xlgetbinaryname.md)を使用して取得されます。両方の関数は関数リファレンスにより詳細な説明がありますが（[ DLL またはXLL からしか呼び出せないC API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)を参照）、また両方とも**xltypeBigData** **XLOPER**/ **XLOPER12**を使用します。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p136">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook. They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md). Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="e17d7-297">バイナリ名の実用的な適用を制限する既知の問題については、[ Excel XLL開発における既知の問題](known-issues-in-excel-xll-development.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="e17d7-298">Excel のスタック</span><span class="sxs-lookup"><span data-stu-id="e17d7-298">Excel Stack</span></span>

<span data-ttu-id="e17d7-p137">Excel は、読み込んだすべての DLL とスタック領域を共有します。通常、スタック領域は普段の使用量よりも多く、次に取り上げるいくつかのガイドラインに従う限りは問題となることはありません。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="e17d7-p138">非常に大きな構造体をスタックの値によって関数の引数として渡さないでください。代わりにポインタまたはリファレンスを渡してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="e17d7-p139">大きな構造体をスタックに返さないでください。静的または動的に割り当てられたメモリへのポインタを返すか、またはリファレンスによって渡された引数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="e17d7-p140">関数コード内で非常に大きな自動変数構造を宣言しないでください。必要な場合は、それらを静的として宣言してください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="e17d7-p141">再帰深度が常に浅いことが確実でない限り、関数を再帰的に呼び出さないでください。代わりにループを使ってみてください。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="e17d7-p142">DLL がC API を使用してExcel に呼び戻されるとき、Excel は最初に、可能性上最悪の呼び出し方法に対して十分なスペースがスタック上にあるかどうかを確認します。十分なスペースがない可能性があると思われる場合は、たとえ実際にその特定の呼び出しに対する十分なスペースがあったとしても、呼び出しが安全であるとは言えません。この場合、呼び戻しにはコード**xlretFailed**が返されます。 C API とスタックの通常の使用では、これがC API呼び出しの失敗の原因となる可能性は低いです。</span><span class="sxs-lookup"><span data-stu-id="e17d7-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="e17d7-313">このエラーが発生する場合、または懸念する場合、あるいは原因不明のエラー発生原因としてのスタック領域の不足を解消する場合、[xlStack](xlstack.md) 関数への呼び出しでスタック領域がどれほどあるかを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="e17d7-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e17d7-314">関連項目</span><span class="sxs-lookup"><span data-stu-id="e17d7-314">See also</span></span>



[<span data-ttu-id="e17d7-315">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="e17d7-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="e17d7-316">Excel におけるマルチスレッド処理とメモリ競合</span><span class="sxs-lookup"><span data-stu-id="e17d7-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="e17d7-317">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="e17d7-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

