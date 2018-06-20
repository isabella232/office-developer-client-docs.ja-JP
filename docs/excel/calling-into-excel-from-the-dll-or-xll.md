---
title: DLL または XLL から Excel に呼び出す
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- ダイアログ ボックス [excel 2007] を呼び出すことは、コマンド、Dll の [Excel 2007]、[Excel 2007] のコマンドを Excel では、[Excel 2007] の C API 関数に引数を渡す方法を呼び出すことを excel のダイアログ ボックスを呼び出すと、コマンド [Excel 2007] では、DLL または xll ファイル、Excel4 からアクセスできる機能 [Excel 2007] Excel12 関数 [Excel 2007] XLCallVer [Excel 2007] の [Excel 2007] は、operRes 引数を関数、関数 [Excel 2007] では、DLL または xll ファイル、Excel12v からアクセス可能な機能の [Excel 2007]、DLL のみ [Excel 2007]、[Excel 2007] c 言語の API に渡す機能引数、引数 [Excel 2007]、コマンド [Excel 2007] では、他の言語バージョンを呼び出す、DLL 専用のコマンド [Excel 2007]、[Excel 2007] の各国語版、関数を呼び出すとカウント コマンド、Xll [Excel 2007] では、Excel 4 v 関数 [Excel への呼び出しExcel 2007]、xlfn の引数 [Excel 2007] では、関数 [Excel 2007] では、他の言語バージョンを呼び出す
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798820"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="7ef4c-104">DLL または XLL から Excel に呼び出す</span><span class="sxs-lookup"><span data-stu-id="7ef4c-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="7ef4c-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7ef4c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7ef4c-p101">Microsoft Excel を使用すると、DLL は組み込みの Excel コマンド、ワークシート関数、マクロ シート関数にアクセスできます。こうしたコマンドや関数は、Visual Basic for Applications (VBA) で呼び出される DLL コマンドと関数から、および Excel によって直接呼び出される登録済み XLL コマンドと関数から使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-p101">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions. These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="7ef4c-108">Excel4、Excel4v、Excel12、Excel12v 関数</span><span class="sxs-lookup"><span data-stu-id="7ef4c-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="7ef4c-109">Excel では、 [Excel4](excel4-excel12.md)、 [Excel4v](excel4v-excel12v.md)、 [Excel12](excel4-excel12.md)、および[Excel12v](excel4v-excel12v.md)のコールバック関数を使用してコマンドや機能にアクセスするのには、DLL を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="7ef4c-110">**Excel4**と**Excel4v**関数は、Excel バージョン 4 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="7ef4c-111">**XLOPER**データ構造で動作します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="7ef4c-112">Excel 2007 には、2 つ新しいコールバック関数、 **Excel12**と**Excel12v**、 **XLOPER12**のデータ構造体の使用が導入されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="7ef4c-113">**Excel4**と**Excel4v**関数は、ライブラリ、DLL や XLL プロジェクトに含める必要があります Xlcall32.lib でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="7ef4c-114">**XLOPER12**構造体を使用して、Excel の機能にアクセスする場合に、プロジェクトに含める必要があります Xlcall.cpp SDK の C++ ソース ファイルには、 **Excel12**と**Excel12v**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="7ef4c-115">次のコードは、これら 4 つの関数の関数プロトタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="7ef4c-116">最初の 3 つの引数は、2 番目の引数は、最初のペアでは、 **XLOPER**へのポインターと 2 番目のペアで、 **XLOPER12**へのポインターが同じです。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="7ef4c-117">呼び出し規約は、可変個引数リストを許可するには、 **Excel4**と**Excel12** **に従って _cdecl**です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="7ef4c-118">省略記号は、 **Excel4**の**XLOPER**の値と**Excel12**を**XLOPER12**の値へのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="7ef4c-119">_Count_パラメーターの値をポインターの数に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="7ef4c-120">**Excel のすべてのバージョン**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="7ef4c-121">**Excel 2007 の起動**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="7ef4c-122">**Excel4**、 **Excel4v**、 **Excel12**、または**Excel12v**を呼び出すことができる DLL、Excel は、DLL に制御を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="7ef4c-123">これは、次のシナリオでのみこれらの API のコールバックを呼び出すことができることを意味します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="7ef4c-124">Excel が直接または VBA を介して呼び出した XLL コマンドから。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="7ef4c-125">Excel が直接または VBA を介して呼び出した XLL ワークシート関数またはマクロ シート関数から。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="7ef4c-126">次のシナリオでは、Excel C API を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="7ef4c-127">( [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx)関数) からでは、オペレーティング システム イベント。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-127">From an operating system event (for example, from the [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) function).</span></span> 
    
