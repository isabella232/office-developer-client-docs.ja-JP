---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate function [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303928"
---
# <a name="xlfevaluate"></a><span data-ttu-id="ff19b-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="ff19b-104">xlfEvaluate</span></span>

 <span data-ttu-id="ff19b-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff19b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ff19b-106">Microsoft Excel のパーサーと関数エバリュエーターを使用して、ワークシートのセルに入力できる任意の式を評価します。</span><span class="sxs-lookup"><span data-stu-id="ff19b-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="ff19b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff19b-107">Parameters</span></span>

 <span data-ttu-id="ff19b-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="ff19b-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="ff19b-p101">評価する文字列です。文字列は任意のテキストにできます。先頭の等号 (=) は省略可能です。これは正式に、ワークシートまたはマクロ シートのセルに入力できます。</span><span class="sxs-lookup"><span data-stu-id="ff19b-p101">The string to be evaluated. A leading equal sign (=) is optional. The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ff19b-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ff19b-112">Property value/Return value</span></span>

<span data-ttu-id="ff19b-113">文字列の評価結果を返します。これは **xltypeNum**、**xltypeStr**、**xltypeBool**、**xltypeErr**、**xltypeNil**、**xltypeMulti** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="ff19b-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff19b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ff19b-114">Remarks</span></span>

<span data-ttu-id="ff19b-p102">文字列には関数のみを含めることができます。コマンドは対応しません。これは、数式バーで **F9** を押した場合と同じです。**xlfEvaluate** がスレッド セーフとして登録された XLL ワークシート関数から呼び出された場合、式にはスレッドセーフ関数のみを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff19b-p102">The string can contain only functions, not command equivalents. It is equivalent to pressing **F9** from the formula bar. If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="ff19b-p103">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL. Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL. For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="ff19b-p103">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL. Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL. For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="ff19b-121">**xlfEvaluate** は、開かれていない外部シートへの参照の評価には使用できません。</span><span class="sxs-lookup"><span data-stu-id="ff19b-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ff19b-122">例</span><span class="sxs-lookup"><span data-stu-id="ff19b-122">Example</span></span>

<span data-ttu-id="ff19b-123">この例では、**xlfEvaluate** を使用して強制的にテキスト "!B38" をセル B38 の内容にします。</span><span class="sxs-lookup"><span data-stu-id="ff19b-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="ff19b-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="ff19b-124"></span></span> <span data-ttu-id="ff19b-125">この関数はコマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドから呼び出された場合にのみ正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="ff19b-125">This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ff19b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff19b-126">See also</span></span>

- [<span data-ttu-id="ff19b-127">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="ff19b-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

