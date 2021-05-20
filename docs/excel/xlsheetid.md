---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid function [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2ca1bb478c5c985ad7032e30ed0cfe3aef31406
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428432"
---
# <a name="xlsheetid"></a><span data-ttu-id="d6c00-104">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="d6c00-104">xlSheetId</span></span>

<span data-ttu-id="d6c00-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6c00-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d6c00-106">外部参照を作成するために、名前付きのシートのシート ID を検索します。</span><span class="sxs-lookup"><span data-stu-id="d6c00-106">Finds the sheet ID of a named sheet in order to construct external references.</span></span>
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a><span data-ttu-id="d6c00-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6c00-107">Parameters</span></span>

<span data-ttu-id="d6c00-108">_pxSheetName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d6c00-108">_pxSheetName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d6c00-p101">(Optional). The name of the book and sheet you want to find out about. If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span><span class="sxs-lookup"><span data-stu-id="d6c00-p101">(Optional). The name of the book and sheet you want to find out about. If omitted, the **xlSheetId** function returns the sheet ID of the active (front) sheet.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d6c00-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="d6c00-112">Return value</span></span>

<span data-ttu-id="d6c00-113">_pxRes-\>val.mref.idSheet_ 内にシート ID を返します。</span><span class="sxs-lookup"><span data-stu-id="d6c00-113">Returns the sheet ID in  _pxRes-\>val.mref.idSheet_.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6c00-114">_pxRes-\>val.mref.lpmref_ 配列ポインターは、この呼び出しの後で NULL に設定されるため、**xlFree** を呼び出して、このタイプに通常含まれているメモリを解放する必要はありません (これは完全に安全ですが必要ありません)。</span><span class="sxs-lookup"><span data-stu-id="d6c00-114">The  _pxRes-\>val.mref.lpmref_ array pointer is set to NULL after this call so that there is no need to call **xlFree** to release the memory that this type normally contains, although it is completely safe to do so.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d6c00-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d6c00-115">Remarks</span></span>

<span data-ttu-id="d6c00-p102">指定されたシートを含むブックは、この関数を使用するために開いている必要があります。DLL から開いていないブックへの参照を作成する方法はありません。**xlSheetId** を使用した参照の作成について詳しくは、「[Excel のメモリ管理](memory-management-in-excel.md)」で **xltypeRef** の作成例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6c00-p102">The workbook containing the specified sheet must be open to use this function. There is no way to construct a reference to an unopened workbook from a DLL. For more information about using **xlSheetId** to construct references, see [Memory Management in Excel](memory-management-in-excel.md) for examples of **xltypeRef** construction.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d6c00-119">例</span><span class="sxs-lookup"><span data-stu-id="d6c00-119">Example</span></span>

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d6c00-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6c00-120">See also</span></span>

- [<span data-ttu-id="d6c00-121">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="d6c00-121">xlSheetNm</span></span>](xlsheetnm.md)
- [<span data-ttu-id="d6c00-122">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="d6c00-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

