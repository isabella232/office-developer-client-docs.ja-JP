---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum function [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406942"
---
# <a name="funcsum"></a><span data-ttu-id="0f95a-104">FuncSum</span><span class="sxs-lookup"><span data-stu-id="0f95a-104">FuncSum</span></span>

 <span data-ttu-id="0f95a-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0f95a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0f95a-p101">1 ～ 29 個の引数を取って、それらの合計を計算する、サンプル ユーザー定義ワークシート関数。各引数に指定できるのは、1 つの数字、範囲、または配列です。GENERIC.xll が読み込まれると、GENERIC.xll によってこの関数が登録されて、ワークシートから呼び出すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f95a-p101">Example user-defined worksheet function that takes 1 to 29 arguments and computes their sum. Each argument can be a single number, a range, or an array. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span> 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a><span data-ttu-id="0f95a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f95a-109">Parameters</span></span>

 <span data-ttu-id="0f95a-110">_px1-px29_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="0f95a-110">_px1-px29_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="0f95a-p102">**XLOPER12** 引数へのポインター。この関数は、任意の入力の型を受け入れますが、数字、数字のリテラル配列、および数字または空白セルのみが含まれている範囲を対象に作動するようコーディングされています。指定された引数の数が 29 に満たない場合、残りの引数は **xltypeMissing** として指定されます。</span><span class="sxs-lookup"><span data-stu-id="0f95a-p102">Pointers to **XLOPER12** arguments. The function accepts any kind of input type but is coded only to operate on numbers, literal arrays of numbers, and ranges containing only numbers or blank cells. If fewer than 29 arguments are supplied, the remaining arguments are supplied as **xltypeMissing**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0f95a-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="0f95a-114">Property value/Return value</span></span>

<span data-ttu-id="0f95a-115">(**LPXLOPER12 xltypeNum** または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="0f95a-115">(**LPXLOPER12 xltypeNum** or **xltypeErr**)</span></span>
  
<span data-ttu-id="0f95a-p103">供給された引数リスト、範囲内のセル、配列内の要素に、数字以外の文字が存在する場合の、引数の合計、あるいは #VALUE!。</span><span class="sxs-lookup"><span data-stu-id="0f95a-p103">The sum of the arguments or #VALUE! if there are non-numerics in the supplied argument list or in a cell in a range or element in an array.</span></span>
  
### <a name="example"></a><span data-ttu-id="0f95a-118">例</span><span class="sxs-lookup"><span data-stu-id="0f95a-118">Example</span></span>

<span data-ttu-id="0f95a-119">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f95a-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f95a-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f95a-120">See also</span></span>



[<span data-ttu-id="0f95a-121">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="0f95a-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

