---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow function [excel 2007],TempActiveRow12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798942"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="237bc-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="237bc-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="237bc-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="237bc-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="237bc-106">作業中のシートの行全体の外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="237bc-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="237bc-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="237bc-107">Parameters</span></span>

 <span data-ttu-id="237bc-108">_row_</span><span class="sxs-lookup"><span data-stu-id="237bc-108">_row_</span></span>
  
<span data-ttu-id="237bc-p101">参照する行。0 を基準とするため、行 1 は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、WORD 整数で使用できる最大値は 65,535 = 2^16 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 以降では、最大値は 1,048,575 = 2^20 - 1 です。RW は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="237bc-p101">The row to be referenced. Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="237bc-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="237bc-114">Return value</span></span>

<span data-ttu-id="237bc-115">渡される行のセルの **xltypeRef** 外部参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="237bc-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="237bc-116">例</span><span class="sxs-lookup"><span data-stu-id="237bc-116">Example</span></span>

<span data-ttu-id="237bc-117">この例では、**TempActiveRow12** 関数を使用して行 113 を選択します。</span><span class="sxs-lookup"><span data-stu-id="237bc-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="237bc-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="237bc-118">See also</span></span>



[<span data-ttu-id="237bc-119">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="237bc-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

