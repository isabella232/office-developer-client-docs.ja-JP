---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- tempactivecell12 function [excel 2007],TempActiveCell function [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413193"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="c1d95-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="c1d95-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="c1d95-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c1d95-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c1d95-106">作業中のシートのセルへの外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="c1d95-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="c1d95-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1d95-107">Parameters</span></span>

 <span data-ttu-id="c1d95-108">_row_</span><span class="sxs-lookup"><span data-stu-id="c1d95-108">_row_</span></span>
  
<span data-ttu-id="c1d95-p101">参照する行。0 を基準とするため、行 1 は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、WORD 整数で使用できる最大値は 65,535 = 2^16 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 以降では、最大値は 1,048,575 = 2^20 - 1 です。RW は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="c1d95-p101">The row to be referenced. Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="c1d95-114">_col_</span><span class="sxs-lookup"><span data-stu-id="c1d95-114">_col_</span></span>
  
<span data-ttu-id="c1d95-p102">参照する列。0 を基準とするため、列 A は 0 として渡されます。Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、最大値は 255 = 2^8 - 1 です。これは、BYTE 整数で使用できる最大値です。ブックを実行する Excel 2007 では、最大値は 16,383 = 2^14 - 1 です。COL は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="c1d95-p102">The column to be referenced. This is zero-based so that column A is passed as 0. In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c1d95-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="c1d95-120">Return value</span></span>

<span data-ttu-id="c1d95-121">渡されるセルの **xltypeRef** 外部参照を返します。</span><span class="sxs-lookup"><span data-stu-id="c1d95-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c1d95-122">例</span><span class="sxs-lookup"><span data-stu-id="c1d95-122">Example</span></span>

<span data-ttu-id="c1d95-123">次の例では、**TempActiveCell12** を使用して B94 の内容を作業中のシートに表示します。</span><span class="sxs-lookup"><span data-stu-id="c1d95-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c1d95-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1d95-124">See also</span></span>



[<span data-ttu-id="c1d95-125">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="c1d95-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

