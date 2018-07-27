---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref function [excel 2007],TempActiveRef12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798944"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="83c7b-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="83c7b-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="83c7b-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="83c7b-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="83c7b-106">作業中のワークシート上にある長方形のブロックのセルへの外部参照を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="83c7b-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="83c7b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83c7b-107">Parameters</span></span>

 <span data-ttu-id="83c7b-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="83c7b-108">_rwFirst_</span></span>
  
<span data-ttu-id="83c7b-109">参照の開始行。</span><span class="sxs-lookup"><span data-stu-id="83c7b-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="83c7b-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="83c7b-110">_rwLast_</span></span>
  
<span data-ttu-id="83c7b-111">参照の終了行。</span><span class="sxs-lookup"><span data-stu-id="83c7b-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="83c7b-p101">0 を基準とするため、行 1 は 0 として渡されます。Microsoft Office Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、WORD 整数で使用できる最大値は 65,535 = 2^16 - 1 です。バイトの整数で実行できる最大値とします。ブックを実行する Excel 2007 以降では、最大値は 1,048,575 = 2^20 - 1 です。RW は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="83c7b-p101">Row arguments are zero-based so that row 1 is passed as 0. In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer. Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1. RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="83c7b-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="83c7b-116">_colFirst_</span></span>
  
<span data-ttu-id="83c7b-117">参照の開始列番号。</span><span class="sxs-lookup"><span data-stu-id="83c7b-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="83c7b-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="83c7b-118">_colLast_</span></span>
  
<span data-ttu-id="83c7b-119">参照の終了列番号。</span><span class="sxs-lookup"><span data-stu-id="83c7b-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="83c7b-p102">列の引数は 0 を基準とするため、列 A は 0 として渡されます。Excel 2003 以前のバージョンと、互換モードでブックを実行する Excel 2007 以降では、最大値は 255 = 2^8 - 1 です。これは、BYTE 整数で使用できる最大値です。ブックを実行する Excel 2007 では、最大値は 16,383 = 2^14 - 1 です。COL は、XLCALL.H の 32 ビット符号付き整数として定義されます。</span><span class="sxs-lookup"><span data-stu-id="83c7b-p102">Column arguments are zero-based so that column A is passed as 0. In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer. Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1. COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="83c7b-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="83c7b-124">Return value</span></span>

<span data-ttu-id="83c7b-125">渡される長方形のブロックのセルへの **xltypeRef** 外部参照を返します。</span><span class="sxs-lookup"><span data-stu-id="83c7b-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="83c7b-126">例</span><span class="sxs-lookup"><span data-stu-id="83c7b-126">Example</span></span>

<span data-ttu-id="83c7b-127">この例では、**TempActiveRef12** 関数を使用して A105:C110 のセルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="83c7b-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="83c7b-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="83c7b-128">See also</span></span>



[<span data-ttu-id="83c7b-129">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="83c7b-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

