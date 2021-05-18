---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414110"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="b7b3d-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="b7b3d-103">xlAsyncReturn</span></span>

<span data-ttu-id="b7b3d-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b7b3d-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b7b3d-105">非同期ユーザー定義関数 (UDF) の結果を返すために使用します。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="b7b3d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b7b3d-106">Parameters</span></span>

<span data-ttu-id="b7b3d-107">_pxAsyncHandle_ (**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="b7b3d-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="b7b3d-108">結果を返す先の UDF の非同期ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="b7b3d-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="b7b3d-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="b7b3d-110">UDF の戻り値です。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b7b3d-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="b7b3d-111">Property value/Return value</span></span>

<span data-ttu-id="b7b3d-p101">成功した場合は、**TRUE** (**xltypeBool**) が返されます。失敗した場合は、**FALSE** が返されます。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-p101">If successful, returns **TRUE** (**xltypeBool**). If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7b3d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b7b3d-114">Remarks</span></span>

<span data-ttu-id="b7b3d-p102">**xlAsyncReturn** は、再計算中に Excel が非計算スレッドに対して許可する唯一のコールバックです。非同期 UDF の非同期の部分では、**xlAsyncReturn** 以外のコールバックを実行できません。XLL は戻り値を保持するために、割り当てられたメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-p102">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation. The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**. The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="b7b3d-118">_pxAsyncHandle_ および _pxFunctionResult_ パラメーターを、シングル コールバックでハンドルの配列と対応する値を返すために使用する場合、これらのパラメーターを **xltypeMulti** 型にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="b7b3d-119">シングル コールバックを使用するときは、非同期ハンドルと戻り値を含む 1 次元の配列からなる XLOPER12 構造を指す LPXLOPER12 を渡します。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="b7b3d-120">これらの配列は、非同期ハンドルが対応する値と正しく一致するよう、Excel に対して同じ順序である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="b7b3d-121">次の例は、**xlAsyncReturn** を使用して、バッチ呼び出しを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b7b3d-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b7b3d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7b3d-122">See also</span></span>

- [<span data-ttu-id="b7b3d-123">非同期のユーザー定義関数</span><span class="sxs-lookup"><span data-stu-id="b7b3d-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

