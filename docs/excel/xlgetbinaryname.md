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
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798978"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="521d2-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="521d2-104">xlGetBinaryName</span></span>

<span data-ttu-id="521d2-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="521d2-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="521d2-106">[xlDefineBinaryName 関数](xldefinebinaryname.md)によって保存されたデータのハンドルを返すのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="521d2-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="521d2-107">定義されているバイナリ名が含まれるデータはブックに保存され、いつでも名前でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="521d2-107">Used to allocate persistent storage for an xltypeBigDataXLOPER/XLOPER12. Data with a defined binary name is saved with the workbook, and can be accessed by name at any time. For more information, see "Binary Name Scope Limitation" in Known Issues.</span></span> <span data-ttu-id="521d2-108">詳細については、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」の「バイナリ名のスコープ制限」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="521d2-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="521d2-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="521d2-109">Parameters</span></span>

<span data-ttu-id="521d2-110">_pxRes _ (**xltypeBigData** または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="521d2-110">_pxRes _(**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="521d2-p102">取得されたデータまたはエラーを指定する Bigdata 構造体は、取得できなかったデータまたは定義されていない名前になります。関数が戻った時点で、**XLOPER**/ **XLOPER12** の **hdata** メンバーに名前付きデータのハンドルが格納されています。_pxRes_ が不要になったら、**xlFree** の呼び出しでこれを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="521d2-p102">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined. When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.  _pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="521d2-114">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="521d2-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="521d2-115">データの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="521d2-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="521d2-116">注釈</span><span class="sxs-lookup"><span data-stu-id="521d2-116">Remarks</span></span>

<span data-ttu-id="521d2-p103">Microsoft Excel は、**hdata** で返されたメモリ ハンドルを所有します。Windows では、このハンドルはグローバル メモリ ハンドルです (**GlobalAlloc** 関数によって割り当てられます)。</span><span class="sxs-lookup"><span data-stu-id="521d2-p103">Microsoft Excel owns the memory handle returned in **hdata**. In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="521d2-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="521d2-119">See also</span></span>

- [<span data-ttu-id="521d2-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="521d2-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="521d2-121">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="521d2-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