- <span data-ttu-id="7ef4c-128">DLL が作成したバックグラウンド スレッドから。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="7ef4c-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="7ef4c-129">Return values</span></span>

<span data-ttu-id="7ef4c-p105">これら 4 つの関数はいずれも整数値を返します。この値によって、呼び出し元に対して、関数またはコマンドが正常に呼び出されたかどうかが知らされます。次のいずれかの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-p105">All four of these functions return an integer value that informs the caller whether the function or command was called successfully. The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="7ef4c-132">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-132">**Return value**</span></span>|<span data-ttu-id="7ef4c-133">**として Xlcall.h で定義されています。**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="7ef4c-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ef4c-135">0</span><span class="sxs-lookup"><span data-stu-id="7ef4c-135">0</span></span>  <br/> |<span data-ttu-id="7ef4c-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="7ef4c-137">関数やコマンドが正常に実行します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-137">The function or command executed successfully.</span></span> <span data-ttu-id="7ef4c-138">実行が正常にエラーがないことはありません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="7ef4c-139">たとえば、 **Excel4**を返す**xlretSuccess** **検索**をには、関数を呼び出すときに評価されることも **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="7ef4c-140">検索文字列が見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-140">because the search text could not be found.</span></span> <span data-ttu-id="7ef4c-141">種類と返される**XLOPER/XLOPER12**の値を検査する必要がありますこの可能性については。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-142">1</span><span class="sxs-lookup"><span data-stu-id="7ef4c-142">1</span></span>  <br/> |<span data-ttu-id="7ef4c-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="7ef4c-144">コマンド マクロは、 **[キャンセル**] ボタンをクリックするか、ESC キーを押すと、ユーザーによって停止されました。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-145">2</span><span class="sxs-lookup"><span data-stu-id="7ef4c-145">2</span></span>  <br/> |<span data-ttu-id="7ef4c-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="7ef4c-p107">指定された関数コードまたはコマンド コードが無効です。このエラーは、呼び出し元の関数に関数またはコマンドを呼び出すアクセス許可がない場合に生じます。たとえば、ワークシート関数は、マクロ シート情報関数またはコマンド関数を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-p107">The supplied function or command code is not valid. This error can occur when the calling function does not have permission to call the function or command. For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-150">4</span><span class="sxs-lookup"><span data-stu-id="7ef4c-150">4</span></span>  <br/> |<span data-ttu-id="7ef4c-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="7ef4c-152">呼び出しで指定した引数の数が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-153">8</span><span class="sxs-lookup"><span data-stu-id="7ef4c-153">8</span></span>  <br/> |<span data-ttu-id="7ef4c-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="7ef4c-155">**XLOPER**または**XLOPER12**の引数の値の 1 つ以上が正しく形成、または設定します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-156">16</span><span class="sxs-lookup"><span data-stu-id="7ef4c-156">16</span></span>  <br/> |<span data-ttu-id="7ef4c-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="7ef4c-158">Excel によって、操作でスタックがオーバーフローする危険が検出され、関数が呼び出されませんでした。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-159">32</span><span class="sxs-lookup"><span data-stu-id="7ef4c-159">32</span></span>  <br/> |<span data-ttu-id="7ef4c-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="7ef4c-161">コマンドまたは関数は、他の戻り値のいずれかで記述されていないため失敗しました。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="7ef4c-162">たとえば、大量のメモリを必要とする操作はこのエラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="7ef4c-163">[XlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx)関数を使用して、非常に大きな配列への参照を**xltypeMulti**に変換しようとしたらこれでした。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) function.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-164">64</span><span class="sxs-lookup"><span data-stu-id="7ef4c-164">64</span></span>  <br/> |<span data-ttu-id="7ef4c-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="7ef4c-p109">計算されていないセルの値を取得しようとする操作が行われました。Excel で再計算整合性を保持するため、ワークシート関数ではこれを行うことができません。ただし、マクロ シート関数として登録された XLL コマンドおよび関数は、計算されていないセル値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-p109">The operation attempted to retrieve the value of an uncalculated cell. To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this. However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-169">128</span><span class="sxs-lookup"><span data-stu-id="7ef4c-169">128</span></span>  <br/> |<span data-ttu-id="7ef4c-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="7ef4c-171">(Excel 2007 で開始)スレッド セーフとして登録されている XLL ワークシート関数は、スレッド セーフではない C API 関数を呼び出すしようとしました。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="7ef4c-172">たとえば、スレッド セーフでない関数では、XLM 関数**xlfGetCell**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-173">256</span><span class="sxs-lookup"><span data-stu-id="7ef4c-173">256</span></span>  <br/> |<span data-ttu-id="7ef4c-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="7ef4c-175">(Excel 2010 年に開始)非同期関数のハンドルが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="7ef4c-176">512</span><span class="sxs-lookup"><span data-stu-id="7ef4c-176">512</span></span>  <br/> |<span data-ttu-id="7ef4c-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="7ef4c-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="7ef4c-178">(Excel 2010 年に開始)クラスターでは、呼び出しはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="7ef4c-179">返しますエラー値のいずれかのテーブルで (つまり、それを返さない**xlretSuccess**)、 **XLOPER**または**XLOPER12**の戻り値も設定する **#VALUE!** です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="7ef4c-180">チェックの成功のための十分なテストがありますが、呼び出しが両方の**xlretSuccess**を返すことに注意してください、特定の状況で、 **#VALUE!** です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="7ef4c-181">**XlretUncalced**または**xlretAbort**のいずれかで、C API を呼び出し、DLL や XLL コードはコントロールに戻ります Excel (Excel で割り当てられたメモリを解放する[xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx)関数の呼び出し以外の他の C API の呼び出しを行う前にリソースの**XLOPER**および**XLOPER12**の値)。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="7ef4c-182">コマンドまたは関数の列挙型引数: xlfn</span><span class="sxs-lookup"><span data-stu-id="7ef4c-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="7ef4c-183">_Xlfn_引数は、コールバックを最初の引数が機能し、32 ビット符号付き整数です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="7ef4c-184">次の例のようには、その値は Xlcall.h、SDK のヘッダー ファイルで定義されている関数やコマンドの列挙値のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
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

