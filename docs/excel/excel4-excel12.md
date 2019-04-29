---
title: Excel4、Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- excel4 関数 [excel 2007]、Excel12 関数 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429447"
---
# <a name="excel4excel12"></a><span data-ttu-id="1b585-104">Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="1b585-104">Excel4/Excel12</span></span>

<span data-ttu-id="1b585-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b585-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1b585-106">Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 専用の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1b585-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL/XLL or code resource.</span></span>
  
<span data-ttu-id="1b585-107">Excel のすべての最新バージョンは、**Excel4** をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1b585-107">All recent versions of Excel support **Excel4**.</span></span> <span data-ttu-id="1b585-108">Excel 2007 以降では、**Excel12** がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1b585-108">Starting in Excel 2007, **Excel12** is supported.</span></span> 
  
<span data-ttu-id="1b585-p102">これらの関数は、Excel が DLL または XLL に制御を渡している場合にのみ、呼び出すことができます。これらの関数は、Excel が Visual Basic for Applications (VBA) への呼び出しを介して間接的に制御を渡したときにも呼び出せます。たとえば、[DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) 関数に対する呼び出しの間も、オペレーティング システムが DLL を呼び出しているときも、これらの関数を呼び出すことはできません。DLL が作成したスレッドからも、これらの関数を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="1b585-p102">These functions can be called only when Excel has passed control to the DLL or XLL. They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA). They cannot be called at any other time. For example, they cannot be called during calls to the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="1b585-p103">[Excel4v と Excel12v](excel4v-excel12v.md) 関数は、配列としてそれらの引数を受け入れます。一方、**Excel4** と **Excel12** 関数は、スタック上の可変長リストとしてそれらの引数を受け入れます。それ以外の点のすべてで、**Excel4** は **Excel4v** と同じように動作し、**Excel12** は **Excel12v** と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="1b585-p103">The [Excel4v and Excel12v](excel4v-excel12v.md) functions accept their arguments as an array, whereas the **Excel4** and **Excel12** functions accept their arguments as a variable-length list on the stack. In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="1b585-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b585-115">Parameters</span></span>

 <span data-ttu-id="1b585-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="1b585-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="1b585-p104">呼び出すコマンド、関数、または特殊関数を示す数値。_iFunction_ の有効な値の一覧は、次の解説を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b585-p104">A number that indicates the command, function, or special function you want to call. For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="1b585-119">_pxRes_ (**LPXLOPER** または **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="1b585-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="1b585-120">評価された関数の結果を保持する、**XLOPER** (**Excel4** の場合) または **XLOPER12** (**Excel12** の場合) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b585-120">A pointer to an **XLOPER** (with **Excel4**) or an **XLOPER12** (with **Excel12**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="1b585-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="1b585-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="1b585-122">関数へ渡される後続の引数の数。</span><span class="sxs-lookup"><span data-stu-id="1b585-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="1b585-123">Excel 2003 までのバージョンでは、0 から 30 までの任意の数です。</span><span class="sxs-lookup"><span data-stu-id="1b585-123">In versions of Excel up to 2003, this can be any number from 0 through 30.</span></span> <span data-ttu-id="1b585-124">Excel 2007 以降は、0 から 255 までの任意の数です。</span><span class="sxs-lookup"><span data-stu-id="1b585-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="1b585-125">_argument1, ..._ (**LPXLOPER** または **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="1b585-125">_argument1, ..._ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="1b585-p106">省略可能な、関数への引数。すべての引数が **XLOPER** または **XLOPER12** の値へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b585-p106">The optional arguments to the function. All arguments must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1b585-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="1b585-128">Return value</span></span>

<span data-ttu-id="1b585-129">次の整数値 (**int**) の 1 つを返します。</span><span class="sxs-lookup"><span data-stu-id="1b585-129">Returns one of the following integer (**int**) values.</span></span>
  
