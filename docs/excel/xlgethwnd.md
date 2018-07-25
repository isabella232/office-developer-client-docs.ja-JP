---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798995"
---
# <a name="xlgethwnd"></a><span data-ttu-id="74c70-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="74c70-104">xlGetHwnd</span></span>

<span data-ttu-id="74c70-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74c70-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="74c70-106">Microsoft Excel ウィンドウの最上位のウィンドウ ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="74c70-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="74c70-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74c70-107">Parameters</span></span>

<span data-ttu-id="74c70-108">この関数には引数はありません。</span><span class="sxs-lookup"><span data-stu-id="74c70-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="74c70-109">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="74c70-109">Property Value/Return Value</span></span>

<span data-ttu-id="74c70-110">**val.w** フィールドにウィンドウ ハンドル (**xltypeInt**) が格納されます。</span><span class="sxs-lookup"><span data-stu-id="74c70-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="74c70-111">注釈</span><span class="sxs-lookup"><span data-stu-id="74c70-111">Remarks</span></span>

<span data-ttu-id="74c70-112">この関数は、Windows API のコードを記述するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="74c70-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="74c70-p101">[Excel4](excel4-excel12.md) または [Excel4v](excel4v-excel12v.md) を使用して、この関数を呼び出すと、返される XLOPER 整数変数は、16 ビット符号付き short int になります。この場合に格納できるのは、32 ビット Windows ハンドルの下位 16 ビットのみです。上位の部分を確認するには、コードですべてのオープン ウィンドウを反復処理し、上位の部分との一致を見つける必要があります。Excel 2007 以降では、**XLOPER12** の整数変数は 32 ビットの符号付き整数になり、すべてのオープン ウィンドウを反復処理する必要がなくなっています。</span><span class="sxs-lookup"><span data-stu-id="74c70-p101">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle. To find the high part, your code must iterate through all open windows looking for a match with the low part. Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="74c70-116">例</span><span class="sxs-lookup"><span data-stu-id="74c70-116">Example</span></span>

<span data-ttu-id="74c70-117">`SAMPLES\GENERIC\GENERIC.C` で、[fShowDialog 関数](fshowdialog.md) のコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="74c70-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74c70-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="74c70-118">See also</span></span>

- [<span data-ttu-id="74c70-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="74c70-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="74c70-120">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="74c70-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

