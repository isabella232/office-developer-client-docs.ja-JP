---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf function [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799000"
---
# <a name="xludf"></a>xlUDF

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
ユーザー定義関数 (UDF) を呼び出します。この関数により、DLL は Visual Basic for Applications (VBA) のユーザー定義関数、XLM マクロ言語の関数、およびその他のアドインに含まれる登録済みの関数を呼び出すことができます。
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>パラメーター

_pxFnRef_ (**xltypeRef**、**xltypeSRef**、**xltypeStr**、または **xltypeNum**)
  
呼び出す関数の参照。これはマクロ シートのセルの参照、文字列としての関数の登録名、または関数の登録 ID になります。_pxFunctionText_ 引数を指定した **xlfRegister** または **REGISTER** で登録された XLL アドイン関数の場合、**xlfEvaluate** を使用して名前を検索することで、この ID を取得できます。 
  
_pxArg1, ..._
  
ユーザー定義関数に渡すゼロ以上の引数。Excel 2007 より前のバージョンでこの関数を呼び出す場合、関数に渡せる追加引数の最大数は 29 です (_pxFnRef_ を含めると合計 30)。Excel 2007 以降では、この制限は 254 に引き上げられています (_pxFnRef_ を含めると合計 255)。
  
## <a name="return-value"></a>戻り値

ユーザー定義関数が返す値を返します。
  
## <a name="example"></a>例

次の例では、BOOK1.XLS のシート Macro1 に対して **TestMacro** を実行します。マクロが Macro1 という名前のシートにあることを確認してください。 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