|<span data-ttu-id="1b585-130">**値**</span><span class="sxs-lookup"><span data-stu-id="1b585-130">**Value**</span></span>|<span data-ttu-id="1b585-131">**リターン コード**</span><span class="sxs-lookup"><span data-stu-id="1b585-131">**Return code**</span></span>|<span data-ttu-id="1b585-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="1b585-132">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b585-133">.0</span><span class="sxs-lookup"><span data-stu-id="1b585-133">0</span></span>  <br/> |<span data-ttu-id="1b585-134">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="1b585-134">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="1b585-135">関数は正常に呼び出されました。</span><span class="sxs-lookup"><span data-stu-id="1b585-135">The function was called successfully.</span></span> <span data-ttu-id="1b585-136">これは、この関数が Excel のエラー値を返さなかったという意味ではありません。それを判断するには、結果の _pxRes_ パラメーターの種類と値を調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b585-136">This does not mean that the function did not return an Excel error value; to find that out, you must look at the type and value of the resulting  _pxRes_ parameter.</span></span>  <br/> |
|<span data-ttu-id="1b585-137">1 </span><span class="sxs-lookup"><span data-stu-id="1b585-137">1</span></span>  <br/> |<span data-ttu-id="1b585-138">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="1b585-138">**xlretAbort**</span></span> <br/> |<span data-ttu-id="1b585-p108">コマンドまたは関数が異常終了しました (内部アボート)。これは、XLM マクロ シートが **CLOSE** を呼び出すことによってそれ自体を閉じた場合、またはExcel がメモリ不足になる場合に起こります。Excel がこのエラーを返す場合、呼び出し元の関数は即座に終了する必要があります。DLL が **xlFree** を呼び出すことが許可されるのは、終了前のみです。C API に対するそれ以外のすべての呼び出しは許可されません。ユーザーは、**[ファイル]** メニューの **[保存]** コマンドを使用して、対話形式で任意の作業を保存できます。</span><span class="sxs-lookup"><span data-stu-id="1b585-p108">The command or function was terminated abnormally (internal abort). This can occur if an XLM macro sheet closes itself by calling **CLOSE**, or if Excel is out of memory. If Excel returns this error, the calling function must exit immediately. The DLL is permitted to call **xlFree** only before exiting. All other calls to the C API are not permitted. The user can save any work interactively by using the **Save** command on the **File** menu.  </span></span><br/> |
|<span data-ttu-id="1b585-145">2 </span><span class="sxs-lookup"><span data-stu-id="1b585-145">2</span></span>  <br/> |<span data-ttu-id="1b585-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="1b585-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="1b585-p109">指定された関数の数が正しくありません。Xlcall.h ヘッダー ファイルの定数を使用している場合、実行中の Excel のバージョンでサポートされていない何かを呼び出さない限り、これが起こることはありません。</span><span class="sxs-lookup"><span data-stu-id="1b585-p109">An invalid function number was supplied. If you are using constants from the Xlcall.h header file, this should not occur unless you are calling something that is not supported in the version of Excel you are running.</span></span>  <br/> |
|<span data-ttu-id="1b585-149">4 </span><span class="sxs-lookup"><span data-stu-id="1b585-149">4</span></span>  <br/> |<span data-ttu-id="1b585-150">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="1b585-150">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="1b585-151">入力された引数の数が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="1b585-151">An invalid number of arguments was entered.</span></span> <span data-ttu-id="1b585-152">Excel 2003 までのバージョンでは、すべての関数の引数の最大数は 30 です。</span><span class="sxs-lookup"><span data-stu-id="1b585-152">In versions up to Excel 2003, the maximum number of arguments any function can take is 30.</span></span> <span data-ttu-id="1b585-153">Excel 2007 以降では、最大数は 255 です。</span><span class="sxs-lookup"><span data-stu-id="1b585-153">Starting in Excel 2007, the maximum number is 255.</span></span> <span data-ttu-id="1b585-154">引数の数が固定されている場合もありますし、最小値が必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1b585-154">Some require a fixed or minimum number of arguments.</span></span>  <br/> |
|<span data-ttu-id="1b585-155">8 </span><span class="sxs-lookup"><span data-stu-id="1b585-155">8</span></span>  <br/> |<span data-ttu-id="1b585-156">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="1b585-156">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="1b585-157">関数に渡された **XLOPER** または **XLOPER12** が正しくないか、使用された引数の種類が間違っています。</span><span class="sxs-lookup"><span data-stu-id="1b585-157">An invalid **XLOPER** or **XLOPER12** was passed to the function, or an argument of the wrong type was used.</span></span>  <br/> |
|<span data-ttu-id="1b585-158">16 </span><span class="sxs-lookup"><span data-stu-id="1b585-158">16</span></span>  <br/> |<span data-ttu-id="1b585-159">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="1b585-159">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="1b585-p111">スタック オーバーフローが発生しました。**xlStack** を使用して、スタックの残容量を監視します。大規模なローカル (自動) の配列や構造をスタック上で割り当てることを避け、可能な場合にはそれらを静的にします。(スタック オーバーフローが、検出されることなく発生する場合があることにご注意ください。)</span><span class="sxs-lookup"><span data-stu-id="1b585-p111">A stack overflow occurred. Use **xlStack** to monitor the amount of room left on the stack. Avoid allocating very large local (automatic) arrays and structures on the stack where possible; make them static. (Note that a stack overflow might occur without being detected.)  </span></span><br/> |
|<span data-ttu-id="1b585-164">32</span><span class="sxs-lookup"><span data-stu-id="1b585-164">32</span></span>  <br/> |<span data-ttu-id="1b585-165">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="1b585-165">**xlretFailed**</span></span> <br/> |<span data-ttu-id="1b585-p112">コマンドと等価の関数が失敗しました。これは、[マクロ エラーの警告] ダイアログボックスを表示するマクロ コマンドと等価です。</span><span class="sxs-lookup"><span data-stu-id="1b585-p112">A command-equivalent function failed. This is equivalent to a macro command displaying the macro error alert dialog box.</span></span>  <br/> |
|<span data-ttu-id="1b585-168">64</span><span class="sxs-lookup"><span data-stu-id="1b585-168">64</span></span>  <br/> |<span data-ttu-id="1b585-169">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="1b585-169">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="1b585-p113">現在のセルの後に再計算するようスケジュールされているために、まだ計算されていないセルを逆参照しようとしました。この場合、DLL は制御を即時に Excel に戻す必要があります。DLL が **xlFree** を呼び出すのが許可されるのは、終了する前のみです。C API に対するそれ以外のすべての呼び出しは許可されません。再計算されていないセルの値にアクセスできる関数とできない関数についての詳細は、「[Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b585-p113">An attempt was made to dereference a cell that has not been calculated yet, because it is scheduled to be recalculated after the current cell. In this case, the DLL should return control to Excel immediately. The DLL is permitted to call **xlFree** only before exiting. All other calls to the C API are not permitted. For more information about which functions can and cannot access the values of cells that have not been recalculated, see [Excel Commands, Functions, and States](excel-commands-functions-and-states.md).  </span></span><br/> |
|<span data-ttu-id="1b585-175">128</span><span class="sxs-lookup"><span data-stu-id="1b585-175">128</span></span>  <br/> |<span data-ttu-id="1b585-176">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="1b585-176">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="1b585-177">ブックの再計算がマルチ スレッドで実行中に、スレッド セーフではない、あるいはスレッド セーフでない可能性がある関数を呼び出そうとしました。</span><span class="sxs-lookup"><span data-stu-id="1b585-177">An attempt was made to call a function that is not, or might not be, thread safe during a multithreaded recalculation of the workbook.</span></span>  <br/> <span data-ttu-id="1b585-178">Excel 2007 以降、この値が返されるようになり、XLL ワークシート関数内でのみ、スレッド セーフとして宣言されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-178">Starting in Excel 2007, this value is returned, and only within XLL worksheet functions declared as thread safe.</span></span>  <br/> |
|<span data-ttu-id="1b585-179">256</span><span class="sxs-lookup"><span data-stu-id="1b585-179">256</span></span>  <br/> |<span data-ttu-id="1b585-180">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="1b585-180">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="1b585-181">非同期関数のハンドルが無効です。</span><span class="sxs-lookup"><span data-stu-id="1b585-181">The asynchronous function handle is invalid.</span></span>  <br/> <span data-ttu-id="1b585-182">この値は、Excel 2010 でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-182">This value is used only by Excel 2010.</span></span>  <br/> |
|<span data-ttu-id="1b585-183">512</span><span class="sxs-lookup"><span data-stu-id="1b585-183">512</span></span>  <br/> |<span data-ttu-id="1b585-184">**xlRetNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="1b585-184">**xlRetNotClusterSafe**</span></span> <br/> |<span data-ttu-id="1b585-185">クラスターでは、呼び出しはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1b585-185">The call is not supported on clusters.</span></span>  <br/> <span data-ttu-id="1b585-186">この値は、Excel 2010 でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-186">This value is used only by Excel 2010.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b585-187">備考</span><span class="sxs-lookup"><span data-stu-id="1b585-187">Remarks</span></span>

### <a name="valid-ifunction-values"></a><span data-ttu-id="1b585-188">有効な iFunction の値</span><span class="sxs-lookup"><span data-stu-id="1b585-188">Valid iFunction values</span></span>

<span data-ttu-id="1b585-189">有効な **iFunction** の値は、Xlcall.h ヘッダー ファイルまたは次の特殊関数のいずれかで定義される、任意の **xlf...** または **xlc...** 定数です。</span><span class="sxs-lookup"><span data-stu-id="1b585-189">Valid **iFunction** values are any of the **xlf...** or **xlc...** constants defined in the Xlcall.h header file or any of the following special functions.</span></span> 
  
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b585-190">**xlAbort**</span><span class="sxs-lookup"><span data-stu-id="1b585-190">**xlAbort**</span></span> <br/> |<span data-ttu-id="1b585-191">**xlEnableXLMsgs**</span><span class="sxs-lookup"><span data-stu-id="1b585-191">**xlEnableXLMsgs**</span></span> <br/> |<span data-ttu-id="1b585-192">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="1b585-192">**xlGetInst**</span></span> <br/> |<span data-ttu-id="1b585-193">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="1b585-193">**xlSheetNm**</span></span> <br/> |
|<span data-ttu-id="1b585-194">**xlCoerce**</span><span class="sxs-lookup"><span data-stu-id="1b585-194">**xlCoerce**</span></span> <br/> |<span data-ttu-id="1b585-195">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="1b585-195">**xlFree**</span></span> <br/> |<span data-ttu-id="1b585-196">**xlGetName**</span><span class="sxs-lookup"><span data-stu-id="1b585-196">**xlGetName**</span></span> <br/> |<span data-ttu-id="1b585-197">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="1b585-197">**xlStack**</span></span> <br/> |
|<span data-ttu-id="1b585-198">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="1b585-198">**xlDefineBinaryName**</span></span> <br/> |<span data-ttu-id="1b585-199">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="1b585-199">**xlGetBinaryName**</span></span> <br/> |<span data-ttu-id="1b585-200">**xlSet**</span><span class="sxs-lookup"><span data-stu-id="1b585-200">**xlSet**</span></span> <br/> |<span data-ttu-id="1b585-201">**xlUDF**</span><span class="sxs-lookup"><span data-stu-id="1b585-201">**xlUDF**</span></span> <br/> |
|<span data-ttu-id="1b585-202">**xlDisableXLMsgs**</span><span class="sxs-lookup"><span data-stu-id="1b585-202">**xlDisableXLMsgs**</span></span> <br/> |<span data-ttu-id="1b585-203">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="1b585-203">**xlGetHwnd**</span></span> <br/> |<span data-ttu-id="1b585-204">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="1b585-204">**xlSheetId**</span></span> <br/> ||
   
### <a name="different-types-of-functions"></a><span data-ttu-id="1b585-205">関数のさまざまな種類</span><span class="sxs-lookup"><span data-stu-id="1b585-205">Different Types of Functions</span></span>

 <span data-ttu-id="1b585-p114">**Excel4** と **Excel12** は、関数の 3 つのクラスを識別します。関数は、Excel が DLL を呼び出す際の 3 種類の状態に基づいて分類されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-p114">**Excel4** and **Excel12** distinguish among three classes of functions. The functions are classified according to the three states in which Excel might call the DLL.</span></span> 
  
- <span data-ttu-id="1b585-208">クラス 1 は、DLL が再計算の結果としてワークシートから呼び出された場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-208">Class 1 applies when the DLL is called from a worksheet as a result of recalculation.</span></span> 
    
- <span data-ttu-id="1b585-209">クラス 2 は、DLL が関数マクロ内部から呼び出された場合、またはタイプ テキストで番号記号 (#) を付けて登録されたワークシートから呼び出された場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b585-209">Class 2 applies when the DLL is called from within a function macro or from a worksheet where it was registered with a number sign (#) in the type text.</span></span>
    
- <span data-ttu-id="1b585-p115">クラス 3は、DLL が、オブジェクト、マクロ、メニュー、ツールバー、ショートカット キー、**ExecuteExcel4Macro** メソッドから呼び出された場合に適用されます。また、**ツール、マクロ、実行**の各コマンドから呼び出された場合にも適用されます。詳細は、「[Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b585-p115">Class 3 applies when a DLL is called from an object, macro, menu, toolbar, shortcut key, **ExecuteExcel4Macro** method, or the **Tools/Macro/Run** command. For more information, see [Excel Commands, Functions, and States](excel-commands-functions-and-states.md).</span></span>
    
<span data-ttu-id="1b585-212">次の表は、各クラスでどの関数が有効かを示しています。</span><span class="sxs-lookup"><span data-stu-id="1b585-212">The following table shows what functions are valid in each class.</span></span>
  
|<span data-ttu-id="1b585-213">**Class 1**</span><span class="sxs-lookup"><span data-stu-id="1b585-213">**Class 1**</span></span>|<span data-ttu-id="1b585-214">**Class 2**</span><span class="sxs-lookup"><span data-stu-id="1b585-214">**Class 2**</span></span>|<span data-ttu-id="1b585-215">**Class 3**</span><span class="sxs-lookup"><span data-stu-id="1b585-215">**Class 3**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b585-216">任意のワークシート関数</span><span class="sxs-lookup"><span data-stu-id="1b585-216">Any worksheet function</span></span>  <br/> <span data-ttu-id="1b585-217">**xlSet** を除く、任意の XLL 専用の **xl...** 関数。</span><span class="sxs-lookup"><span data-stu-id="1b585-217">Any XLL-only **xl...** function except **xlSet**.</span></span>  <br/> <span data-ttu-id="1b585-218">**xlfCaller**</span><span class="sxs-lookup"><span data-stu-id="1b585-218">**xlfCaller**</span></span> <br/> |<span data-ttu-id="1b585-219">任意のワークシート関数</span><span class="sxs-lookup"><span data-stu-id="1b585-219">Any worksheet function</span></span>  <br/> <span data-ttu-id="1b585-220">**xlSet** を除く、任意の **xl...** 関数。</span><span class="sxs-lookup"><span data-stu-id="1b585-220">Any **xl...** function except **xlSet**.</span></span>  <br/> <span data-ttu-id="1b585-221">ワークスペースまたは開いているどのブックにも影響する操作を実行せずに値を返す、マクロ シート関数 (**xlfCaller** を含む)。</span><span class="sxs-lookup"><span data-stu-id="1b585-221">Macro sheet functions, including **xlfCaller**, that return a value but perform no action that affects the workspace or any open workbook.</span></span>  <br/> |<span data-ttu-id="1b585-222">任意の関数 (**xlSet** を含む) およびコマンド等価関数。</span><span class="sxs-lookup"><span data-stu-id="1b585-222">Any function, including **xlSet** and command-equivalent functions.</span></span>  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a><span data-ttu-id="1b585-223">コマンドと等価の関数のダイアログ ボックスの表示</span><span class="sxs-lookup"><span data-stu-id="1b585-223">Displaying the Dialog Box for a Command-Equivalent Function</span></span>

<span data-ttu-id="1b585-p116">コマンドと等価の関数がダイアログ ボックスと関連付けられている場合、**iFunction** の **xlPrompt** ビットを設定できます。これは、コマンドを実行する前に、Excel が適切なダイアログ ボックスを表示することを意味します。</span><span class="sxs-lookup"><span data-stu-id="1b585-p116">If a command-equivalent function has an associated dialog box, you can set the **xlPrompt** bit in **iFunction**. This means that Excel displays the appropriate dialog box before carrying out the command.</span></span>
  
### <a name="writing-international-dlls"></a><span data-ttu-id="1b585-226">International DLL の作成</span><span class="sxs-lookup"><span data-stu-id="1b585-226">Writing International DLLs</span></span>

<span data-ttu-id="1b585-p117">**iFunction** の **xlIntl** ビットを設定する場合、その関数またはコマンドは、インターナショナル マクロ シートから呼び出されている場合と同様に実行されます。これは、そのコマンドが国際バージョン (ローカライズされたバージョン) で実行されているとしても、Excel の米国バージョンと同様に動作するという意味です。</span><span class="sxs-lookup"><span data-stu-id="1b585-p117">If you set the **xlIntl** bit in **iFunction**, the function or command is carried out as if it were being called from an International Macro Sheet. This means that the command behaves as it would on the U.S. version of Excel, even if it is running on an international (localized) version.</span></span>
  
### <a name="xlretuncalced-or-xlretabort"></a><span data-ttu-id="1b585-229">xlretUncalced または xlretAbort</span><span class="sxs-lookup"><span data-stu-id="1b585-229">xlretUncalced or xlretAbort</span></span>

<span data-ttu-id="1b585-p118">戻り値の 1 つを受け取った後、DLL は直ちにクリーンアップを行い、制御を Excel に返す必要があります。**xlFree** 以外では、戻り値の 1 つを受け取った後、C API 経由での Excel へのコールバックはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="1b585-p118">After receiving one of these return values, your DLL must clean up and return control to Excel immediately. Callbacks into Excel via the C API, except **xlFree**, are disabled after receiving one of these return values.</span></span>
  
## <a name="example"></a><span data-ttu-id="1b585-232">例</span><span class="sxs-lookup"><span data-stu-id="1b585-232">Example</span></span>

<span data-ttu-id="1b585-233">次の例は、呼び出し元のセルを選択するために、**Excel12** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b585-233">The following example uses the **Excel12** function to select the cell from which it was called.</span></span> 
  
<span data-ttu-id="1b585-234">このコード例は、Excel 2010 XLL SDK で提供されている、より大きな例の一部です。例は、SDK がインストールされている場所の次の位置にあります:</span><span class="sxs-lookup"><span data-stu-id="1b585-234">This code example is part of a larger example provided in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span>
  
<span data-ttu-id="1b585-235">\Samples\Example\Example.c。</span><span class="sxs-lookup"><span data-stu-id="1b585-235">\Samples\Example\Example.c.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b585-236">この関数は、コマンド マクロ (xlcSelect) を呼び出し、それゆえに、それが XLM マクロ シートから呼び出された場合にのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="1b585-236">This function calls a command macro (xlcSelect) and, therefore, works only if it is called from an XLM macro sheet.</span></span> 
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="1b585-237">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b585-237">See also</span></span>



[<span data-ttu-id="1b585-238">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="1b585-238">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)

