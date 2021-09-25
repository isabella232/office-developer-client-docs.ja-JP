---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 36560fc0362654a209f87feb74e548cd5b68f809
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596807"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
非同期ユーザー定義関数 (UDF) の結果を返すために使用します。
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>パラメーター

_pxAsyncHandle_ (**xltypeBigData**)
  
結果を返す先の UDF の非同期ハンドルです。
  
_pxFunctionResult_
  
UDF の戻り値です。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は、**TRUE** (**xltypeBool**) が返されます。失敗した場合は、**FALSE** が返されます。
  
## <a name="remarks"></a>注釈

**xlAsyncReturn** は、再計算中に Excel が非計算スレッドに対して許可する唯一のコールバックです。非同期 UDF の非同期の部分では、**xlAsyncReturn** 以外のコールバックを実行できません。XLL は戻り値を保持するために、割り当てられたメモリを解放する必要があります。
  
_pxAsyncHandle_ および _pxFunctionResult_ パラメーターを、シングル コールバックでハンドルの配列と対応する値を返すために使用する場合、これらのパラメーターを **xltypeMulti** 型にすることもできます。 シングル コールバックを使用するときは、非同期ハンドルと戻り値を含む 1 次元の配列からなる XLOPER12 構造を指す LPXLOPER12 を渡します。 これらの配列は、非同期ハンドルが対応する値と正しく一致するよう、Excel に対して同じ順序である必要があります。 
  
次の例は、**xlAsyncReturn** を使用して、バッチ呼び出しを作成する方法を示しています。
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a>関連項目

- [非同期のユーザー定義関数](asynchronous-user-defined-functions.md)

