---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12 function [excel 2007],TempNum function [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426633"
---
# <a name="tempnumtempnum12"></a><span data-ttu-id="633c2-104">TempNum/TempNum12</span><span class="sxs-lookup"><span data-stu-id="633c2-104">TempNum/TempNum12</span></span>

 <span data-ttu-id="633c2-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="633c2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="633c2-106">Microsoft Excel ワークシートの番号を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数 (IEEE 8 バイトの倍精度浮動小数点型)。</span><span class="sxs-lookup"><span data-stu-id="633c2-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet number (an IEEE 8-byte double).</span></span> 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a><span data-ttu-id="633c2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="633c2-107">Parameters</span></span>

 <span data-ttu-id="633c2-108">_d_ (**double**)</span><span class="sxs-lookup"><span data-stu-id="633c2-108">_d_ (**double**)</span></span>
  
<span data-ttu-id="633c2-p101">対象の値。IEEE 規格の非正規数は現在サポートされていないため、ゼロに丸められます。負の無限大に対応しています。</span><span class="sxs-lookup"><span data-stu-id="633c2-p101">The intended value. Note that IEEE sub-normal numbers are not currently supported and are rounded to zero. Negative infinity is supported.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="633c2-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="633c2-112">Return value</span></span>

<span data-ttu-id="633c2-113">渡される値を含む数値型 **xltypeNum** を返します。渡された値が非正規数の場合はゼロを返します。</span><span class="sxs-lookup"><span data-stu-id="633c2-113">Returns a numeric **xltypeNum** containing the value passed in or zero if the passed in value was sub-normal.</span></span> 
  
## <a name="example"></a><span data-ttu-id="633c2-114">例</span><span class="sxs-lookup"><span data-stu-id="633c2-114">Example</span></span>

<span data-ttu-id="633c2-115">この例では、**TempNum12** 関数を使用して、**xlfGetWorkspace** に引数を渡しています。</span><span class="sxs-lookup"><span data-stu-id="633c2-115">This example uses the **TempNum12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="633c2-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="633c2-116">See also</span></span>



[<span data-ttu-id="633c2-117">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="633c2-117">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

