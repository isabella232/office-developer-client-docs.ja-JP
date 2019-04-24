---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12 function [excel 2007],TempActiveColumn function [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310473"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="43e57-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="43e57-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="43e57-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43e57-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43e57-106">作業中のシートの列全体の外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="43e57-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="43e57-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43e57-107">Parameters</span></span>

 <span data-ttu-id="43e57-108">_col_ (**BYTE**)</span><span class="sxs-lookup"><span data-stu-id="43e57-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="43e57-p101">参照する列。0 を基準とするため、列 A は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、BYTE 整数で使用できる最大値は 255 = 2^8 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 では、最大値は 16,383 = 2^14 - 1 です。COL は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="43e57-p101">The column to be referenced. This is zero-based so that column A is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="43e57-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="43e57-114">Return value</span></span>

<span data-ttu-id="43e57-115">渡される列の **xltypeRef** 外部参照を返します。</span><span class="sxs-lookup"><span data-stu-id="43e57-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="43e57-116">例</span><span class="sxs-lookup"><span data-stu-id="43e57-116">Example</span></span>

<span data-ttu-id="43e57-117">次の例では、**TempActiveColumn12** を使用して、列 B 全体を選択します。</span><span class="sxs-lookup"><span data-stu-id="43e57-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="43e57-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="43e57-118">See also</span></span>



[<span data-ttu-id="43e57-119">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="43e57-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

