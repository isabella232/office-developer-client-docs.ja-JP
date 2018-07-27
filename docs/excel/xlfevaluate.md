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
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798970"
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
  
**xlfEvaluate** 関数は、主に DLL が定義済みの名前に割り当てられた値を検索できるようにするために使用します。この名前はシート上にあるか、DLL 内で定義された非表示の名前です。 DLL/XLL 内では、ワークシートの名前に少なくとも感嘆符 (!) のプレフィックスを付けて、ワークシートが DLL の外部として解釈される必要があることに注意してください。 詳細については、「[名前と他のワークシートの式を評価する](evaluating-names-and-other-worksheet-formula-expressions.md)」を参照してください。
  
 **xlfEvaluate** は、開かれていない外部シートへの参照の評価には使用できません。 
  
## <a name="example"></a>例

この例では、**xlfEvaluate** を使用して強制的にテキスト "!B38" をセル B38 の内容にします。 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C` この関数はコマンド マクロ (**xlcAlert**) を呼び出し、マクロ シートまたはマクロ コマンドから呼び出された場合にのみ正しく動作します。
  
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

