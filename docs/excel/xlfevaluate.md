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
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798970"
---
# <a name="xlfevaluate"></a><span data-ttu-id="ce0cd-104">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="ce0cd-104">xlfEvaluate</span></span>

 <span data-ttu-id="ce0cd-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ce0cd-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ce0cd-106">Microsoft Excel のパーサーと関数エバリュエーターを使用して、ワークシートのセルに入力できる任意の式を評価します。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-106">Uses the Microsoft Excel parser and function evaluator to evaluate any expression that could be entered in a worksheet cell.</span></span>
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a><span data-ttu-id="ce0cd-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ce0cd-107">Parameters</span></span>

 <span data-ttu-id="ce0cd-108">_pxFormulaText (xltypeStr)_</span><span class="sxs-lookup"><span data-stu-id="ce0cd-108">_pxFormulaText (xltypeStr)_</span></span>
  
<span data-ttu-id="ce0cd-p101">評価する文字列です。文字列は任意のテキストにできます。先頭の等号 (=) は省略可能です。これは正式に、ワークシートまたはマクロ シートのセルに入力できます。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-p101">The string to be evaluated. A leading equal sign (=) is optional. The string can be any text that can legally be entered into a worksheet or macro sheet cell.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ce0cd-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="ce0cd-112">Property Value/Return Value</span></span>

<span data-ttu-id="ce0cd-113">文字列の評価結果を返します。これは **xltypeNum**、**xltypeStr**、**xltypeBool**、**xltypeErr**、**xltypeNil**、**xltypeMulti** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-113">Returns the result of evaluating the string which can be any of the types **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce0cd-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ce0cd-114">Remarks</span></span>

<span data-ttu-id="ce0cd-p102">文字列には関数のみを含めることができます。コマンドは対応しません。これは、数式バーで **F9** を押した場合と同じです。**xlfEvaluate** がスレッド セーフとして登録された XLL ワークシート関数から呼び出された場合、式にはスレッドセーフ関数のみを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-p102">The string can contain only functions, not command equivalents. It is equivalent to pressing **F9** from the formula bar. If **xlfEvaluate** is called from an XLL worksheet function that has been registered as thread safe, the expression must only contain thread-safe functions.</span></span> 
  
<span data-ttu-id="ce0cd-118">**xlfEvaluate** 関数は、主に DLL が定義済みの名前に割り当てられた値を検索できるようにするために使用します。この名前はシート上にあるか、DLL 内で定義された非表示の名前です。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-118">The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL. Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL. For more information, see Evaluating Names and Other Worksheet Formula Expressions.</span></span> <span data-ttu-id="ce0cd-119">DLL/XLL 内では、ワークシートの名前に少なくとも感嘆符 (!) のプレフィックスを付けて、ワークシートが DLL の外部として解釈される必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-119">Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL.</span></span> <span data-ttu-id="ce0cd-120">詳細については、「[名前と他のワークシートの式を評価する](evaluating-names-and-other-worksheet-formula-expressions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-120">For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).</span></span>
  
 <span data-ttu-id="ce0cd-121">**xlfEvaluate** は、開かれていない外部シートへの参照の評価には使用できません。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-121">**xlfEvaluate** cannot be used to evaluate references to an external sheet that is not open.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ce0cd-122">例</span><span class="sxs-lookup"><span data-stu-id="ce0cd-122">Example</span></span>

<span data-ttu-id="ce0cd-123">この例では、**xlfEvaluate** を使用して強制的にテキスト "!B38" をセル B38 の内容にします。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-123">This example uses **xlfEvaluate** to coerce the text "!B38" to the contents of cell B38.</span></span> 
  
 <span data-ttu-id="ce0cd-124">`\SAMPLES\EXAMPLE\EXAMPLE.C`</span><span class="sxs-lookup"><span data-stu-id="ce0cd-124"></span></span> <span data-ttu-id="ce0cd-125">この関数はコマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドから呼び出された場合にのみ正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="ce0cd-125">\SAMPLES\EXAMPLE\EXAMPLE.C. This function calls a command macro (**xlcAlert**) and will work correctly only when called from a macro sheet or as a macro command.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ce0cd-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce0cd-126">See also</span></span>

- [<span data-ttu-id="ce0cd-127">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="ce0cd-127">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

