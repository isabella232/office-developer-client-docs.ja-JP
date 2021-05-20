---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf function [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430645"
---
# <a name="xludf"></a><span data-ttu-id="db7e3-104">xlUDF</span><span class="sxs-lookup"><span data-stu-id="db7e3-104">xlUDF</span></span>

<span data-ttu-id="db7e3-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="db7e3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="db7e3-p101">ユーザー定義関数 (UDF) を呼び出します。この関数により、DLL は Visual Basic for Applications (VBA) のユーザー定義関数、XLM マクロ言語の関数、およびその他のアドインに含まれる登録済みの関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="db7e3-p101">Calls a user-defined function (UDF). This function allows a DLL to call Visual Basic for Applications (VBA) user-defined functions, XLM macro language functions, and registered functions contained in other add-ins.</span></span>
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a><span data-ttu-id="db7e3-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="db7e3-108">Parameters</span></span>

<span data-ttu-id="db7e3-109">_pxFnRef_ (**xltypeRef**、**xltypeSRef**、**xltypeStr**、または **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="db7e3-109">_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="db7e3-p102">呼び出す関数の参照。これはマクロ シートのセルの参照、文字列としての関数の登録名、または関数の登録 ID になります。_pxFunctionText_ 引数を指定した **xlfRegister** または **REGISTER** で登録された XLL アドイン関数の場合、**xlfEvaluate** を使用して名前を検索することで、この ID を取得できます。</span><span class="sxs-lookup"><span data-stu-id="db7e3-p102">The reference of the function you want to call. This can be a macro sheet cell reference, the registered name of the function as a string, or the register ID of the function. For XLL add-in functions registered using **xlfRegister** or **REGISTER** with the argument  _pxFunctionText_ supplied, the ID can be obtained by using **xlfEvaluate** to look up the name.</span></span> 
  
<span data-ttu-id="db7e3-113">_pxArg1, ..._</span><span class="sxs-lookup"><span data-stu-id="db7e3-113">_pxArg1, ..._</span></span>
  
<span data-ttu-id="db7e3-p103">ユーザー定義関数に渡すゼロ以上の引数。Excel 2007 より前のバージョンでこの関数を呼び出す場合、関数に渡せる追加引数の最大数は 29 です (_pxFnRef_ を含めると合計 30)。Excel 2007 以降では、この制限は 254 に引き上げられています (_pxFnRef_ を含めると合計 255)。</span><span class="sxs-lookup"><span data-stu-id="db7e3-p103">Zero or more arguments to the user-defined function. When you are calling this function in versions earlier than Excel 2007, the maximum number of additional arguments that can be passed is 29, which is 30 including  _pxFnRef_. Starting in Excel 2007, this limit is raised to 254, which is 255 including  _pxFnRef_.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="db7e3-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="db7e3-117">Return value</span></span>

<span data-ttu-id="db7e3-118">ユーザー定義関数が返す値を返します。</span><span class="sxs-lookup"><span data-stu-id="db7e3-118">Returns whatever value the user-defined function returned.</span></span>
  
## <a name="example"></a><span data-ttu-id="db7e3-119">例</span><span class="sxs-lookup"><span data-stu-id="db7e3-119">Example</span></span>

<span data-ttu-id="db7e3-p104">次の例では、BOOK1.XLS のシート Macro1 に対して **TestMacro** を実行します。マクロが Macro1 という名前のシートにあることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="db7e3-p104">The following example runs **TestMacro** on sheet Macro1 in BOOK1.XLS. Make sure that the macro is on a sheet named Macro1.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="db7e3-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="db7e3-122">See also</span></span>

- [<span data-ttu-id="db7e3-123">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="db7e3-123">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

