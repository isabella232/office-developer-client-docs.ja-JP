---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798994"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="32868-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="32868-103">xlGetInstPtr</span></span>

<span data-ttu-id="32868-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="32868-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="32868-105">現在 DLL を呼び出している Microsoft Excel インスタンスのインスタンス ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="32868-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="32868-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32868-106">Parameters</span></span>

<span data-ttu-id="32868-107">この関数には引数はありません。</span><span class="sxs-lookup"><span data-stu-id="32868-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="32868-108">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="32868-108">Property Value/Return Value</span></span>

<span data-ttu-id="32868-109">インスタンス ハンドル (**xltypeBigData**) は **val.bigdata.h.hdata** フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="32868-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32868-110">注釈</span><span class="sxs-lookup"><span data-stu-id="32868-110">Remarks</span></span>

<span data-ttu-id="32868-111">この関数を使用すると、DLL を呼び出している Excel の複数の実行中インスタンスを特定できます。</span><span class="sxs-lookup"><span data-stu-id="32868-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="32868-112">この関数は、32 ビットと 64 ビットの両方のバージョンの Excel で適切な値を返します。</span><span class="sxs-lookup"><span data-stu-id="32868-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="32868-113">[xlGetInst](xlgetinst.md) 関数の拡張機能として Excel 2010 で導入され、32 ビット バージョンの Excel でのみ正常に動作します。</span><span class="sxs-lookup"><span data-stu-id="32868-113">This function returns a correct value with both 32-bit and 64-bit versions of Excel. It was introduced in xl14short as an extension to the xlGetInst function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="32868-114">この関数は、API のコールバック関数の [Excel4 と Excel12](excel4-excel12.md) の両方を使用して呼び出されたときに正常に作動します。これは **XLOPER** と **XLOPER12** が **xltypeBigData** の型の値をサポートする同じ構造を持つからです。</span><span class="sxs-lookup"><span data-stu-id="32868-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="32868-115">例</span><span class="sxs-lookup"><span data-stu-id="32868-115">Example</span></span>

<span data-ttu-id="32868-p102">次の例では、呼び出し元 Excel の最終コピーのインスタンスを、呼び出し元 Excel の現在のコピーと比較します。この 2 つが同じであれば 1 を返し、そうでなければ 0 を返します。関数が失敗した場合は、-1 を返します。この例は、Excel の 32 ビット バージョンと 64 ビット バージョンの両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="32868-p102">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it. If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1. This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="32868-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="32868-119">See also</span></span>

- [<span data-ttu-id="32868-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="32868-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="32868-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="32868-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="32868-122">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="32868-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

