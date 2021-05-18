---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- xlautofree function [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413291"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="c53ec-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="c53ec-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="c53ec-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c53ec-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c53ec-p101">XLL ワークシート関数が **XLOPER**/ **XLOPER12** を返した直後に、XLL で解放する必要のあるメモリがまだあることを示すフラグを設定するために Excel によって呼び出されます。これにより、動的に割り当てられた配列、文字列および外部参照をメモリ リークなしに XLL でワークシートに返せるようになります。詳細については、「[Excel でのメモリ管理](memory-management-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p101">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release. This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="c53ec-109">**xlAutoFree12** 関数と **XLOPER12** データ型は、Excel 2007 以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c53ec-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="c53ec-p102">Excel では、XLL がこれらいずれかの関数を実装してエクスポートする必要はありません。ただし、動的にメモリが割り当てられている、または動的に割り当てられたメモリへのポインターを含んでいる XLOPER または XLOPER12 を XLL 関数が返す場合は、その必要があります。これらのデータ型に選択するメモリ管理の方法は、XLL 全体での一貫性を確保し、**xlAutoFree** および **xlAutoFree12** の実装方法と矛盾しないようにします。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p102">Excel does not require an XLL to implement and export either of these functions. However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory. Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="c53ec-113">**xlAutoFree**/ **xlAutoFree12** 関数の内部では、Excel へのコールバックは無効化されています。これには 1 つの例外があり、Excel によって割り当てられたメモリを解放するための **xlFree** の呼び出しは可能です。</span><span class="sxs-lookup"><span data-stu-id="c53ec-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="c53ec-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c53ec-114">Parameters</span></span>

 <span data-ttu-id="c53ec-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="c53ec-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="c53ec-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="c53ec-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="c53ec-117">解放する必要のあるメモリが割り当てられている **XLOPER** または **XLOPER12** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c53ec-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c53ec-118">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="c53ec-118">Property value/Return value</span></span>

<span data-ttu-id="c53ec-119">この関数は値を返しません。void を返すように宣言されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c53ec-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c53ec-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c53ec-120">Remarks</span></span>

<span data-ttu-id="c53ec-p103">Excel がマルチスレッドのブックの再計算を使用するように構成されている場合、**xlAutoFree**/ **xlAutoFree12** は、それを返した関数の呼び出しに使用されたスレッドと同じスレッドで呼び出されます。**xlAutoFree**/ **xlAutoFree12** の呼び出しは、常に、そのスレッドで後続のワークシートのセルが評価される前に行われます。これにより、XLL でのスレッド セーフな設計が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p103">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it. The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread. This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="c53ec-124">カスタムの **xlAutoFree**/ **xlAutoFree12** 関数で _pxFree_ の **xltype** フィールドを調べる場合は、**xlbitDLLFree** ビットが設定されたままになっている点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="c53ec-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c53ec-125">例</span><span class="sxs-lookup"><span data-stu-id="c53ec-125">Example</span></span>

 <span data-ttu-id="c53ec-126">**実装例 1**</span><span class="sxs-lookup"><span data-stu-id="c53ec-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="c53ec-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C` の最初のコードでは、非常に特殊な **xlAutoFree** の実装例を示しています。これは 1 つの関数 **fArray** だけに使用するように設計されています。一般に、XLL には解放する必要のあるメモリを返す関数が複数あります。その場合は、あまり限定的でない実装が必要になります。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p104">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**. In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="c53ec-129">**実装例 2**</span><span class="sxs-lookup"><span data-stu-id="c53ec-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="c53ec-p105">2 番目の実装例は、セクション 1.6.3、xl12_Str_example、xl12_Ref_example、および xl12_Multi_example の **XLOPER12** の作成例で使用した前提条件に適合します。その前提条件とは、「**xlbitDLLFree** ビットが設定されているときには、すべての文字列、配列、および外部参照メモリが **malloc** を使用して動的に割り当てられていて、free の呼び出しで解放する必要がある」というものです。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p105">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example. The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="c53ec-132">**実装例 3**</span><span class="sxs-lookup"><span data-stu-id="c53ec-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="c53ec-p106">3 番目の実装例は、**malloc** を使用して **XLOPER12** が割り当てた文字列、外部参照および配列を返す関数をエクスポートした XLL、または **XLOPER12** 自体も動的に割り当てられた XLL に適合します。動的に割り当てられた **XLOPER12** へのポインターが一方向に返されることで、関数がスレッド セーフであることを保証します。</span><span class="sxs-lookup"><span data-stu-id="c53ec-p106">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated. Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="c53ec-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="c53ec-135">See also</span></span>



[<span data-ttu-id="c53ec-136">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="c53ec-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

