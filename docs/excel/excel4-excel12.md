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
- excel4 関数 [excel 2007] Excel12 関数 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1c2c775cc7c5b051e4a1381df09ef29e79e2aca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798867"
---
# <a name="excel4excel12"></a><span data-ttu-id="737ae-104">Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="737ae-104">Excel4/Excel12</span></span>

 <span data-ttu-id="737ae-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="737ae-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="737ae-106">Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 専用の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。</span><span class="sxs-lookup"><span data-stu-id="737ae-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL/XLL or code resource.</span></span>
  
<span data-ttu-id="737ae-107">すべての最新バージョンの Excel では、 **Excel4**をサポートします。</span><span class="sxs-lookup"><span data-stu-id="737ae-107">All recent versions of Excel support **Excel4**.</span></span> <span data-ttu-id="737ae-108">Excel 2007 以降では、 **Excel12**がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="737ae-108">Starting in Excel 2007, **Excel12** is supported.</span></span> 
  
<span data-ttu-id="737ae-p102">�����̊֐��́AExcel �� DLL �܂��� XLL �ɐ����n���Ă���ꍇ�ɂ̂݁A�Ăяo�����Ƃ��ł��܂��B�����̊֐��́AExcel �� Visual Basic for Applications (VBA) �ւ̌Ăяo�����ĊԐړI�ɐ����n���Ă���ꍇ�ɂ�Ăяo����邱�Ƃ�����܂��B����ȊO�̎��ɁA�����̊֐���Ăяo�����Ƃ͂ł��܂���B���Ƃ��΁A[DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) �֐��ɑ΂���Ăяo���̊Ԃ�A�I�y���[�e�B���O �V�X�e���� DLL ��Ăяo���Ă���Ƃ���A�����̊֐���Ăяo�����Ƃ͂ł��܂���BDLL ���쐬�����X���b�h�����A�����̊֐���Ăяo�����Ƃ͂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="737ae-p102">These functions can be called only when Excel has passed control to the DLL or XLL. They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA). They cannot be called at any other time. For example, they cannot be called during calls to the [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="737ae-113">**Excel4**と**Excel12**関数は、スタック上の可変長リストとして、引数を受け取るが、 [Excel4v と Excel12v](excel4v-excel12v.md)関数は、配列として引数をそのまま使用します。</span><span class="sxs-lookup"><span data-stu-id="737ae-113">The [Excel4v and Excel12v](excel4v-excel12v.md) functions accept their arguments as an array, whereas the **Excel4** and **Excel12** functions accept their arguments as a variable-length list on the stack.</span></span> <span data-ttu-id="737ae-114">その他のすべての点では、 **Excel4**の**Excel4v**と同じ動作し、 **Excel12**の**Excel12v**と同じ動作です。</span><span class="sxs-lookup"><span data-stu-id="737ae-114">In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="737ae-115">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="737ae-115">Parameters</span></span>

 <span data-ttu-id="737ae-116">_iFunction_(**int**)</span><span class="sxs-lookup"><span data-stu-id="737ae-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="737ae-p104">�Ăяo���R�}���h�A�֐��A�܂��͓���֐���������l�B _iFunction_ �̗L���Ȓl�̈ꗗ�́A���̉���Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="737ae-p104">A number that indicates the command, function, or special function you want to call. For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="737ae-119">_pxRes_(**LPXLOPER**または**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="737ae-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="737ae-120">( **Excel4**) とは、 **XLOPER**を**XLOPER12** ( **Excel12**) と評価された関数の結果を保持するへのポインター。</span><span class="sxs-lookup"><span data-stu-id="737ae-120">A pointer to an **XLOPER** (with **Excel4**) or an **XLOPER12** (with **Excel12**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="737ae-121">_iCount_(**int**)</span><span class="sxs-lookup"><span data-stu-id="737ae-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="737ae-122">関数に渡されるそれ以降の引数の数。</span><span class="sxs-lookup"><span data-stu-id="737ae-122">The number of subsequent arguments that will be passed to the function.</span></span> <span data-ttu-id="737ae-123">2003 までのバージョンの Excel は 0 から 30 までの任意の数になります。</span><span class="sxs-lookup"><span data-stu-id="737ae-123">In versions of Excel up to 2003, this can be any number from 0 through 30.</span></span> <span data-ttu-id="737ae-124">Excel 2007 以降では、これは、0 255 までからの任意の数。</span><span class="sxs-lookup"><span data-stu-id="737ae-124">Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="737ae-125">_argument1、._(**LPXLOPER**または**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="737ae-125">_argument1, ..._ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="737ae-126">関数の省略可能な引数です。</span><span class="sxs-lookup"><span data-stu-id="737ae-126">The optional arguments to the function.</span></span> <span data-ttu-id="737ae-127">すべての引数は、 **XLOPER**または**XLOPER12**の値へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="737ae-127">All arguments must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="737ae-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="737ae-128">Return value</span></span>

<span data-ttu-id="737ae-129">以下の整数 (**int**) の値のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="737ae-129">Returns one of the following integer (**int**) values.</span></span>
  
|<span data-ttu-id="737ae-130">**値**</span><span class="sxs-lookup"><span data-stu-id="737ae-130">**Value**</span></span>|<span data-ttu-id="737ae-131">**リターン コード**</span><span class="sxs-lookup"><span data-stu-id="737ae-131">**Return code**</span></span>|<span data-ttu-id="737ae-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="737ae-132">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="737ae-133">0</span><span class="sxs-lookup"><span data-stu-id="737ae-133">0</span></span>  <br/> |<span data-ttu-id="737ae-134">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="737ae-134">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="737ae-135">関数は正常に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-135">The function was called successfully.</span></span> <span data-ttu-id="737ae-136">関数が、Excel のエラー値を返さなかったことはありません。アウトを見つけるには、型と結果の_pxRes_パラメーターの値を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="737ae-136">This does not mean that the function did not return an Excel error value; to find that out, you must look at the type and value of the resulting  _pxRes_ parameter.</span></span>  <br/> |
|<span data-ttu-id="737ae-137">1</span><span class="sxs-lookup"><span data-stu-id="737ae-137">1</span></span>  <br/> |<span data-ttu-id="737ae-138">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="737ae-138">**xlretAbort**</span></span> <br/> |<span data-ttu-id="737ae-139">コマンドまたは関数が異常終了しました (内部アボート)。</span><span class="sxs-lookup"><span data-stu-id="737ae-139">The command or function was terminated abnormally (internal abort).</span></span> <span data-ttu-id="737ae-140">これは、XLM マクロ シートで**CLOSE**を呼び出すことによって自動的に閉じる場合、または Excel がメモリが不足している場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="737ae-140">This can occur if an XLM macro sheet closes itself by calling **CLOSE**, or if Excel is out of memory.</span></span> <span data-ttu-id="737ae-141">Excel では、このエラーが返された場合、呼び出し元の関数は即座に終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="737ae-141">If Excel returns this error, the calling function must exit immediately.</span></span> <span data-ttu-id="737ae-142">DLL は、 **xlFree**を終了する前にのみ呼び出すことが許可されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-142">The DLL is permitted to call **xlFree** only before exiting.</span></span> <span data-ttu-id="737ae-143">他のすべての c 言語の API 呼び出しは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="737ae-143">All other calls to the C API are not permitted.</span></span> <span data-ttu-id="737ae-144">ユーザーは [**ファイル**] メニューの [**上書き保存**] コマンドを使用して対話的に作業を保存できます。</span><span class="sxs-lookup"><span data-stu-id="737ae-144">The user can save any work interactively by using the **Save** command on the **File** menu.</span></span>  <br/> |
|<span data-ttu-id="737ae-145">2</span><span class="sxs-lookup"><span data-stu-id="737ae-145">2</span></span>  <br/> |<span data-ttu-id="737ae-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="737ae-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="737ae-p109">指定された関数の数が正しくありません。Xlcall.h ヘッダー ファイルの定数を使用している場合、実行中の Excel のバージョンでサポートされていない何かを呼び出さない限り、これが起こることはありません。</span><span class="sxs-lookup"><span data-stu-id="737ae-p109">An invalid function number was supplied. If you are using constants from the Xlcall.h header file, this should not occur unless you are calling something that is not supported in the version of Excel you are running.</span></span>  <br/> |
|<span data-ttu-id="737ae-149">4</span><span class="sxs-lookup"><span data-stu-id="737ae-149">4</span></span>  <br/> |<span data-ttu-id="737ae-150">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="737ae-150">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="737ae-151">無効な数の引数が入力されました。</span><span class="sxs-lookup"><span data-stu-id="737ae-151">An invalid number of arguments was entered.</span></span> <span data-ttu-id="737ae-152">Excel 2003 までのバージョンでは、関数が受け取ることができます引数の最大数は 30 です。</span><span class="sxs-lookup"><span data-stu-id="737ae-152">In versions up to Excel 2003, the maximum number of arguments any function can take is 30.</span></span> <span data-ttu-id="737ae-153">Excel 2007 以降では、最大数は、255 です。</span><span class="sxs-lookup"><span data-stu-id="737ae-153">Starting in Excel 2007, the maximum number is 255.</span></span> <span data-ttu-id="737ae-154">いくつかは、引数の数が固定または最小値を必要があります。</span><span class="sxs-lookup"><span data-stu-id="737ae-154">Some require a fixed or minimum number of arguments.</span></span>  <br/> |
|<span data-ttu-id="737ae-155">8</span><span class="sxs-lookup"><span data-stu-id="737ae-155">8</span></span>  <br/> |<span data-ttu-id="737ae-156">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="737ae-156">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="737ae-157">無効の**XLOPER**または**XLOPER12**は、関数に渡されたか、間違った型の引数が使用されました。</span><span class="sxs-lookup"><span data-stu-id="737ae-157">An invalid **XLOPER** or **XLOPER12** was passed to the function, or an argument of the wrong type was used.</span></span>  <br/> |
|<span data-ttu-id="737ae-158">16</span><span class="sxs-lookup"><span data-stu-id="737ae-158">16</span></span>  <br/> |<span data-ttu-id="737ae-159">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="737ae-159">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="737ae-160">スタック オーバーフローが発生しました。</span><span class="sxs-lookup"><span data-stu-id="737ae-160">A stack overflow occurred.</span></span> <span data-ttu-id="737ae-161">**XlStack**を使用すると、スタック上の部屋の左側の量を監視できます。</span><span class="sxs-lookup"><span data-stu-id="737ae-161">Use **xlStack** to monitor the amount of room left on the stack.</span></span> <span data-ttu-id="737ae-162">可能な場合は、ローカル (自動) の非常に大きな配列とスタック上の構造体の割り当てを回避します。静的となってください。</span><span class="sxs-lookup"><span data-stu-id="737ae-162">Avoid allocating very large local (automatic) arrays and structures on the stack where possible; make them static.</span></span> <span data-ttu-id="737ae-163">(スタック オーバーフローが検出されることがなく発生する可能性に注意してください)。</span><span class="sxs-lookup"><span data-stu-id="737ae-163">(Note that a stack overflow might occur without being detected.)</span></span>  <br/> |
|<span data-ttu-id="737ae-164">32</span><span class="sxs-lookup"><span data-stu-id="737ae-164">32</span></span>  <br/> |<span data-ttu-id="737ae-165">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="737ae-165">**xlretFailed**</span></span> <br/> |<span data-ttu-id="737ae-p112">コマンドと等価の関数が失敗しました。これは、[マクロ エラーの警告] ダイアログボックスを表示するマクロ コマンドと等価です。</span><span class="sxs-lookup"><span data-stu-id="737ae-p112">A command-equivalent function failed. This is equivalent to a macro command displaying the macro error alert dialog box.</span></span>  <br/> |
|<span data-ttu-id="737ae-168">64</span><span class="sxs-lookup"><span data-stu-id="737ae-168">64</span></span>  <br/> |<span data-ttu-id="737ae-169">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="737ae-169">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="737ae-170">現在のセルの後に再計算することになる予定ですので、まだ計算されていないセルを逆参照しようとしました。</span><span class="sxs-lookup"><span data-stu-id="737ae-170">An attempt was made to dereference a cell that has not been calculated yet, because it is scheduled to be recalculated after the current cell.</span></span> <span data-ttu-id="737ae-171">この例では、DLL コントロールを Excel にすぐに返すか。</span><span class="sxs-lookup"><span data-stu-id="737ae-171">In this case, the DLL should return control to Excel immediately.</span></span> <span data-ttu-id="737ae-172">DLL は、 **xlFree**を終了する前にのみ呼び出すことが許可されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-172">The DLL is permitted to call **xlFree** only before exiting.</span></span> <span data-ttu-id="737ae-173">他のすべての c 言語の API 呼び出しは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="737ae-173">All other calls to the C API are not permitted.</span></span> <span data-ttu-id="737ae-174">先の詳細については関数およびできますが再計算されていない、 [Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)を表示するセルの値にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="737ae-174">For more information about which functions can and cannot access the values of cells that have not been recalculated, see [Excel Commands, Functions, and States](excel-commands-functions-and-states.md).</span></span>  <br/> |
|<span data-ttu-id="737ae-175">128</span><span class="sxs-lookup"><span data-stu-id="737ae-175">128</span></span>  <br/> |<span data-ttu-id="737ae-176">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="737ae-176">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="737ae-177">ブックの再計算がマルチ スレッドで実行中に、スレッド セーフではない、あるいはスレッド セーフでない可能性がある関数を呼び出そうとしました。</span><span class="sxs-lookup"><span data-stu-id="737ae-177">An attempt was made to call a function that is not, or might not be, thread safe during a multithreaded recalculation of the workbook.</span></span>  <br/> <span data-ttu-id="737ae-178">Excel 2007 以降では、この値が返されると同様のスレッド セーフで XLL ワークシート関数の宣言内でのみです。</span><span class="sxs-lookup"><span data-stu-id="737ae-178">Starting in Excel 2007, this value is returned, and only within XLL worksheet functions declared as thread safe.</span></span>  <br/> |
|<span data-ttu-id="737ae-179">256</span><span class="sxs-lookup"><span data-stu-id="737ae-179">256</span></span>  <br/> |<span data-ttu-id="737ae-180">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="737ae-180">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="737ae-181">非同期関数のハンドルが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="737ae-181">The asynchronous function handle is invalid.</span></span>  <br/> <span data-ttu-id="737ae-182">この値は、Excel 2010 でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-182">This value is used only by Excel 2010.</span></span>  <br/> |
|<span data-ttu-id="737ae-183">512</span><span class="sxs-lookup"><span data-stu-id="737ae-183">512</span></span>  <br/> |<span data-ttu-id="737ae-184">**xlRetNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="737ae-184">**xlRetNotClusterSafe**</span></span> <br/> |<span data-ttu-id="737ae-185">クラスターでは、呼び出しはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="737ae-185">The call is not supported on clusters.</span></span>  <br/> <span data-ttu-id="737ae-186">この値は、Excel 2010 でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-186">This value is used only by Excel 2010.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="737ae-187">備考</span><span class="sxs-lookup"><span data-stu-id="737ae-187">Remarks</span></span>

### <a name="valid-ifunction-values"></a><span data-ttu-id="737ae-188">有効な iFunction の値</span><span class="sxs-lookup"><span data-stu-id="737ae-188">Valid iFunction values</span></span>

<span data-ttu-id="737ae-189">有効な**iFunction**の値は、 **xlf.** または**xlc.** Xlcall.h ヘッダー ファイルまたは特殊な関数を次のいずれかで定義されている定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="737ae-189">Valid **iFunction** values are any of the **xlf...** or **xlc...** constants defined in the Xlcall.h header file or any of the following special functions.</span></span> 
  
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="737ae-190">**xlAbort**</span><span class="sxs-lookup"><span data-stu-id="737ae-190">**xlAbort**</span></span> <br/> |<span data-ttu-id="737ae-191">**xlEnableXLMsgs**</span><span class="sxs-lookup"><span data-stu-id="737ae-191">**xlEnableXLMsgs**</span></span> <br/> |<span data-ttu-id="737ae-192">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="737ae-192">**xlGetInst**</span></span> <br/> |<span data-ttu-id="737ae-193">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="737ae-193">**xlSheetNm**</span></span> <br/> |
|<span data-ttu-id="737ae-194">**xlCoerce**</span><span class="sxs-lookup"><span data-stu-id="737ae-194">**xlCoerce**</span></span> <br/> |<span data-ttu-id="737ae-195">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="737ae-195">**xlFree**</span></span> <br/> |<span data-ttu-id="737ae-196">**xlGetName**</span><span class="sxs-lookup"><span data-stu-id="737ae-196">**xlGetName**</span></span> <br/> |<span data-ttu-id="737ae-197">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="737ae-197">**xlStack**</span></span> <br/> |
|<span data-ttu-id="737ae-198">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="737ae-198">**xlDefineBinaryName**</span></span> <br/> |<span data-ttu-id="737ae-199">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="737ae-199">**xlGetBinaryName**</span></span> <br/> |<span data-ttu-id="737ae-200">**xlSet**</span><span class="sxs-lookup"><span data-stu-id="737ae-200">**xlSet**</span></span> <br/> |<span data-ttu-id="737ae-201">**xlUDF**</span><span class="sxs-lookup"><span data-stu-id="737ae-201">**xlUDF**</span></span> <br/> |
|<span data-ttu-id="737ae-202">**xlDisableXLMsgs**</span><span class="sxs-lookup"><span data-stu-id="737ae-202">**xlDisableXLMsgs**</span></span> <br/> |<span data-ttu-id="737ae-203">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="737ae-203">**xlGetHwnd**</span></span> <br/> |<span data-ttu-id="737ae-204">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="737ae-204">**xlSheetId**</span></span> <br/> ||
   
### <a name="different-types-of-functions"></a><span data-ttu-id="737ae-205">関数のさまざまな種類</span><span class="sxs-lookup"><span data-stu-id="737ae-205">Different Types of Functions</span></span>

 <span data-ttu-id="737ae-206">**Excel4**と**Excel12**関数の 3 つのクラスを区別します。</span><span class="sxs-lookup"><span data-stu-id="737ae-206">**Excel4** and **Excel12** distinguish among three classes of functions.</span></span> <span data-ttu-id="737ae-207">関数は、Excel が、DLL を呼び出す場合があります、3 つの状態によって分類されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-207">The functions are classified according to the three states in which Excel might call the DLL.</span></span> 
  
- <span data-ttu-id="737ae-208">クラス 1 は、DLL が再計算の結果としてワークシートから呼び出された場合に適用されます。 </span><span class="sxs-lookup"><span data-stu-id="737ae-208">Class 1 applies when the DLL is called from a worksheet as a result of recalculation.</span></span> 
    
- <span data-ttu-id="737ae-209">クラス 2 は、DLL が関数マクロ内部から呼び出された場合、またはタイプ テキストで番号記号 (#) を付けて登録されたワークシートから呼び出された場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-209">Class 2 applies when the DLL is called from within a function macro or from a worksheet where it was registered with a number sign (#) in the type text.</span></span>
    
- <span data-ttu-id="737ae-210">クラス 3 では、DLL がオブジェクト、マクロ、メニューのツールバー、ショートカット キー、 **ExecuteExcel4Macro**メソッド、または**ツール/マクロ/実行**] コマンドから呼び出されたときに適用されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-210">Class 3 applies when a DLL is called from an object, macro, menu, toolbar, shortcut key, **ExecuteExcel4Macro** method, or the **Tools/Macro/Run** command.</span></span> <span data-ttu-id="737ae-211">詳細については、 [Excel のコマンド、関数、および状態](excel-commands-functions-and-states.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="737ae-211">For more information, see [Excel Commands, Functions, and States](excel-commands-functions-and-states.md).</span></span>
    
<span data-ttu-id="737ae-212">次の表は、各クラスでどの関数が有効かを示しています。</span><span class="sxs-lookup"><span data-stu-id="737ae-212">The following table shows what functions are valid in each class.</span></span>
  
|<span data-ttu-id="737ae-213">**クラス 1**</span><span class="sxs-lookup"><span data-stu-id="737ae-213">**Class 1**</span></span>|<span data-ttu-id="737ae-214">**クラス 2**</span><span class="sxs-lookup"><span data-stu-id="737ae-214">**Class 2**</span></span>|<span data-ttu-id="737ae-215">**クラス 3**</span><span class="sxs-lookup"><span data-stu-id="737ae-215">**Class 3**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="737ae-216">任意のワークシート関数</span><span class="sxs-lookup"><span data-stu-id="737ae-216">Any worksheet function</span></span>  <br/> <span data-ttu-id="737ae-217">**XlSet**を除く任意の xll ファイル専用の**xl.** 関数です。</span><span class="sxs-lookup"><span data-stu-id="737ae-217">Any XLL-only **xl...** function except **xlSet**.</span></span>  <br/> <span data-ttu-id="737ae-218">**xlfCaller**</span><span class="sxs-lookup"><span data-stu-id="737ae-218">**xlfCaller**</span></span> <br/> |<span data-ttu-id="737ae-219">任意のワークシート関数</span><span class="sxs-lookup"><span data-stu-id="737ae-219">Any worksheet function</span></span>  <br/> <span data-ttu-id="737ae-220">**XlSet**を除くすべての**xl.** 関数です。</span><span class="sxs-lookup"><span data-stu-id="737ae-220">Any **xl...** function except **xlSet**.</span></span>  <br/> <span data-ttu-id="737ae-221">マクロ シート機能、 **xlfCaller**を含む値を返しますが、ワークスペースに影響する操作、または開いているブックを実行しません。</span><span class="sxs-lookup"><span data-stu-id="737ae-221">Macro sheet functions, including **xlfCaller**, that return a value but perform no action that affects the workspace or any open workbook.</span></span>  <br/> |<span data-ttu-id="737ae-222">**XlSet**と同じコマンド ・関数を含む関数、です。</span><span class="sxs-lookup"><span data-stu-id="737ae-222">Any function, including **xlSet** and command-equivalent functions.</span></span>  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a><span data-ttu-id="737ae-223">コマンドと等価の関数のダイアログ ボックスの表示</span><span class="sxs-lookup"><span data-stu-id="737ae-223">Displaying the Dialog Box for a Command-Equivalent Function</span></span>

<span data-ttu-id="737ae-224">コマンドに相当する関数に、関連付けられたダイアログ ボックスがある場合は、 **iFunction**で**xlPrompt**ビットを設定できます。</span><span class="sxs-lookup"><span data-stu-id="737ae-224">If a command-equivalent function has an associated dialog box, you can set the **xlPrompt** bit in **iFunction**.</span></span> <span data-ttu-id="737ae-225">つまり、あるコマンドを実行する前に適切なダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="737ae-225">This means that Excel displays the appropriate dialog box before carrying out the command.</span></span>
  
### <a name="writing-international-dlls"></a><span data-ttu-id="737ae-226">International DLL の作成</span><span class="sxs-lookup"><span data-stu-id="737ae-226">Writing International DLLs</span></span>

<span data-ttu-id="737ae-227">**IFunction**に**xlIntl**ビットを設定すると、関数やコマンドが実行、インターナショナル マクロ シートから呼び出されているされた場合と同様です。</span><span class="sxs-lookup"><span data-stu-id="737ae-227">If you set the **xlIntl** bit in **iFunction**, the function or command is carried out as if it were being called from an International Macro Sheet.</span></span> <span data-ttu-id="737ae-228">つまり、コマンドと動作を米国のバージョンの Excel では、国際 (ローカライズされた) バージョンで実行されている場合でも。</span><span class="sxs-lookup"><span data-stu-id="737ae-228">This means that the command behaves as it would on the U.S. version of Excel, even if it is running on an international (localized) version.</span></span>
  
### <a name="xlretuncalced-or-xlretabort"></a><span data-ttu-id="737ae-229">xlretUncalced または xlretAbort</span><span class="sxs-lookup"><span data-stu-id="737ae-229">xlretUncalced or xlretAbort</span></span>

<span data-ttu-id="737ae-230">、これらの戻り値のいずれかを受信した後、DLL する必要がありますをクリーンアップし、すぐにコントロールを Excel に返します。</span><span class="sxs-lookup"><span data-stu-id="737ae-230">After receiving one of these return values, your DLL must clean up and return control to Excel immediately.</span></span> <span data-ttu-id="737ae-231">これらの戻り値のいずれかを受信した後は、 **xlFree**を除いて、C API を使用して Excel にコールバックが無効になります。</span><span class="sxs-lookup"><span data-stu-id="737ae-231">Callbacks into Excel via the C API, except **xlFree**, are disabled after receiving one of these return values.</span></span>
  
## <a name="example"></a><span data-ttu-id="737ae-232">例</span><span class="sxs-lookup"><span data-stu-id="737ae-232">Example</span></span>

<span data-ttu-id="737ae-233">次の例では、 **Excel12**関数を使用して、呼び出し元のセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="737ae-233">The following example uses the **Excel12** function to select the cell from which it was called.</span></span> 
  
<span data-ttu-id="737ae-234">このコード例は、SDK がインストールされている次の場所に、Excel 2010 XLL SDK で提供されている大きな例の一部です。</span><span class="sxs-lookup"><span data-stu-id="737ae-234">This code example is part of a larger example provided in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span>
  
<span data-ttu-id="737ae-235">\Samples\Example\Example.c。</span><span class="sxs-lookup"><span data-stu-id="737ae-235">\Samples\Example\Example.c.</span></span>
  
> [!NOTE]
> <span data-ttu-id="737ae-236">この関数は、コマンド マクロ (xlcSelect) を呼び出し、それゆえに、それが XLM マクロ シートから呼び出された場合にのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="737ae-236">This function calls a command macro (xlcSelect) and, therefore, works only if it is called from an XLM macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="737ae-237">関連項目</span><span class="sxs-lookup"><span data-stu-id="737ae-237">See also</span></span>



[<span data-ttu-id="737ae-238">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="737ae-238">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)

