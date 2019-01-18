---
title: DLL または XLL から Excel に呼び出す
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- ダイアログ ボックス [excel 2007]、excel コマンドの呼び出し、DLL [Excel 2007]、Excel への呼び出し、C API 関数への引数の引き渡し [Excel 2007]、コマンド [Excel 2007]、ダイアログ ボックスでの呼び出し、コマンド [Excel 2007]、DLL/XLL からアクセス可能、Excel4 関数 [Excel 2007]、Excel12 関数 [Excel 2007]、XLCallVer 関数 [Excel 2007]、operRes 引数 [Excel 2007]、関数 [Excel 2007]、DLL/XLL からアクセス可能、Excel12v 関数 [Excel 2007]、DLL 専用関数 [Excel 2007]、C API [Excel 2007]、引数の引き渡し、引数の数 [Excel 2007]、コマンド [Excel 2007]、インターナショナル バージョンでの呼び出し、DLL 専用コマンド [Excel 2007]、インターナショナル バージョン [Excel 2007]、関数およびコマンドの呼び出し、XLL [Excel 2007]、Excel への呼び出し、Excel 4v 関数 [Excel 2007]、xlfn 引数 [Excel 2007]、関数 [Excel 2007]、インターナショナル バージョンでの呼び出し
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726121"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="3531f-104">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="3531f-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="3531f-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3531f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3531f-p101">Microsoft Excel を使用すると、DLL は組み込みの Excel コマンド、ワークシート関数、マクロ シート関数にアクセスできます。こうしたコマンドや関数は、Visual Basic for Applications (VBA) で呼び出される DLL コマンドと関数から、および Excel によって直接呼び出される登録済み XLL コマンドと関数から使用できます。</span><span class="sxs-lookup"><span data-stu-id="3531f-p101">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions. These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="3531f-108">Excel4、Excel4v、Excel12、Excel12v 関数</span><span class="sxs-lookup"><span data-stu-id="3531f-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="3531f-109">Excel を使用すると、DLL はコールバック関数 [Excel4](excel4-excel12.md)、[Excel4v](excel4v-excel12v.md)、[Excel12](excel4-excel12.md)、[Excel12v](excel4v-excel12v.md) を介してコマンドや関数にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3531f-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="3531f-110">**Excel4** 関数と **Excel4v** 関数は、Excel バージョン 4 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="3531f-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="3531f-111">これらは **XLOPER** データ構造で動作します。</span><span class="sxs-lookup"><span data-stu-id="3531f-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="3531f-112">Excel 2007 では、新しいコールバック関数である **Excel12** と **Excel12v** が導入されました。これらは **XLOPER12** データ構造で動作します。</span><span class="sxs-lookup"><span data-stu-id="3531f-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="3531f-113">**Excel4** 関数と **Excel4v** 関数は、ライブラリ Xlcall32.lib によってエクスポートされ、DLL または XLL プロジェクトに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3531f-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="3531f-114">**Excel12** と **Excel12v** はプロジェクト内の SDK C++ source ファイル Xlcall.cpp に含めます。**XLOPER12** 構造を使用して Excel 機能にアクセスする場合は、これらの関数をプロジェクトに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3531f-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="3531f-115">以下のコードは、これら 4 つの関数の関数プロトタイプを示しています。</span><span class="sxs-lookup"><span data-stu-id="3531f-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="3531f-116">最初の 3 つの引数は同じですが、2 番目の引数が最初のペアでは **XLOPER** へのポインターで、次のペアでは **XLOPER12** へのポインターである点が異なります。</span><span class="sxs-lookup"><span data-stu-id="3531f-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="3531f-117">呼び出し規約は、**Excel4** と **Excel12** では **_cdecl** で、可変の引数リストが許可されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="3531f-118">省略記号は、**Excel4** の **XLOPER** 値、および **Excel12** の **XLOPER12** 値へのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="3531f-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="3531f-119">ポインターの数は、_count_ パラメーターの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="3531f-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="3531f-120">**すべてのバージョンの Excel**</span><span class="sxs-lookup"><span data-stu-id="3531f-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="3531f-121">**Excel 2007 以降**</span><span class="sxs-lookup"><span data-stu-id="3531f-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="3531f-p104">DLL で **Excel4**、**Excel4v**、**Excel12**、または **Excel12v** を呼び出すことができるようにするには、Excel が DLL に制御を渡す必要があります。つまり、こうした C API コールバックは、次のシナリオでのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3531f-p104">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL. This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="3531f-124">Excel が直接または VBA を介して呼び出した XLL コマンドから。</span><span class="sxs-lookup"><span data-stu-id="3531f-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="3531f-125">Excel が直接または VBA を介して呼び出した XLL ワークシート関数またはマクロ シート関数から。</span><span class="sxs-lookup"><span data-stu-id="3531f-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="3531f-126">次のシナリオでは、Excel C API を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="3531f-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="3531f-127">オペレーティング システム イベントから (たとえば、[DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) 関数から)。</span><span class="sxs-lookup"><span data-stu-id="3531f-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="3531f-128">DLL が作成したバックグラウンド スレッドから。</span><span class="sxs-lookup"><span data-stu-id="3531f-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="3531f-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="3531f-129">Return values</span></span>

