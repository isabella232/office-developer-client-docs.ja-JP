---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798963"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="49bf0-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="49bf0-103">xlAsyncReturn</span></span>

<span data-ttu-id="49bf0-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="49bf0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="49bf0-105">�񓯊����[�U�[��\`�֐� (UDF) �̌��ʂ�Ԃ����߂Ɏg�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="49bf0-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="49bf0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="49bf0-106">Parameters</span></span>

<span data-ttu-id="49bf0-107">_pxAsyncHandle_(**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="49bf0-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="49bf0-108">���ʂ�Ԃ���� UDF �̔񓯊��n���h���ł��B</span><span class="sxs-lookup"><span data-stu-id="49bf0-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="49bf0-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="49bf0-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="49bf0-110">UDF �̖߂�l�ł��B</span><span class="sxs-lookup"><span data-stu-id="49bf0-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="49bf0-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="49bf0-111">Property value/Return value</span></span>

<span data-ttu-id="49bf0-112">成功した場合は、 **TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="49bf0-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="49bf0-113">失敗した場合は、 **FALSE**が返されます。</span><span class="sxs-lookup"><span data-stu-id="49bf0-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49bf0-114">����</span><span class="sxs-lookup"><span data-stu-id="49bf0-114">Remarks</span></span>

<span data-ttu-id="49bf0-p102">**xlAsyncReturn** �́A�Čv�Z���Ɍv�Z�ȊO�̃X���b�h�� Excel ���g�p�������B��̃R�[���o�b�N�ł��B�񓯊� UDF �̔񓯊��ȕ������A **xlAsyncReturn** �ȊO�̂����Ȃ�R�[���o�b�N����s���Ȃ��悤�ɂ���K�v������܂��BXLL �́A�߂�l��ێ����邽�߂ɁA���蓖�Ă�ꂽ��������������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="49bf0-p102">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation. The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**. The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="49bf0-118">_PxAsyncHandle_および_pxFunctionResult_パラメーターには、1 つのコールバックでは、ハンドルと対応する値の配列を返すために使用すると、タイプ**xltypeMulti**のことができます。</span><span class="sxs-lookup"><span data-stu-id="49bf0-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="49bf0-119">単一のコールバックを使用して、1 つの値を返す非同期ハンドルが格納されている次元の配列を含む XLOPER12 構造体を指す、LPXLOPER12 を渡します。</span><span class="sxs-lookup"><span data-stu-id="49bf0-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="49bf0-120">これらのアレイは、excel の場合、対応する値を持つ非同期のハンドルを正しく一致するように同じ順序でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="49bf0-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="49bf0-121">���̗�́A **xlAsyncReturn** ��g�p���āA�o�b�\`�Ăяo����쐬������@������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="49bf0-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="49bf0-122">�֘A����</span><span class="sxs-lookup"><span data-stu-id="49bf0-122">See also</span></span>

- <span data-ttu-id="49bf0-123">[�񓯊��̃��[�U�[��\`�֐�](asynchronous-user-defined-functions.md)</span><span class="sxs-lookup"><span data-stu-id="49bf0-123">[Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md)</span></span>