<span data-ttu-id="7ef4c-185">関数は、0x0fff の 16 進数、0 (**xlfCount**) から最高 Excel 2013 での番号が割り当てられますが、すべてのワークシートとマクロ シートは、547 10 進数、0x0223 16 進数 (**xlfFloor_precise**) です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="7ef4c-186">0x8000 16 進数 (**xlcBeep**) から 0x8fff の 16 進数、使用の範囲のコマンドのすべての機能は、Excel 2013 での最高の割り当てられた番号は、16 進数の 0x8328 (**xlcHideallInkannots**)。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="7ef4c-187">としてヘッダー ファイルでこれらの定義は、 `(n | xlCommand)` 、`n`の 10 進数は 0 以上、および**xlCommand**が 0x8000 を 16 進数として定義されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="7ef4c-188">ダイアログ ボックスを使用した Excel コマンドの起動</span><span class="sxs-lookup"><span data-stu-id="7ef4c-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="7ef4c-189">コマンド コードのいくつかは、ダイアログ ボックスを使用する Excel での操作に対応しています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="7ef4c-190">たとえば、 **xlcFileDelete**では、1 つの引数: ファイル名またはマスク。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="7ef4c-191">ユーザーがキャンセルまたは削除操作を変更する機会を持ってできるようにダイアログ ボックスを起動できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="7ef4c-192">それもなしで呼び出される] ダイアログ ボックスでは、存在して、呼び出し元がアクセス許可を持つと仮定した場合、それ以上の介入なしのファイルまたはファイルを削除する場合。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="7ef4c-193">このようなコマンドを呼び出すと、ダイアログ ボックスの形式で、コマンドの列挙体を 0x1000 (**xlPrompt**) のビットごとの OR 演算を使用して組み合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="7ef4c-194">マスク my_data に一致する現在のディレクトリ内のファイルを削除するコード例を次に示します\*.bak、引数が true の場合にのみ、ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="7ef4c-195">インターナショナル バージョンの関数およびコマンドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="7ef4c-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="7ef4c-196">関数およびコマンド名の XLM をさまざまな言語で表示するのには Excel を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="7ef4c-197">いくつかの C API コマンドおよび関数は、関数やコマンド名として解釈される文字列を操作します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="7ef4c-198">たとえば、 **xlcFormula**では、指定したセルに配置することは意図されている文字列引数を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="7ef4c-199">アドインのすべての言語設定を使用するのには、英語の文字列名を指定し、関数やコマンドの列挙に含まれるビット 0x2000 (**xlIntl**) を設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="7ef4c-200">コード例を次の配置のと同じ`=SUM(X1:X100)`作業中のシートのセル A2 に。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="7ef4c-201">Framework 関数、 **TempActiveRef**を使用して**XLOPER**の一時的な外部参照を作成することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="7ef4c-202">数式は A2 に含まれる適切なロケールが指定した言語で表示されます (たとえば、`=SOMME(X1:X100)`の言語がフランス語の場合)。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
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
> <span data-ttu-id="7ef4c-203">**Excel12**への呼び出しの結果が必要ないので、0 (NULL) は**xResult**のアドレスではなく 2 番目の引数として渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="7ef4c-204">これについては次のセクションで詳細説明します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-204">This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="7ef4c-205">DLL 専用の関数とコマンド</span><span class="sxs-lookup"><span data-stu-id="7ef4c-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="7ef4c-206">Excel には、DLL や xll ファイルからアクセスできる機能の数が少ないがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="7ef4c-207">としてヘッダー ファイルで定義されているこれらは`(n | xlSpecial)`、`n`よりも大きい値または 0 に等しい 10 進数では、 `xlSpecial` 0x4000 16 進数として定義されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="7ef4c-208">これらの関数は次の表に記載されているし、 [API 関数のリファレンス](excel-xll-sdk-api-function-reference.md)に記載されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="7ef4c-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="7ef4c-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="7ef4c-210">0</span><span class="sxs-lookup"><span data-stu-id="7ef4c-210">0</span></span> | <span data-ttu-id="7ef4c-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-212">Excel によって割り当てられたメモリ リソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="7ef4c-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="7ef4c-214">1</span><span class="sxs-lookup"><span data-stu-id="7ef4c-214">1</span></span> | <span data-ttu-id="7ef4c-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-216">Excel スタック上の空き領域を返します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="7ef4c-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="7ef4c-218">2</span><span class="sxs-lookup"><span data-stu-id="7ef4c-218">2</span></span> | <span data-ttu-id="7ef4c-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-220">**XLOPER**および**XLOPER12**型間の変換します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="7ef4c-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="7ef4c-222">3</span><span class="sxs-lookup"><span data-stu-id="7ef4c-222">3</span></span> | <span data-ttu-id="7ef4c-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-224">セル値の設定のための高速なメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="7ef4c-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="7ef4c-226">4</span><span class="sxs-lookup"><span data-stu-id="7ef4c-226">4</span></span> | <span data-ttu-id="7ef4c-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-228">内部 ID からワークシート名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="7ef4c-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="7ef4c-230">5</span><span class="sxs-lookup"><span data-stu-id="7ef4c-230">5</span></span> | <span data-ttu-id="7ef4c-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-232">名前から、ワークシートの内部 ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="7ef4c-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="7ef4c-234">6</span><span class="sxs-lookup"><span data-stu-id="7ef4c-234">6</span></span> | <span data-ttu-id="7ef4c-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-236">ユーザーが **[キャンセル**] ボタンがクリックされたか、ESC キーが押されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="7ef4c-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="7ef4c-238">7</span><span class="sxs-lookup"><span data-stu-id="7ef4c-238">7</span></span> | <span data-ttu-id="7ef4c-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-240">Excel インスタンス ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="7ef4c-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="7ef4c-242">8</span><span class="sxs-lookup"><span data-stu-id="7ef4c-242">8</span></span> | <span data-ttu-id="7ef4c-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-244">Excel のメイン ウィンドウ ハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="7ef4c-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="7ef4c-246">9</span><span class="sxs-lookup"><span data-stu-id="7ef4c-246">9</span></span> | <span data-ttu-id="7ef4c-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-248">DLL のパスとファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="7ef4c-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="7ef4c-250">10</span><span class="sxs-lookup"><span data-stu-id="7ef4c-250">10</span></span> | <span data-ttu-id="7ef4c-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-252">���̊֐��͎g�p����Ă��炸�A�Ăяo�����K�v��Ȃ��Ȃ�܂����B</span><span class="sxs-lookup"><span data-stu-id="7ef4c-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="7ef4c-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="7ef4c-254">11</span><span class="sxs-lookup"><span data-stu-id="7ef4c-254">11</span></span> | <span data-ttu-id="7ef4c-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-256">���̊֐��͎g�p����Ă��炸�A�Ăяo�����K�v��Ȃ��Ȃ�܂����B</span><span class="sxs-lookup"><span data-stu-id="7ef4c-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="7ef4c-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="7ef4c-258">12</span><span class="sxs-lookup"><span data-stu-id="7ef4c-258">12</span></span> | <span data-ttu-id="7ef4c-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-260">永続バイナリ ストレージ名を定義します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="7ef4c-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="7ef4c-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="7ef4c-262">13</span><span class="sxs-lookup"><span data-stu-id="7ef4c-262">13</span></span> | <span data-ttu-id="7ef4c-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="7ef4c-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="7ef4c-264">バイナリ ストレージが永続的な名前のデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="7ef4c-265">XLOPER/XLOPER12 の値を返す: operRes</span><span class="sxs-lookup"><span data-stu-id="7ef4c-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="7ef4c-266">_OperRes_引数では、コールバックには、2 番目の引数では、 **XLOPER** (**Excel4**および**Excel4v**) または**XLOPER12** (**Excel12**および**Excel12v**) へのポインターします。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="7ef4c-267">呼び出しが成功すると、関数やコマンドの戻り値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="7ef4c-268">**operRes**は、戻り値が必要ない場合、0 (NULL ポインター) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="7ef4c-269">以前が指すメモリは、メモリ リークを回避するのには呼び出しをする前に解放する必要がありますように、 **operRes**の以前の内容が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="7ef4c-270">**OperRes**がエラーに設定されている場合は (たとえば、引数が適切ではありません) 場合は、関数やコマンドを呼び出すことができない、 **#VALUE!** です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="7ef4c-271">コマンドは、成功すると、 **FALSE**に失敗した場合や、ユーザーのキャンセルにより、または**ブール値****は TRUE**常に返します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="7ef4c-272">2 回目以降の引数の数: count</span><span class="sxs-lookup"><span data-stu-id="7ef4c-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="7ef4c-273">引数_count_はコールバックには、3 番目の引数では、32 ビット符号付き整数です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="7ef4c-274">1 から数えて、それ以降の引数の数を設定します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="7ef4c-275">関数やコマンドの引数をとらない場合は、0 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="7ef4c-276">ほとんどを実行するよりも少ない、Microsoft Office Excel 2003 では、任意の関数が取ることができる引数の最大数、30、です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="7ef4c-277">Excel 2007 以降では、任意の関数が取ることができる引数の最大数は 255 に増加させました。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="7ef4c-278">**Excel4**と**Excel12**、_カウント_は、渡される**XLOPER**または**XLOPER12**の値へのポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="7ef4c-279">その_数_の値より少ない引数を渡すには十分に注意する必要があります] に設定されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="7ef4c-280">Excel スタックに先読みし、無効な**XLOPER**または**XLOPER12**の値、アプリケーション クラッシュが発生する可能性がありますを処理しようとしていますが発生します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="7ef4c-281">**Excel4v**と**Excel12v**は、_カウント_は、次と最後の引数として渡される**XLOPER**または**XLOPER12**の値へのポインターの配列のサイズです。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="7ef4c-282">もう一度、このオーバーランが発生している配列の境界になります、サイズ、_数_の要素よりも小さく、配列を渡すには十分に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="7ef4c-283">C API 関数への引数の引き渡し</span><span class="sxs-lookup"><span data-stu-id="7ef4c-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="7ef4c-284">両方**Excel4**および**Excel12**を可変長引数リストでは、_カウント_、それぞれ**XLOPER**および**XLOPER12**の値へのポインターとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="7ef4c-285">**Excel4v**と**Excel12v** _カウント_ポインターの場合は**Excel4v**、 **XLOPER**の値、 **Excel12v**の場合**XLOPER12**の値の配列へのポインターである 1 つの引数がかかります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="7ef4c-286">配列フォーム、 **Excel4v** **Excel12v**では、引数の数が変数の場合、C API への呼び出しを正常にコードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="7ef4c-287">次の例では、数値の可変サイズの配列を受け取るし、c 言語の API を使用して、Excel のワークシート関数を使用して、合計、平均、最小、および最大を計算する関数を示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
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