<span data-ttu-id="3531f-p105">これら 4 つの関数はいずれも整数値を返します。この値によって、呼び出し元に対して、関数またはコマンドが正常に呼び出されたかどうかが知らされます。次のいずれかの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-p105">All four of these functions return an integer value that informs the caller whether the function or command was called successfully. The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="3531f-132">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="3531f-132">**Return value**</span></span>|<span data-ttu-id="3531f-133">**Xlcall.h での定義**</span><span class="sxs-lookup"><span data-stu-id="3531f-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="3531f-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="3531f-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3531f-135">0</span><span class="sxs-lookup"><span data-stu-id="3531f-135">0</span></span>  <br/> |<span data-ttu-id="3531f-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="3531f-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="3531f-p106">関数またはコマンドが正常に実行されました。これは、エラーなく実行されたことを意味するわけではありません。たとえば、**Excel4** は、**FIND** 関数を呼び出して検索テキストが見つからないために **#VALUE!** に評価される場合であっても、**xlretSuccess** を返すことがあります。返される **XLOPER/XLOPER12** の型と値についてはこの可能性を考慮して検証しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3531f-p106">The function or command executed successfully. This does not mean that the execution was error free. For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!** because the search text could not be found. You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.  </span></span><br/> |
|<span data-ttu-id="3531f-142">1</span><span class="sxs-lookup"><span data-stu-id="3531f-142">1</span></span>  <br/> |<span data-ttu-id="3531f-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="3531f-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="3531f-144">コマンド マクロは、ユーザーが **[キャンセル]** ボタンをクリックしたか、Esc キーを押したために停止しました。</span><span class="sxs-lookup"><span data-stu-id="3531f-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="3531f-145">2</span><span class="sxs-lookup"><span data-stu-id="3531f-145">2</span></span>  <br/> |<span data-ttu-id="3531f-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="3531f-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="3531f-p107">指定された関数コードまたはコマンド コードが無効です。このエラーは、呼び出し元の関数に関数またはコマンドを呼び出すアクセス許可がない場合に生じます。たとえば、ワークシート関数は、マクロ シート情報関数またはコマンド関数を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="3531f-p107">The supplied function or command code is not valid. This error can occur when the calling function does not have permission to call the function or command. For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="3531f-150">4</span><span class="sxs-lookup"><span data-stu-id="3531f-150">4</span></span>  <br/> |<span data-ttu-id="3531f-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="3531f-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="3531f-152">呼び出しで指定した引数の数が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="3531f-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="3531f-153">8</span><span class="sxs-lookup"><span data-stu-id="3531f-153">8</span></span>  <br/> |<span data-ttu-id="3531f-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="3531f-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="3531f-155">1 つ以上の引数の **XLOPER** 値または **XLOPER12** 値の形式が正しくないか、誤って入力されています。</span><span class="sxs-lookup"><span data-stu-id="3531f-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="3531f-156">16</span><span class="sxs-lookup"><span data-stu-id="3531f-156">16</span></span>  <br/> |<span data-ttu-id="3531f-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="3531f-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="3531f-158">Excel によって、操作でスタックがオーバーフローするリスクが検出され、関数が呼び出されませんでした。</span><span class="sxs-lookup"><span data-stu-id="3531f-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="3531f-159">32</span><span class="sxs-lookup"><span data-stu-id="3531f-159">32</span></span>  <br/> |<span data-ttu-id="3531f-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="3531f-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="3531f-p108">コマンドまたは関数が、他のいずれの戻り値によっても記述されていない理由によって失敗しました。たとえば、あまりにも大量のメモリを必要とする操作はこのエラーで失敗します。[xlCoerce](xlcoerce.md) 関数を使用して、**xltypeMulti** 配列にとても大きな参照を変換しようとすると生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3531f-p108">The command or function failed for a reason not described by one of the other return values. An operation that would require too much memory, for example, would fail with this error. This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.  </span></span><br/> |
|<span data-ttu-id="3531f-164">64</span><span class="sxs-lookup"><span data-stu-id="3531f-164">64</span></span>  <br/> |<span data-ttu-id="3531f-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="3531f-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="3531f-p109">計算されていないセルの値を取得しようとする操作が行われました。Excel で再計算整合性を保持するため、ワークシート関数ではこれを行うことができません。ただし、マクロ シート関数として登録された XLL コマンドおよび関数は、計算されていないセル値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3531f-p109">The operation attempted to retrieve the value of an uncalculated cell. To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this. However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="3531f-169">128</span><span class="sxs-lookup"><span data-stu-id="3531f-169">128</span></span>  <br/> |<span data-ttu-id="3531f-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="3531f-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="3531f-171">(Excel 2007 以降) スレッド セーフとして登録されている XLL ワークシート関数が、スレッド セーフではない C API 関数を呼び出そうとしました。</span><span class="sxs-lookup"><span data-stu-id="3531f-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="3531f-172">たとえば、スレッド セーフ関数が XLM 関数 **xlfGetCell** を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="3531f-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="3531f-173">256</span><span class="sxs-lookup"><span data-stu-id="3531f-173">256</span></span>  <br/> |<span data-ttu-id="3531f-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="3531f-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="3531f-175">(Excel 2010 以降) 非同期関数ハンドルが無効です。</span><span class="sxs-lookup"><span data-stu-id="3531f-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="3531f-176">512</span><span class="sxs-lookup"><span data-stu-id="3531f-176">512</span></span>  <br/> |<span data-ttu-id="3531f-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="3531f-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="3531f-178">(Excel 2010 以降) クラスターでは、呼び出しはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3531f-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="3531f-p111">関数がこの表のいずれかのエラー値を返す場合 (つまり、**xlretSuccess** を返さない場合)、**XLOPER** または **XLOPER12** 戻り値も **#VALUE!** に設定されます。場合によっては、この値をチェックするだけで成功を十分に確認できますが、呼び出しでは **xlretSuccess** と **#VALUE!** の両方が返る可能性を銘記しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3531f-p111">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**. In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="3531f-181">C API への呼び出し結果が **xlretUncalced** または **xlretAbort** となる場合、DLL コードまたは XLL コードは、他の C API 呼び出し ([xlfree](xlfree.md) 関数を呼び出して、**XLOPER** 値と **XLOPER12** 値で Excel によって割り当てられたメモリ リソースをリリースする場合以外) を行う前に制御を Excel に返さなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3531f-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="3531f-182">コマンドまたは関数の列挙型引数: xlfn</span><span class="sxs-lookup"><span data-stu-id="3531f-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="3531f-183">_xlfn_ 引数は、コールバック関数への最初の引数で、32 ビット符号付き整数です。</span><span class="sxs-lookup"><span data-stu-id="3531f-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="3531f-184">値は、以下の例に示されているように、SDK ヘッダー ファイル Xlcall.h で定義されている関数またはコマンドの列挙型のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3531f-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="3531f-185">すべてのワークシート関数とマクロ シート関数は、0 (**xlfCount**) から 0x0fff 16 進数までの範囲内です。Excel 2013 で割り当てられている最大値は 547 (10 進数)、0x0223 (16 進数) (**xlfFloor_precise**) です。</span><span class="sxs-lookup"><span data-stu-id="3531f-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="3531f-186">すべてのコマンド関数は、0x8000 の 16 進数 (**xlcBeep**) から 0x8fff の 16 進数までの範囲内です。Excel 2013 で割り当てられている最大値は 0x8328 の 16 進数 (**xlcHideallInkannots**) です。</span><span class="sxs-lookup"><span data-stu-id="3531f-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="3531f-187">これらは、ヘッダー ファイルで `(n | xlCommand)` として定義されます。`n` は 0 以上の 10 進数で、**xlCommand** は 0x8000 の 16 進数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="3531f-188">ダイアログ ボックスを使用した Excel コマンドの起動</span><span class="sxs-lookup"><span data-stu-id="3531f-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="3531f-p114">一部のコマンド コードは、ダイアログ ボックスを使用する Excel での操作に対応しています。たとえば、**xlcFileDelete** は 1 つの引数 (ファイル名またはマスク) を取ります。ダイアログ ボックスを使用して起動し、ユーザーが削除操作をキャンセルしたり変更したりする機会を提供できます。また、ダイアログ ボックスを使用せずに呼び出すこともできます。その場合には、ファイルの削除が、ファイルが存在し、呼び出し元にアクセス許可があるという前提で、追加のやり取りなしで行われます。こうしたコマンドをダイアログ ボックス形式で呼び出すには、コマンド列挙型を、0x1000 のビット単位の OR 演算で結合する必要があります (**xlPrompt**)。</span><span class="sxs-lookup"><span data-stu-id="3531f-p114">Some of the command codes correspond to actions in Excel that use dialog boxes. For example, **xlcFileDelete** takes a single argument: a file name or mask. This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation. It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission. To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="3531f-194">次のコード例では、マスク my_data\*.bak に一致する現在のディレクトリ内のファイルを削除します。その際、引数が true の場合にのみダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3531f-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="3531f-195">インターナショナル バージョンの関数およびコマンドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="3531f-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="3531f-p115">関数名および XLM コマンド名をさまざまな言語で表示するように Excel を設定できます。一部の C API コマンドおよび関数は、関数名やコマンド名として解釈される文字列を操作します。たとえば、**xlcFormula** は、指定のセルに配置される文字列引数を取ります。アドインがあらゆる言語設定で動作するためには、英語の文字列名を指定し、関数またはコマンドの列挙体にビット 0x2000 (**xlIntl**) を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3531f-p115">You can configure Excel to display functions and XLM command names in a variety of languages. Some C API commands and functions operate on strings that are interpreted as function or command names. For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell. For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="3531f-200">次のコード例では、作業中のワークシートのセル A2 に `=SUM(X1:X100)` と同等の働きをするものを配置します。</span><span class="sxs-lookup"><span data-stu-id="3531f-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="3531f-201">一時的な外部参照 **XLOPER** を作成するために、フレームワーク関数 **TempActiveRef** が使用されている点に注目してください。</span><span class="sxs-lookup"><span data-stu-id="3531f-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="3531f-202">この数式は A2 に適切なロケールに基づく言語 (たとえば、言語がフランス語の場合には `=SOMME(X1:X100)`) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="3531f-p117">**Excel12** の呼び出し結果は必須ではないため、**xResult** のアドレスの代わりに 0 (NULL) が 2 番目の引数として渡される可能性があります。これについては次のセクションで詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="3531f-p117">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**. This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="3531f-205">DLL 専用の関数とコマンド</span><span class="sxs-lookup"><span data-stu-id="3531f-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="3531f-206">Excel では、DLL や XLL からのみアクセスできる関数が少数サポートされています。</span><span class="sxs-lookup"><span data-stu-id="3531f-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="3531f-207">これらは、ヘッダー ファイルで `(n | xlSpecial)` として定義されます。`n` は 0 以上の 10 進数で、`xlSpecial` は 0x4000 の 16 進数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="3531f-208">これらの関数は以下の表にまとめられ、[API 関数リファレンス](excel-xll-sdk-api-function-reference.md)に記されています。</span><span class="sxs-lookup"><span data-stu-id="3531f-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="3531f-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="3531f-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="3531f-210">0</span><span class="sxs-lookup"><span data-stu-id="3531f-210">0</span></span> | <span data-ttu-id="3531f-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-212">Excel によって割り当てられたメモリ リソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="3531f-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="3531f-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="3531f-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="3531f-214">1</span><span class="sxs-lookup"><span data-stu-id="3531f-214">1</span></span> | <span data-ttu-id="3531f-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-216">Excel スタック上の空き領域を返します。</span><span class="sxs-lookup"><span data-stu-id="3531f-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="3531f-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="3531f-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="3531f-218">2</span><span class="sxs-lookup"><span data-stu-id="3531f-218">2</span></span> | <span data-ttu-id="3531f-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-220">**XLOPER** と **XLOPER12** の種類の間で変換します</span><span class="sxs-lookup"><span data-stu-id="3531f-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="3531f-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="3531f-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="3531f-222">3</span><span class="sxs-lookup"><span data-stu-id="3531f-222">3</span></span> | <span data-ttu-id="3531f-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-224">セル値の設定のための高速なメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="3531f-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="3531f-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="3531f-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="3531f-226">4</span><span class="sxs-lookup"><span data-stu-id="3531f-226">4</span></span> | <span data-ttu-id="3531f-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-228">内部 ID からワークシート名を取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="3531f-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="3531f-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="3531f-230">5</span><span class="sxs-lookup"><span data-stu-id="3531f-230">5</span></span> | <span data-ttu-id="3531f-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-232">名前から、ワークシートの内部 ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="3531f-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="3531f-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="3531f-234">6</span><span class="sxs-lookup"><span data-stu-id="3531f-234">6</span></span> | <span data-ttu-id="3531f-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-236">ユーザーが **[キャンセル]** ボタンをクリックしたか、Esc キーを押したかを検証します。</span><span class="sxs-lookup"><span data-stu-id="3531f-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="3531f-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="3531f-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="3531f-238">7</span><span class="sxs-lookup"><span data-stu-id="3531f-238">7</span></span> | <span data-ttu-id="3531f-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-240">Excel インスタンス ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="3531f-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="3531f-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="3531f-242">8</span><span class="sxs-lookup"><span data-stu-id="3531f-242">8</span></span> | <span data-ttu-id="3531f-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-244">Excel のメイン ウィンドウ ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="3531f-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="3531f-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="3531f-246">9</span><span class="sxs-lookup"><span data-stu-id="3531f-246">9</span></span> | <span data-ttu-id="3531f-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-248">DLL のパスとファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="3531f-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="3531f-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="3531f-250">10</span><span class="sxs-lookup"><span data-stu-id="3531f-250">10</span></span> | <span data-ttu-id="3531f-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-252">この関数は廃止されており、呼び出される必要もなくなりました。</span><span class="sxs-lookup"><span data-stu-id="3531f-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="3531f-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="3531f-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="3531f-254">11</span><span class="sxs-lookup"><span data-stu-id="3531f-254">11</span></span> | <span data-ttu-id="3531f-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-256">この関数は廃止されており、呼び出される必要もなくなりました。</span><span class="sxs-lookup"><span data-stu-id="3531f-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="3531f-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="3531f-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="3531f-258">12</span><span class="sxs-lookup"><span data-stu-id="3531f-258">12</span></span> | <span data-ttu-id="3531f-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-260">永続バイナリ ストレージ名を定義します。</span><span class="sxs-lookup"><span data-stu-id="3531f-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="3531f-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="3531f-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="3531f-262">13</span><span class="sxs-lookup"><span data-stu-id="3531f-262">13</span></span> | <span data-ttu-id="3531f-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="3531f-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="3531f-264">永続バイナリ ストレージ名のデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="3531f-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="3531f-265">戻り値 XLOPER/XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="3531f-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="3531f-266">_operRes_ 引数は、コールバックへの 2 番目の引数であり、**XLOPER** (**Excel4** および **Excel4v**) または **XLOPER12** (**Excel12** および **Excel12v**) へのポインターでもあります。</span><span class="sxs-lookup"><span data-stu-id="3531f-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="3531f-267">呼び出しが正常に行われると、関数またはコマンドの戻り値が引数に含まれます。</span><span class="sxs-lookup"><span data-stu-id="3531f-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="3531f-268">戻り値が必要ない場合は、**operRes** を 0 (Null ポインター) に設定します。</span><span class="sxs-lookup"><span data-stu-id="3531f-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="3531f-269">**operRes** の以前のコンテンツは上書きされるので、以前にポイントされていたメモリは、呼び出し前に解放してメモリ リークを回避しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3531f-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="3531f-p120">関数やコマンドを呼び出すことができない場合 (たとえば、引数が正しくない場合)、**operRes** はエラー **#VALUE!** に設定されます。コマンドが成功する場合には常に **Boolean** **TRUE** を返します。失敗した場合、またはユーザーがキャンセルした場合には **FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="3531f-p120">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**. A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="3531f-272">2 回目以降の引数の数: count</span><span class="sxs-lookup"><span data-stu-id="3531f-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="3531f-273">_count_ 引数は、コールバック関数への 3 番目の引数で、32 ビット符号付き整数です。</span><span class="sxs-lookup"><span data-stu-id="3531f-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="3531f-274">これは、2 番目以降の引数の数に設定する必要があります。この数は 1 から始まります。</span><span class="sxs-lookup"><span data-stu-id="3531f-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="3531f-275">関数やコマンドが引数を取らない場合は、0 に設定してください。</span><span class="sxs-lookup"><span data-stu-id="3531f-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="3531f-276">Microsoft Office Excel 2003 では、任意の関数で取ることができる引数の最大数は 30 です。ただし、多くの場合に実際に取る数はそれより少なくなります。</span><span class="sxs-lookup"><span data-stu-id="3531f-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="3531f-277">Excel 2007 以降、任意の関数で取ることができる引数の最大数は 255 に拡張されました。</span><span class="sxs-lookup"><span data-stu-id="3531f-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="3531f-278">**Excel4** と **Excel12** の場合、_count_ は、渡される **XLOPER** 値または **XLOPER12** 値へのポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="3531f-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="3531f-279">_count_ が設定されている値よりも少ない数の引数を渡すことがないように十分に注意してください。</span><span class="sxs-lookup"><span data-stu-id="3531f-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="3531f-280">少ない数にすると、Excel はスタックを先読みし、無効な **XLOPER** 値または **XLOPER12** 値を処理しようとするため、アプリケーション クラッシュが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3531f-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="3531f-281">**Excel4v** と **Excel12v**の場合、_count_ は、次の引数と最後の引数として渡される **XLOPER** 値または **XLOPER12** 値へのポインターの配列のサイズです。</span><span class="sxs-lookup"><span data-stu-id="3531f-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="3531f-282">この場合も、_count_ 要素よりも小さいサイズの配列を渡すことがないように十分に注意してください。そうした配列を渡すと、配列の境界がオーバーランしてしまうことになります。</span><span class="sxs-lookup"><span data-stu-id="3531f-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="3531f-283">C API 関数への引数の引き渡し</span><span class="sxs-lookup"><span data-stu-id="3531f-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="3531f-284">**Excel4** と **Excel12** は _count_ の後に可変長引数リストを受け取り、それぞれが **XLOPER** 値および **XLOPER12** 値へのポインターとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="3531f-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="3531f-285">**Excel4v** と **Excel12v** は _count_ の後に 1 つの引数を受け取ります。これは、**Excel4v** では **XLOPER** 値への、**Excel12v** では **XLOPER12** 値へのポインター配列へのポインターとなります。</span><span class="sxs-lookup"><span data-stu-id="3531f-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="3531f-p125">配列フォーム **Excel4v** および **Excel12v** を使用すると、引数の数が可変の場合に C API への呼び出しを分かりやすくコーディングできます。次の例は、数値の可変サイズの配列を取り、C API を介して合計、平均、最小、最大を計算する Excel ワークシート関数を使用する関数について示しています。 </span><span class="sxs-lookup"><span data-stu-id="3531f-p125">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable. The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="3531f-p126">前述のコードで **XLOPER12** 値への参照を **XLOPER** に、**Excel12v** への参照を **Excel4v** に置き換えると、あらゆるバージョンの Excel で動作する関数になります。Excel 関数の **SUM**、**AVERAGE**、**MIN**、**MAX** のこの操作は単純で、C におけるコーディングの効率を向上させると同時に、引数の準備や Excel への呼び出しのオーバーヘッドを回避できます。ただし、Excel に入っている関数の多くはより複雑ですが、この方法が役立つ場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3531f-p126">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel. This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel. However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="3531f-p127">[xlfRegister](xlfregister-form-1.md) のトピックには、**Excel4v** と **Excel12v** を使用した別の処理例が記されています。XLL ワークシート関数を登録すると、**[関数貼り付け]** ダイアログ ボックスで使用されている各引数の説明文字列を提供できます。そのため、**xlfRegister** に指定する引数の合計数は XLL 関数が取る引数の数に依存し、関数ごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="3531f-p127">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**. When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box. Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="3531f-p128">常に引数の数が同じ C API 関数またはコマンドを呼び出す場合には、こうした引数のポインター配列を作成するという追加手順を回避したいことがあります。その場合、**Excel4** と **Excel12** を使用する方が単純かつ分かりやすくなります。たとえば、XLL 関数とコマンドを登録するときに、DLL または XLL の完全なパスとファイル名を提供する必要があります。次の **Excel4** と **Excel12** の例に示されているように、**xlfGetName** への呼び出しでファイル名を取得し、それを **xlFree** を呼び出してリリースします。</span><span class="sxs-lookup"><span data-stu-id="3531f-p128">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments. In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**. For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL. You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="3531f-298">実際には、関数 **Excel12v_example** はより効率的にコーディングできます。そのためには、1 つの **xltypeMulti** **XLOPER12** 引数を作成し、**Excel12** を使用して C API を呼び出します。その例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3531f-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="3531f-p129">この場合、**Excel12** の戻り値は無視されます。代わりにコードによって、返された **XLOPER12** が **xltypeNum** であるかをチェックして、呼び出しが成功したかどうかを判別します。</span><span class="sxs-lookup"><span data-stu-id="3531f-p129">In this case, the return value of **Excel12** is ignored. The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="3531f-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="3531f-301">XLCallVer</span></span>

