---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 function [excel 2007],TempInt function [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310480"
---
# <a name="tempinttempint12"></a><span data-ttu-id="002ca-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="002ca-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="002ca-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="002ca-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="002ca-106">整数を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="002ca-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="002ca-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="002ca-107">Parameters</span></span>

 <span data-ttu-id="002ca-108">_i_</span><span class="sxs-lookup"><span data-stu-id="002ca-108">_i_</span></span>
  
<span data-ttu-id="002ca-p101">対象の整数値。**XLOPER** 整数は、符号付き 16 ビット整数 (short int) であるのに対し、**XLOPER12** 整数は、符号付き 32 ビット整数 ([long] int) であることにご注意ください。</span><span class="sxs-lookup"><span data-stu-id="002ca-p101">The intended integer value. Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="002ca-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="002ca-111">Return value</span></span>

<span data-ttu-id="002ca-112">渡された値を含む **xltypeInt** 整数を返します。</span><span class="sxs-lookup"><span data-stu-id="002ca-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="002ca-113">例</span><span class="sxs-lookup"><span data-stu-id="002ca-113">Example</span></span>

<span data-ttu-id="002ca-114">この例では、**TempInt12** 関数を使用して、**xlfGetWorkspace** に引数を渡しています。</span><span class="sxs-lookup"><span data-stu-id="002ca-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="002ca-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="002ca-115">See also</span></span>



[<span data-ttu-id="002ca-116">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="002ca-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

