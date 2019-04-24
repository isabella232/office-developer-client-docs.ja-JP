---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12 function [excel 2007],TempStrConst function [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310326"
---
# <a name="tempstrconsttempstr12"></a><span data-ttu-id="6c5d6-104">TempStrConst/TempStr12</span><span class="sxs-lookup"><span data-stu-id="6c5d6-104">TempStrConst/TempStr12</span></span>

 <span data-ttu-id="6c5d6-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6c5d6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6c5d6-p101">**xltypeStr** 文字列を含む一時的な **XLOPER/XLOPER12** を作成するフレームワーク ライブラリ関数。入力として Null で終了するソースの文字列を受け取ります。この関数は、新しいメモリ バッファーを割り当てて、そのバッファーに渡された文字列をコピーします。入力文字列は変更されないため、**const** として宣言されます。</span><span class="sxs-lookup"><span data-stu-id="6c5d6-p101">Framework library function that creates a temporary **XLOPER/XLOPER12** that contains an **xltypeStr** string, taking a null-terminated source string as input. The function allocates a new memory buffer and copies the passed-in string into it. The input string is not altered and so is declared as **const**.</span></span>
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a><span data-ttu-id="6c5d6-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c5d6-109">Parameters</span></span>

 <span data-ttu-id="6c5d6-110">_str_</span><span class="sxs-lookup"><span data-stu-id="6c5d6-110">_str_</span></span>
  
<span data-ttu-id="6c5d6-p102">Null で終了するソースの文字列へのポインター。**XLOPER** の場合、TempStrConst は 255 バイトより長い文字列を切り捨てます。**XLOPER12** の場合、TempStr12Const は 32,767 Unicode 文字より長い文字列を切り捨てます。</span><span class="sxs-lookup"><span data-stu-id="6c5d6-p102">A pointer to the null-terminated source string. In the case of **XLOPER**s, TempStrConst truncates strings that are longer than 255 bytes. In the case of **XLOPER12**s, TempStr12Const truncates strings that are longer than 32,767 Unicode characters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6c5d6-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c5d6-114">Return value</span></span>

<span data-ttu-id="6c5d6-115">渡された文字列バッファーのコピーを格納している **xltypeStr** 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6c5d6-115">Returns an **xltypeStr** string containing a copy of the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6c5d6-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6c5d6-116">Remarks</span></span>

<span data-ttu-id="6c5d6-p103">**XLOPER** 文字列のフレームワーク関数 **TempStr** の動作は異なります。指定された文字列の最初の文字を後続の文字列の長さで上書きしようとするため、注意が必要です。この動作は安全でないことがあり、読み取り専用の文字列を渡すと、Microsoft Excel がクラッシュする可能性があります。この方法による一時的な文字列の作成は、**TempStrConst** と **TempStr12** の両方で動作する方法としては推奨されなくなりました。したがって、入力文字列の最初の文字は、文字列の先頭として (つまり、長さを表す文字または長さを表す文字用のスペースとしてではなく) 処理されます。影響が予測できないため、開始時にエンコードされた長さを表す文字のある文字列は渡さないでください。</span><span class="sxs-lookup"><span data-stu-id="6c5d6-p103">Note that the **XLOPER** string Framework function, **TempStr**, behaves differently and tries to overwrite the first character of the supplied string with the subsequent string's length. This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string. This way of creating temporary strings is now deprecated in favor of the way in which both **TempStrConst** and **TempStr12** work. Therefore the first character of the input string is treated as the start of the string, that is, not as a length character or as a space for a length character. You should not pass strings that have a length character encoded at the start, as the consequences could be unpredictable.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6c5d6-122">例</span><span class="sxs-lookup"><span data-stu-id="6c5d6-122">Example</span></span>

<span data-ttu-id="6c5d6-123">この例では、**TempStr12** 関数を使用してメッセージ ボックスの文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c5d6-123">This example uses the **TempStr12** function to create a string for a message box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6c5d6-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c5d6-124">See also</span></span>



[<span data-ttu-id="6c5d6-125">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="6c5d6-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