<span data-ttu-id="3531f-302">コールバック **Excel4**、**Excel4v**、**Excel12**、**Excel12v** に加え、Excel は関数 **XLCallVer** をエクスポートします。この関数は、現在実行している C API のバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="3531f-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="3531f-303">関数プロトタイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3531f-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="3531f-304">スレッド セーフなこの関数は、あらゆる XLL コマンドまたは関数から呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="3531f-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="3531f-305">Excel 97 から Excel 2003 までの場合、**XLCallVer** は 1280 = 0x0500 hex = 5 x 256 を返します。これは、Excel バージョン 5 を示します。</span><span class="sxs-lookup"><span data-stu-id="3531f-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="3531f-306">Excel 2007 以降では、3072 = 0x0c00 hex = 12 x 256 を返し、バージョン 12 を示します。</span><span class="sxs-lookup"><span data-stu-id="3531f-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="3531f-307">この関数を使用して実行時に新しい C API を利用できるかどうかを判断できますが、`Excel4(xlfGetWorkspace, &version, 1, &arg)` を使用して Excel の実行バージョンを検出することもできます。`arg` は、2 に設定された数値の **XLOPER** です。</span><span class="sxs-lookup"><span data-stu-id="3531f-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="3531f-308">この関数は、文字列 **XLOPER** を返すので、強制的に整数にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3531f-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="3531f-309">C API バージョンではなく Excel バージョンに依存するのは、ご使用のアドインでも検出しなければならない相違が Excel 2000、Excel 2002、Excel 2003 の間にあるためです。</span><span class="sxs-lookup"><span data-stu-id="3531f-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="3531f-310">たとえば、一部の統計関数の精度に変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="3531f-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3531f-311">関連項目</span><span class="sxs-lookup"><span data-stu-id="3531f-311">See also</span></span>

- [<span data-ttu-id="3531f-312">XLL を作成する</span><span class="sxs-lookup"><span data-stu-id="3531f-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="3531f-313">Excel での XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="3531f-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="3531f-314">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="3531f-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="3531f-315">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="3531f-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="3531f-316">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="3531f-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

