---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst function [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428131"
---
# <a name="xlgetinst"></a><span data-ttu-id="73d02-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="73d02-104">xlGetInst</span></span>

 <span data-ttu-id="73d02-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73d02-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="73d02-106">現在 DLL を呼び出している Microsoft Excel インスタンスのインスタンス ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="73d02-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="73d02-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73d02-107">Parameters</span></span>

<span data-ttu-id="73d02-108">この関数には引数はありません。</span><span class="sxs-lookup"><span data-stu-id="73d02-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="73d02-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="73d02-109">Property value/Return value</span></span>

<span data-ttu-id="73d02-110">インスタンス ハンドル (**xltypeInt**) は、**val.w** フィールドに取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="73d02-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73d02-111">注釈</span><span class="sxs-lookup"><span data-stu-id="73d02-111">Remarks</span></span>

<span data-ttu-id="73d02-112">この関数を使用すると、DLL を呼び出している Excel の複数の実行中インスタンスを特定できます。</span><span class="sxs-lookup"><span data-stu-id="73d02-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="73d02-p101">[Excel4](excel4-excel12.md) または [Excel4v](excel4v-excel12v.md) を使用してこの関数を呼び出すと、返される XLOPER 整数変数は、16 ビット符号付き short int になります。この場合に格納できるのは、32 ビット Windows ハンドルの下位 16 ビットのみです。Excel 2007 以降では、**XLOPER12** の整数変数は 32 ビットの符号付き整数になり、すべてのオープン ウィンドウを反復処理する必要がなくなっています。</span><span class="sxs-lookup"><span data-stu-id="73d02-p101">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle. Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="73d02-p102">**xlGetInst** 関数を 64 ビット版の Microsoft Excel で使用すると、失敗します。これは、**xltypeInt** 値の型の大きさが、Excel によって返される 64 ビット長のハンドルを保持できないためです。このため、Excel 2010 では [xlGetInstPtr](xlgetinstptr.md) という名前の新しい関数が導入されました。この関数は、32 ビットと 64 ビットのどちらのバージョンの Excel でも正常に動作します。</span><span class="sxs-lookup"><span data-stu-id="73d02-p102">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail. This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case. For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="73d02-118">例</span><span class="sxs-lookup"><span data-stu-id="73d02-118">Example</span></span>

<span data-ttu-id="73d02-p103">次の例では、呼び出し元 Excel の最終コピーのインスタンスを、呼び出し元 Excel の現在のコピーと比較します。この 2 つが同じであれば 1 を返し、そうでなければ 0 を返します。関数が失敗した場合は、-1 を返します。</span><span class="sxs-lookup"><span data-stu-id="73d02-p103">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it. If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="73d02-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="73d02-121">See also</span></span>



[<span data-ttu-id="73d02-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="73d02-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="73d02-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="73d02-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="73d02-124">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="73d02-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

