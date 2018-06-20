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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�񓯊����[�U�[��`�֐� (UDF) �̌��ʂ�Ԃ����߂Ɏg�p���܂��B
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>�p�����[�^�[

_pxAsyncHandle_(**xltypeBigData**)
  
���ʂ�Ԃ���� UDF �̔񓯊��n���h���ł��B
  
_pxFunctionResult_
  
UDF �̖߂�l�ł��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は、 **TRUE** (**xltypeBool**) を返します。 失敗した場合は、 **FALSE**が返されます。
  
## <a name="remarks"></a>����

**xlAsyncReturn** �́A�Čv�Z���Ɍv�Z�ȊO�̃X���b�h�� Excel ���g�p�������B��̃R�[���o�b�N�ł��B�񓯊� UDF �̔񓯊��ȕ������A **xlAsyncReturn** �ȊO�̂����Ȃ�R�[���o�b�N����s���Ȃ��悤�ɂ���K�v������܂��BXLL �́A�߂�l��ێ����邽�߂ɁA���蓖�Ă�ꂽ��������������K�v������܂��B
  
_PxAsyncHandle_および_pxFunctionResult_パラメーターには、1 つのコールバックでは、ハンドルと対応する値の配列を返すために使用すると、タイプ**xltypeMulti**のことができます。 単一のコールバックを使用して、1 つの値を返す非同期ハンドルが格納されている次元の配列を含む XLOPER12 構造体を指す、LPXLOPER12 を渡します。 これらのアレイは、excel の場合、対応する値を持つ非同期のハンドルを正しく一致するように同じ順序でなければなりません。 
  
���̗�́A **xlAsyncReturn** ��g�p���āA�o�b�`�Ăяo����쐬������@������Ă��܂��B
  
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

## <a name="see-also"></a>�֘A����

- [�񓯊��̃��[�U�[��`�֐�](asynchronous-user-defined-functions.md)

