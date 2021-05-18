---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412465"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="6828e-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="6828e-104">xlGetBinaryName</span></span>

<span data-ttu-id="6828e-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6828e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6828e-p101">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md). Data with a defined binary name is saved with the workbook and can be accessed by name at any time. For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="6828e-p101">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md). Data with a defined binary name is saved with the workbook and can be accessed by name at any time. For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="6828e-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6828e-109">Parameters</span></span>

<span data-ttu-id="6828e-110">_pxRes_ (**xltypeBigData** または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="6828e-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="6828e-p102">取得されたデータまたはエラーを指定する Bigdata 構造体は、取得できなかったデータまたは定義されていない名前になります。関数が戻った時点で、**XLOPER**/ **XLOPER12** の **hdata** メンバーに名前付きデータのハンドルが格納されています。_pxRes_ が不要になったら、**xlFree** の呼び出しでこれを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6828e-p102">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined. When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.  _pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="6828e-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="6828e-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="6828e-115">データの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="6828e-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6828e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="6828e-116">Remarks</span></span>

<span data-ttu-id="6828e-p103">Microsoft Excel は、**hdata** で返されたメモリ ハンドルを所有します。Windows では、このハンドルはグローバル メモリ ハンドルです (**GlobalAlloc** 関数によって割り当てられます)。</span><span class="sxs-lookup"><span data-stu-id="6828e-p103">Microsoft Excel owns the memory handle returned in **hdata**. In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6828e-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="6828e-119">See also</span></span>

- [<span data-ttu-id="6828e-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="6828e-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="6828e-121">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="6828e-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

