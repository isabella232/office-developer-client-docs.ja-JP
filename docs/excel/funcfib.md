---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib function [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423672"
---
# <a name="funcfib"></a><span data-ttu-id="d61d1-104">FuncFib</span><span class="sxs-lookup"><span data-stu-id="d61d1-104">FuncFib</span></span>

 <span data-ttu-id="d61d1-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d61d1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d61d1-p101">N 番目のフィボナッチ数を計算するユーザー定義ワークシート関数の例です。GENERIC.xll が読み込まれるときに、ワークシートから呼び出すことができるように、この関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="d61d1-p101">Example user-defined worksheet function that computes the Nth Fibonacci number. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a><span data-ttu-id="d61d1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d61d1-108">Parameters</span></span>

 <span data-ttu-id="d61d1-109">_pxN_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="d61d1-109">_pxN_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="d61d1-110">N 番目のフィボナッチ数が必要とされる N の値。</span><span class="sxs-lookup"><span data-stu-id="d61d1-110">The value of N for which the Nth Fibonacci number is required.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d61d1-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="d61d1-111">Property value/Return value</span></span>

<span data-ttu-id="d61d1-112">(成功した場合は **xltypeNum LPXLOPER12**、それ以外の場合は **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="d61d1-112">(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise)</span></span> 
  
<span data-ttu-id="d61d1-113">N 番目のフィボナッチ数。</span><span class="sxs-lookup"><span data-stu-id="d61d1-113">The Nth Fibonacci number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d61d1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d61d1-114">Remarks</span></span>

<span data-ttu-id="d61d1-p102">この関数は、関数ブロック内で戻り値 **XLOPER12** として定義された静的変数を使用します。これはスレッド セーフではないため、この関数もスレッド セーフではありません。Excel 2007 以降では、この戦略を使用して **XLOPER** または **XLOPER12** を返すワークシート関数をスレッド セーフとして登録しないでください。</span><span class="sxs-lookup"><span data-stu-id="d61d1-p102">The function uses a static variable defined within the function block as the return value **XLOPER12**. This is not thread safe, and so this function, and any worksheet function that uses this strategy for returning **XLOPER**s or **XLOPER12**s, should not be registered as thread safe starting in Excel 2007.</span></span>
  
### <a name="example"></a><span data-ttu-id="d61d1-117">例</span><span class="sxs-lookup"><span data-stu-id="d61d1-117">Example</span></span>

<span data-ttu-id="d61d1-118">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d61d1-118">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d61d1-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="d61d1-119">See also</span></span>



[<span data-ttu-id="d61d1-120">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="d61d1-120">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

