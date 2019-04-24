---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack function [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310158"
---
# <a name="xlstack"></a><span data-ttu-id="2cb25-104">xlStack</span><span class="sxs-lookup"><span data-stu-id="2cb25-104">xlStack</span></span>

<span data-ttu-id="2cb25-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2cb25-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2cb25-106">スタック上の空き領域を確認します。</span><span class="sxs-lookup"><span data-stu-id="2cb25-106">Checks the amount of space left on the stack.</span></span>
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="2cb25-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2cb25-107">Parameters</span></span>

<span data-ttu-id="2cb25-108">この関数に引数はありません。</span><span class="sxs-lookup"><span data-stu-id="2cb25-108">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2cb25-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2cb25-109">Property value/Return value</span></span>

<span data-ttu-id="2cb25-110">スタック上に残っているバイト数 (**xltypeInt**) を返します。</span><span class="sxs-lookup"><span data-stu-id="2cb25-110">Returns the number of bytes (**xltypeInt**) remaining on the stack.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2cb25-111">注釈</span><span class="sxs-lookup"><span data-stu-id="2cb25-111">Remarks</span></span>

<span data-ttu-id="2cb25-p101">最近のバージョンの使用可能なスタック領域の容量は、**XLOPER** の 16 ビットの符号付き整数に収まりません。つまり、**xlStack** は **XLOPER** および **Excel4** または **Excel4v** を使用して呼び出したときに -32767 から 32768 の間の値を返すことができる、ということです。この場合に正しい値を取得するには、戻り値を unsigned short 型にキャストします。</span><span class="sxs-lookup"><span data-stu-id="2cb25-p101">The amount of available stack space of recent versions overflows the 16-bit signed integer of the **XLOPER**. This means that **xlStack** can return a value between -32767 and 32768 when called using **XLOPER**s and **Excel4** or **Excel4v**. To obtain the correct value in this case, you must cast the returned value to an unsigned short.</span></span>
  
<span data-ttu-id="2cb25-115">Excel 2007 以降では、**XLOPER12** および **Excel12** または **Excel12v** を使用して、この関数を呼び出す必要があります。その場合、戻り値は使用可能なスタック領域の容量か、64 KB のいずれか小さい方になります。</span><span class="sxs-lookup"><span data-stu-id="2cb25-115">Starting in Excel 2007, you should call this function using **XLOPER12**s and **Excel12** or **Excel12v**, in which case the returned value is amount of stack space available or 64 KB, whichever is the lesser.</span></span>
  
<span data-ttu-id="2cb25-p102">Excel では、スタック上の空き領域に制限があります。この容量を超えないように注意する必要があります。非常に大きなデータ構造を配置したり、可能な限り多くのローカル変数を静的にしてはいけません。関数を再帰的に呼び出さないようにしてください。これを行うと、スタックがすぐにいっぱいになります。</span><span class="sxs-lookup"><span data-stu-id="2cb25-p102">Excel has a limited amount of space on the stack, and you should take care not to overrun this space. Never put very large data structures on the stack, and make as many local variables as possible static. Avoid calling functions recursively, because that will quickly fill up the stack.</span></span>
  
<span data-ttu-id="2cb25-119">スタックをオーバーランしている疑いがある場合は、この関数を頻繁に呼び出して、スタック領域がどの程度残っているか確認します。</span><span class="sxs-lookup"><span data-stu-id="2cb25-119">If you suspect that you are overrunning the stack, call this function frequently to see how much stack space is left.</span></span>
  
## <a name="example"></a><span data-ttu-id="2cb25-120">例</span><span class="sxs-lookup"><span data-stu-id="2cb25-120">Example</span></span>

<span data-ttu-id="2cb25-p103">最初の例では、スタックの空き領域の容量が示された警告メッセージが表示されます。これは `\SAMPLES\EXAMPLE\EXAMPLE.C` に格納されています。2 番目の例も同じことをします (**XLOPER** を使用)。これは SDK のコード例には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2cb25-p103">The first example displays an alert message containing the amount of stack space left and is contained in  `\SAMPLES\EXAMPLE\EXAMPLE.C`. The second example does the same thing, working with **XLOPER**s and is not contained in the SDK example code.</span></span>
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2cb25-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cb25-123">See also</span></span>

- [<span data-ttu-id="2cb25-124">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="2cb25-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

