---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- tempstr function [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798955"
---
# <a name="tempstr"></a><span data-ttu-id="f7d68-104">TempStr</span><span class="sxs-lookup"><span data-stu-id="f7d68-104">TempStr</span></span>

 <span data-ttu-id="f7d68-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7d68-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f7d68-p101">**xltypeStr** バイト文字列を格納している一時的な **XLOPER** を作成する、非推奨のフレームワーク ライブラリ関数です。入力として、NULL で終了するソース文字列を受け取ります。受け取った文字列の最初の文字を後続の文字列の長さで上書きしようとします。この動作は安全でないことがあり、読み取り専用の文字列を渡すと、Microsoft Excel がクラッシュする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f7d68-p101">Deprecated Framework library function that creates a temporary **XLOPER** containing an **xltypeStr** byte string. It takes a null-terminated source string as input. It tries to overwrite the first character of the supplied string with the subsequent string's length. This is not always a safe thing to do: Microsoft Excel might crash if passed a read-only string.</span></span> 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a><span data-ttu-id="f7d68-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7d68-110">Parameters</span></span>

 <span data-ttu-id="f7d68-111">_str_</span><span class="sxs-lookup"><span data-stu-id="f7d68-111">_str_</span></span>
  
<span data-ttu-id="f7d68-p102">NULL で終了するソース文字列へのポインター。**TempStr** は 255 バイトよりも長い文字列を切り詰めます。</span><span class="sxs-lookup"><span data-stu-id="f7d68-p102">A pointer to the null-terminated source string. **TempStr** truncates strings that are longer than 255 bytes.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="f7d68-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7d68-114">Return value</span></span>

<span data-ttu-id="f7d68-115">渡された文字列バッファーへのポインターを格納している **xltypeStr** 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7d68-115">Returns an **xltypeStr** string containing a pointer to the passed-in string buffer.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7d68-116">注釈</span><span class="sxs-lookup"><span data-stu-id="f7d68-116">Remarks</span></span>

<span data-ttu-id="f7d68-p103">この方法による一時的な文字列の作成は、[TempStrConst と TempStr12](tempstrconst-tempstr12.md) の両方で動作する方法としては推奨されなくなりました。これらの関数は、新しいメモリ バッファーを割り当てて、そのバッファーに渡された文字列をコピーします。**TempStrConst** と **TempStr12** の入力文字列は変更されないため、**const** として宣言されます。これに対して、**TempStr** への入力文字列は変更されるため、**const** として宣言できません。入力文字列の最初の文字は、長さ文字のスペースとして扱われ、この関数によって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="f7d68-p103">This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work. These functions allocate a new memory buffer and copy the passed-in string into it. The input strings for **TempStrConst** and **TempStr12** are not altered and so are declared as **const**. In contrast, the input string to **TempStr** is altered and so cannot be declared as **const**. The first character of the input string is treated as space for a length character and is overwritten by this function.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7d68-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7d68-122">See also</span></span>



[<span data-ttu-id="f7d68-123">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="f7d68-123">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

