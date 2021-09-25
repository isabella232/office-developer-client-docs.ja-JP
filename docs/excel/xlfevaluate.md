---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate function [excel 2007]
ms.localizationpriority: medium
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 06526e4cf699cc24fd2cbc9d4cf54d6a018f9d99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557597"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel のパーサーと関数エバリュエーターを使用して、ワークシートのセルに入力できる任意の式を評価します。
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>パラメーター

 _pxFormulaText (xltypeStr)_
  
評価する文字列です。文字列は任意のテキストにできます。先頭の等号 (=) は省略可能です。これは正式に、ワークシートまたはマクロ シートのセルに入力できます。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

文字列の評価結果を返します。これは **xltypeNum**、**xltypeStr**、**xltypeBool**、**xltypeErr**、**xltypeNil**、**xltypeMulti** のいずれかになります。
  
## <a name="remarks"></a>注釈

文字列には関数のみを含めることができます。コマンドは対応しません。これは、数式バーで **F9** を押した場合と同じです。**xlfEvaluate** がスレッド セーフとして登録された XLL ワークシート関数から呼び出された場合、式にはスレッドセーフ関数のみを含める必要があります。 
  
The primary use of the **xlfEvaluate** function is to allow DLLs to find out the value assigned to a defined name that is either on a sheet or a hidden name defined within the DLL. Note that within a DLL/XLL, a worksheet name must be prefixed with at least an exclamation mark (!) to ensure that it is interpreted as external to the DLL. For more information, see [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** は、開かれていない外部シートへの参照の評価には使用できません。 
  
## <a name="example"></a>例

この例では、**xlfEvaluate** を使用して強制的にテキスト "!B38" をセル B38 の内容にします。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. この関数はコマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドから呼び出された場合にのみ正しく動作します。
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>関連項目

- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)

