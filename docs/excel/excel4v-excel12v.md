---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- excel12v function [excel 2007],Excel4v function [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414992"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="5a844-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="5a844-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="5a844-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5a844-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5a844-106">Microsoft Excel ワークシートの内部関数、マクロ シート関数やコマンド、または XLL 固有の特殊関数やコマンドを DLL、XLL、またはコード リソース内部から呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5a844-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="5a844-p101">Excel のすべての最新バージョンは、**Excel4v** をサポートしています。Excel 2007 以降のバージョンでは、**Excel12v** がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5a844-p101">All recent versions of Excel support **Excel4v**. Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="5a844-109">これらの関数は、Excel が DLL または XLL に制御を渡している場合にのみ、呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5a844-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="5a844-110">これらの関数は、Excel が Visual Basic for Applications (VBA) への呼び出しを介して間接的に制御を渡したときにも呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="5a844-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="5a844-111">それ以外の時に、これらの関数を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="5a844-111">They cannot be called at any other time.</span></span> <span data-ttu-id="5a844-112">たとえば、DllMain 関数に対する呼び出しの間も、オペレーティング システムが DLL を呼び出しているときも、これらの関数を呼び出すことはできません。DLL が作成したスレッドからも、これらの関数を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="5a844-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="5a844-p103">[Excel4 と Excel12](excel4-excel12.md) 関数は、スタック上の可変長リストとしてそれらの引数を受け入れます。一方、**Excel4v** と **Excel12v** 関数は、配列としてそれらの引数を受け入れます。それ以外の点のすべてで、**Excel4** は **Excel4v** と同じように動作し、**Excel12** は **Excel12v** と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="5a844-p103">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array. In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="5a844-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a844-115">Parameters</span></span>

 <span data-ttu-id="5a844-116">_iFunction_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="5a844-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="5a844-p104">呼び出すコマンド、関数、または特殊関数を示す数値。_iFunction_ の有効な値の一覧は、次の解説を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a844-p104">A number that indicates the command, function, or special function you want to call. For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="5a844-119">_pxRes_ (**LPXLOPER** または **LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="5a844-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="5a844-120">評価された関数の結果を保持する、**XLOPER** (**Excel4v** の場合) または **XLOPER12** (**Excel12v** の場合) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a844-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="5a844-121">_iCount_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="5a844-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="5a844-p105">関数へ渡される一連の引数の数。Excel 2003 以前のバージョンでは、0 ～ 30 の任意の数です。Excel 2007 以降は、0 ～ 255 の任意の数です。</span><span class="sxs-lookup"><span data-stu-id="5a844-p105">The number of subsequent arguments that will be passed to the function. In versions of Excel up to 2003 this can be any number from 0 through 30. Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="5a844-125">_rgx_ (**LPXLOPER []** または **LPXLOPER12 []**)</span><span class="sxs-lookup"><span data-stu-id="5a844-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="5a844-p106">関数への引数を含む配列です。配列内のすべての引数が **XLOPER** または **XLOPER12** の値を指すポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a844-p106">An array that contains the arguments to the function. All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="5a844-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="5a844-128">Return value</span></span>

<span data-ttu-id="5a844-129">これらの関数は、**Excel4** および **Excel12** と同じ値を返します。</span><span class="sxs-lookup"><span data-stu-id="5a844-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a844-130">注釈</span><span class="sxs-lookup"><span data-stu-id="5a844-130">Remarks</span></span>

<span data-ttu-id="5a844-p107">これらの関数は、演算子に渡された引数の数が可変の場合に役立ちます。たとえば **Excel4v** および **Excel12v** は、[xlfRegister](xlfregister-form-1.md) (引数の合計数が、登録対象の関数が取る引数の数によって決まる) を使用して関数を登録するときに役に立ちます。**Excel4v** および **Excel12v** は、**Excel4** または **Excel12** のラッパー関数を記述するときにも役立ちます。これらの場合、(通常 **Excel4** または **Excel12** に指定される) 可変引数リストを可変サイズの単一の配列の引数に変換し、**Excel4v** または **Excel12v** を使用して Excel にコールバックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a844-p107">These functions are useful where the number of arguments passed to the operator is variable. For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered. **Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**. In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="5a844-135">例</span><span class="sxs-lookup"><span data-stu-id="5a844-135">Example</span></span>

<span data-ttu-id="5a844-136">コードの例については、次に示す SDK をインストールした場所にある、Excel 2010 XLL SDK の **Excel** および **Excel12f** 関数のコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a844-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="5a844-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="5a844-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a844-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a844-138">See also</span></span>



[<span data-ttu-id="5a844-139">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="5a844-139">Excel4/Excel12</span></span>](excel4-excel12.md)

