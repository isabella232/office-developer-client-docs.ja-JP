---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel function [excel 2007],Excel12f function [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310914"
---
# <a name="excelexcel12f"></a><span data-ttu-id="e5408-104">Excel/Excel12f</span><span class="sxs-lookup"><span data-stu-id="e5408-104">Excel/Excel12f</span></span>

 <span data-ttu-id="e5408-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e5408-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e5408-p101">Framework library functions. **Excel** is a wrapper for the [Excel4](excel4-excel12.md) function. **Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function. Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed. If an error occurs, each prints a debug message. When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="e5408-p101">Framework library functions. **Excel** is a wrapper for the [Excel4](excel4-excel12.md) function. **Excel12f** is a wrapper for the [Excel12](excel4-excel12.md) function. Each checks to see that none of the arguments is zero, which would indicate that the creation of a temporary **XLOPER** or **XLOPER12** failed. If an error occurs, each prints a debug message. When finished, each frees all temporary memory that might have been created for temporary **XLOPER**s and **XLOPER12**s.</span></span>
  
 <span data-ttu-id="e5408-p102">**Excel12f**から Excel 2007 C API ライブラリ以降の DLL からのみ呼び出すことができます。さらに、Excel 2007 以降で起動したときのみ動作し、それ以外は **xlretFailed** で失敗します。</span><span class="sxs-lookup"><span data-stu-id="e5408-p102">**Excel12f** can only be called from a DLL starting with the Excel 2007 C API library. Furthermore, it only works when running starting with Excel 2007, and fails with **xlretFailed** otherwise.</span></span> 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a><span data-ttu-id="e5408-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5408-114">Parameters</span></span>

 <span data-ttu-id="e5408-115">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="e5408-115">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="e5408-p103">呼び出すコマンドまたは関数を示す数値。詳細については、「[Excel4/Excel12](excel4-excel12.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5408-p103">A number indicating the command or function you want to call. For more information, see [Excel4/Excel12](excel4-excel12.md).</span></span>
  
 <span data-ttu-id="e5408-118">_pxRes_</span><span class="sxs-lookup"><span data-stu-id="e5408-118">_pxRes_</span></span>
  
<span data-ttu-id="e5408-p104">評価された関数の結果のポインター。結果に示されるメモリはすべて、Excel によって割り当てられ、不要になったら [xlFree](xlfree.md) を呼び出して解放するか、または Excel に戻す場合は **xlbitXLFree** を設定して解放します。</span><span class="sxs-lookup"><span data-stu-id="e5408-p104">A pointer to result of the evaluated function. Any memory pointed to in the result will have been allocated by Excel and should be freed in a call to [xlFree](xlfree.md) once it is no longer needed, or by setting **xlbitXLFree** if returning it to Excel.</span></span> 
  
 <span data-ttu-id="e5408-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="e5408-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="e5408-p105">関数に渡される引数の数。Excel 2007 以降、引数の数は 255 に制限されています。それ以前のバージョンでは引数の数は 30 に制限されています。</span><span class="sxs-lookup"><span data-stu-id="e5408-p105">The number of arguments that will be passed to the function. Starting in Excel 2007, the limit is 255 arguments. In earlier versions, the limit is 30.</span></span>
  
 <span data-ttu-id="e5408-125">_argument1, ..._</span><span class="sxs-lookup"><span data-stu-id="e5408-125">_argument1, ..._</span></span>
  
<span data-ttu-id="e5408-p106">省略可能な、関数の引数。すべての引数は、**Excel** の場合は **XLOPER** へのポインター、**Excel12f** の場合は **XLOPER12** へのポインターにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5408-p106">The optional arguments to the function. All arguments must be pointers to **XLOPER**s in the case of **Excel**, or **XLOPER12**s in the case of **Excel12f**.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e5408-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="e5408-128">Return value</span></span>

<span data-ttu-id="e5408-p107">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**. See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes. In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span><span class="sxs-lookup"><span data-stu-id="e5408-p107">Both functions return the same error and success codes as **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**. See [Excel4/Excel12](excel4-excel12.md) for a full description of these codes. In addition, these Framework functions return **xlretFailed** without calling the C API if a NULL pointer to a parameter is detected.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e5408-132">例</span><span class="sxs-lookup"><span data-stu-id="e5408-132">Example</span></span>

<span data-ttu-id="e5408-133">この例では、不正な引数を **Excel12f** 関数に渡して、デバッガーにメッセージを送信しています。</span><span class="sxs-lookup"><span data-stu-id="e5408-133">This example passes a bad argument to the **Excel12f** function, which sends a message to the debugger.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e5408-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5408-134">See also</span></span>



[<span data-ttu-id="e5408-135">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="e5408-135">Excel4/Excel12</span></span>](excel4-excel12.md)


[<span data-ttu-id="e5408-136">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="e5408-136">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