<span data-ttu-id="7ef4c-288">**XLOPER12**の値への参照を**XLOPER**、および**Excel4v**と**Excel12v**に置き換えて、上記のコードになりますすべてのバージョンの Excel で動作する関数。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="7ef4c-289">**合計**、**平均**、**最小**、および**最大値**は、Excel の関数には、この操作は、単純に C のコードし、引数を準備して、Excel への呼び出しのオーバーヘッドを回避する方が効率的となります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="7ef4c-290">ただし、Excel に含まれている関数の多くより複雑なためこの方法をいくつかの場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="7ef4c-291">[XlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx)トピックには、 **Excel4v**と**Excel12v**の別の例が用意されています。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-291">The [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="7ef4c-292">XLL ワークシート関数を登録するときは、 **[関数貼り付け**] ダイアログ ボックスで使用されている各引数について説明する文字列を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="7ef4c-293">したがって、 **xlfRegister**を提供する合計の引数の数は、XLL 関数は、引数の数によって異なりますおり、次に 1 つの関数から異なります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="7ef4c-294">C API 関数またはコマンドの引数の数が同じで常に呼び出すと、どこに、これらの引数のポインターの配列を作成する余分な手順を避けるためにします。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="7ef4c-295">ような場合は、簡単、 **Excel4**と**Excel12**を使用するクリーナーがあります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="7ef4c-296">たとえば、XLL 関数とコマンドを登録するときは、DLL または xll ファイルのフル パスとファイル名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="7ef4c-297">**XlfGetName**への呼び出しでファイル名を取得し、元の呼び出しを**xlFree**、 **Excel4**と**Excel12**の両方の例を次に示すようにできます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
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

