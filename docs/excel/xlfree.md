---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree function [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424715"
---
# <a name="xlfree"></a><span data-ttu-id="2a8ea-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="2a8ea-104">xlFree</span></span>

 <span data-ttu-id="2a8ea-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a8ea-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2a8ea-p101">[Excel4](excel4-excel12.md)、[Excel4v](excel4v-excel12v.md)、[Excel12](excel4-excel12.md)、または [Excel12v](excel4v-excel12v.md) の呼び出しで戻り値 **XLOPER**/ **XLOPER12** を作成するときに、Microsoft Excel が割り当てたメモリ リソースを解放するために使用します。**xlFree** 関数は補助メモリを解放し、ポインターを **NULL** にリセットしますが、**XLOPER**/ **XLOPER12** の他の部分は破棄しません。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-p101">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md). The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="2a8ea-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2a8ea-108">Parameters</span></span>

 <span data-ttu-id="2a8ea-109">_px_1, ..., px_n_</span><span class="sxs-lookup"><span data-stu-id="2a8ea-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="2a8ea-p102">解放する 1 つ以上の **XLOPER**/ **XLOPER12**。Excel 2003 までのバージョンでは、渡せるポインターの最大数は 30 です。Excel 2007 以降は、255 に増加されました。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-p102">One or more **XLOPER**/ **XLOPER12**s to be freed. In Excel versions up to 2003, the maximum number of pointers that can be passed is 30. Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2a8ea-113">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="2a8ea-113">Property value/Return value</span></span>

<span data-ttu-id="2a8ea-114">この関数は値を返しません。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a8ea-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2a8ea-115">Remarks</span></span>

<span data-ttu-id="2a8ea-p103">**Excel4** または **Excel4v** から戻り値として取得した **XLOPER**、および **Excel12** または **Excel12v** から戻り値として取得した **XLOPER12** は、型が **xltypeStr**、**xltypeMulti**、または **xltypeRef** のいずれかの場合はすべて解放する必要があります。他の型を解放しても、それが **Excel4** または **Excel12** から取得したものである限り、たとえそれが補助メモリを使用しない場合でも、問題が生じることはありません。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-p103">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**. It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="2a8ea-118">解放対象の Excel が割り当てたメモリを含む **XLOPER**/ **XLOPER12** へのポインターを Excel に戻す場合、**xlbitXLFree** を設定して Excel にメモリを確実に解放させます。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2a8ea-119">例</span><span class="sxs-lookup"><span data-stu-id="2a8ea-119">Example</span></span>

<span data-ttu-id="2a8ea-p104">この例では **GET.WORKSPACE(1)** を呼び出し、Excel を実行中のプラットフォームを文字列として返します。コードは返された文字列を後で使用するためにバッファーにコピーします。コードはこのバッファーを後で Excel 関数で使用するために **XLOPER12** に戻します。最後に、コードは警告ボックスに文字列を表示します。</span><span class="sxs-lookup"><span data-stu-id="2a8ea-p104">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string. The code copies this returned string into a buffer for later use. The code places the buffer back into the **XLOPER12** for later use with the Excel function. Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2a8ea-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2a8ea-124">See also</span></span>

- [<span data-ttu-id="2a8ea-125">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="2a8ea-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

