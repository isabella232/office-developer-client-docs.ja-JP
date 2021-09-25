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
ms.localizationpriority: medium
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 225562a856ae631fd2bedfcd3ceecf137e836e63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552200"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
XLL ワークシート関数が **XLOPER**/ **XLOPER12** を返した直後に、XLL で解放する必要のあるメモリがまだあることを示すフラグを設定するために Excel によって呼び出されます。これにより、動的に割り当てられた配列、文字列および外部参照をメモリ リークなしに XLL でワークシートに返せるようになります。詳細については、「[Excel でのメモリ管理](memory-management-in-excel.md)」を参照してください。
  
**xlAutoFree12** 関数と **XLOPER12** データ型は、Excel 2007 以降でサポートされています。 
  
Excel では、XLL がこれらいずれかの関数を実装してエクスポートする必要はありません。ただし、動的にメモリが割り当てられている、または動的に割り当てられたメモリへのポインターを含んでいる XLOPER または XLOPER12 を XLL 関数が返す場合は、その必要があります。これらのデータ型に選択するメモリ管理の方法は、XLL 全体での一貫性を確保し、**xlAutoFree** および **xlAutoFree12** の実装方法と矛盾しないようにします。
  
**xlAutoFree**/ **xlAutoFree12** 関数の内部では、Excel へのコールバックは無効化されています。これには 1 つの例外があり、Excel によって割り当てられたメモリを解放するための **xlFree** の呼び出しは可能です。 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>パラメーター

 _pxFree_ (**LPXLOPER in the case of xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)
  
解放する必要のあるメモリが割り当てられている **XLOPER** または **XLOPER12** へのポインター。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数は値を返しません。void を返すように宣言されている必要があります。
  
## <a name="remarks"></a>注釈

Excel がマルチスレッドのブックの再計算を使用するように構成されている場合、**xlAutoFree**/ **xlAutoFree12** は、それを返した関数の呼び出しに使用されたスレッドと同じスレッドで呼び出されます。**xlAutoFree**/ **xlAutoFree12** の呼び出しは、常に、そのスレッドで後続のワークシートのセルが評価される前に行われます。これにより、XLL でのスレッド セーフな設計が簡単になります。 
  
カスタムの **xlAutoFree**/ **xlAutoFree12** 関数で _pxFree_ の **xltype** フィールドを調べる場合は、**xlbitDLLFree** ビットが設定されたままになっている点に注意してください。 
  
## <a name="example"></a>例

 **実装例 1**
  
`\SAMPLES\EXAMPLE\EXAMPLE.C` の最初のコードでは、非常に特殊な **xlAutoFree** の実装例を示しています。これは 1 つの関数 **fArray** だけに使用するように設計されています。一般に、XLL には解放する必要のあるメモリを返す関数が複数あります。その場合は、あまり限定的でない実装が必要になります。 
  
 **実装例 2**
  
2 番目の実装例は、セクション 1.6.3、xl12_Str_example、xl12_Ref_example、および xl12_Multi_example の **XLOPER12** の作成例で使用した前提条件に適合します。その前提条件とは、「**xlbitDLLFree** ビットが設定されているときには、すべての文字列、配列、および外部参照メモリが **malloc** を使用して動的に割り当てられていて、free の呼び出しで解放する必要がある」というものです。
  
 **実装例 3**
  
3 番目の実装例は、**malloc** を使用して **XLOPER12** が割り当てた文字列、外部参照および配列を返す関数をエクスポートした XLL、または **XLOPER12** 自体も動的に割り当てられた XLL に適合します。動的に割り当てられた **XLOPER12** へのポインターが一方向に返されることで、関数がスレッド セーフであることを保証します。 
  
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

## <a name="see-also"></a>関連項目



[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)