<span data-ttu-id="7ef4c-298">実際には、関数、 **Excel12v_example**、でしたをコーディングするより効率的に、1 つ**xltypeMulti** **XLOPER12**の引数を作成し、次の例のように、 **Excel12**を使用して C API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
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
> <span data-ttu-id="7ef4c-299">この例では、 **Excel12**の戻り値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="7ef4c-300">コードは、返される**XLOPER12**では、呼び出しが成功したかどうかを判断するのには**xltypeNum**が、代わりにチェックします。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="7ef4c-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="7ef4c-301">XLCallVer</span></span>

<span data-ttu-id="7ef4c-302">**Excel4**、 **Excel4v**、 **Excel12**、および**Excel12v**のコールバックだけでなく**XLCallVer**、現在実行されている C API のバージョンを返す関数が Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="7ef4c-303">関数プロトタイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="7ef4c-304">スレッド セーフなこの関数は、あらゆる XLL コマンドまたは関数から呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="7ef4c-305">Excel 2003、Excel 97 では、 **XLCallVer**は 1280 = 値を 0x0500 の 16 進数を返します。 = 5 x 256、Excel バージョン 5 を示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="7ef4c-306">3072 と = 場合は 0x0c00。 16 進数を返す Excel 2007 以降では、12 x 256、同様に 12 のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="7ef4c-307">新しい C API は、実行時に使用できるかどうかを判断するには、これを使用できますが、実行中のバージョンの Excel を使用して検出する方が`Excel4(xlfGetWorkspace, &version, 1, &arg)`、`arg`は、 **XLOPER**を 2 に設定する数値です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="7ef4c-308">**XLOPER**バージョンは、整数値に強制的に変換する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="7ef4c-309">C API のバージョンではなく、Excel のバージョンに依存することの理由は、Excel 2000、Excel 2002 および Excel 2003 を追加で必要な場合も検出される間の相違点があること。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="7ef4c-310">などが変更されたいくつかの統計関数の精度です。</span><span class="sxs-lookup"><span data-stu-id="7ef4c-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ef4c-311">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ef4c-311">See also</span></span>



[<span data-ttu-id="7ef4c-312">XLL ��쐬����</span><span class="sxs-lookup"><span data-stu-id="7ef4c-312">Creating XLLs</span></span>](creating-xlls.md)
  
<span data-ttu-id="7ef4c-313">[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="7ef4c-313">[Accessing XLL Code in Excel](accessing-xll-code-in-excel.md)</span></span>
  
[<span data-ttu-id="7ef4c-314">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="7ef4c-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
  
<span data-ttu-id="7ef4c-315">[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="7ef4c-315">[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)</span></span>
  
[<span data-ttu-id="7ef4c-316">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="7ef4c-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

