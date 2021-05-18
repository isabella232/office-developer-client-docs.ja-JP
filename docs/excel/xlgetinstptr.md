---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405283"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="b923a-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="b923a-103">xlGetInstPtr</span></span>

<span data-ttu-id="b923a-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b923a-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b923a-105">現在 DLL を呼び出している Microsoft Excel インスタンスのインスタンス ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="b923a-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="b923a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b923a-106">Parameters</span></span>

<span data-ttu-id="b923a-107">この関数には引数はありません。</span><span class="sxs-lookup"><span data-stu-id="b923a-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b923a-108">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="b923a-108">Property value/Return value</span></span>

<span data-ttu-id="b923a-109">インスタンス ハンドル (**xltypeBigData**) は **val.bigdata.h.hdata** フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="b923a-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b923a-110">注釈</span><span class="sxs-lookup"><span data-stu-id="b923a-110">Remarks</span></span>

<span data-ttu-id="b923a-111">この関数を使用すると、DLL を呼び出している Excel の複数の実行中インスタンスを特定できます。</span><span class="sxs-lookup"><span data-stu-id="b923a-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="b923a-p101">This function returns a correct value with both 32-bit and 64-bit versions of Excel. It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span><span class="sxs-lookup"><span data-stu-id="b923a-p101">This function returns a correct value with both 32-bit and 64-bit versions of Excel. It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="b923a-114">この関数は、API のコールバック関数の [Excel4 と Excel12](excel4-excel12.md) の両方を使用して呼び出されたときに正常に作動します。これは **XLOPER** と **XLOPER12** が **xltypeBigData** の型の値をサポートする同じ構造を持つからです。</span><span class="sxs-lookup"><span data-stu-id="b923a-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b923a-115">例</span><span class="sxs-lookup"><span data-stu-id="b923a-115">Example</span></span>

<span data-ttu-id="b923a-p102">次の例では、呼び出し元 Excel の最終コピーのインスタンスを、呼び出し元 Excel の現在のコピーと比較します。この 2 つが同じであれば 1 を返し、そうでなければ 0 を返します。関数が失敗した場合は、-1 を返します。この例は、Excel の 32 ビット バージョンと 64 ビット バージョンの両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="b923a-p102">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it. If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1. This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="b923a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="b923a-119">See also</span></span>

- [<span data-ttu-id="b923a-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="b923a-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="b923a-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="b923a-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="b923a-122">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="b923a-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

