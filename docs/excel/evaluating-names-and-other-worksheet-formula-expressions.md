---
title: 名前と他のワークシートの数式を評価する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
ms.localizationpriority: medium
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f2a9f1221acead606b71eedf6deb09133ad25a39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552256"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a>名前と他のワークシートの数式を評価する

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel が、C API で公開する最も重要な機能の 1 つは、ワークシートに合法的に入力できる文字列式を単一の値や値の配列に変換する機能です。これは、定義された名前のコンテンツを読み取る必要がある XLL 関数とコマンドなどにとって不可欠です。この機能は、以下の例に示すように、[xlfEvaluate 関数](xlfevaluate.md)で公開されます。
  
```C
int WINAPI evaluate_name_example(void)
{
  wchar_t *expression = L"\016!MyDefinedName";
  XLOPER12 xNameText, xNameValue;
  xNameText.xltype = xltypeStr;
  xNameText.val.str = expression;
// Try to evaluate the name. Will fail with a #NAME? error
// if MyDefinedName is not defined in the active workbook.
  Excel12(xlfEvaluate, &xNameValue, 1, &xNameText);
// Attempt to convert the value to a string and display it in
// an alert dialog. This fails if xNameValue is an error value.
  Excel12(xlcAlert, 0, 1, &xNameValue);
// Must free xNameValue in case MyDefinedName evaluated to a string
  Excel12(xlFree, 0, 1, &xNameValue);
  return 1;
}
```

ワークシート名を、それ自体か式で評価する場合、少なくとも、名前は ‘!’ というプレフィックスで始める必要があります。そうしないと、Excel は Dll 用に予約されている非表示の名前空間内でその名前を見つけようとします。[xlfSetName 関数](xlfsetname.md)を使って、非表示の DLL 名の作成と削除ができます。非表示の DLL 名かワークシート名かに関係なく、**xlfGetDef** 関数を使って、定義されたどの名前の定義でも取得できます。 
  
ワークシート名全体の指定は、次のような形式です。
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
Excel 2007 では、いくつかの新しいファイル拡張子が導入されました。この Excel セッションで開いているブック間にあいまいな箇所がない場合は、パス、ブック名、シート名を省略することができます。 
  
次の例は、作業中のワークシートの式 `COUNT(A1:IV65536)` を評価して、結果を表示します。範囲アドレスは '!' というプレフィックスで始める必要があることに注意してください。これは、XLM マクロ シートの範囲参照の規則と一致しています。C API XLM は、この規則に従っています。 
  
- `=A1` 現在のマクロ シートのセル A1 への参照 (XLL に対しては定義されていません)。 
  
- `=!A1` 作業中のシート (ワークシートまたはマクロ シートを指定できます) のセル A1 への参照。 
  
- `=Sheet1!A1` 指定されたシート (この場合は Sheet1) のセル A1 への参照。 
  
- `=[Book1.xls]Sheet1!A1` 指定されたブックの指定されたシートのセル A1 への参照。 
  
XLL では、先頭に感嘆符 (**!**) がない参照を値に変換することはできません。 現在のマクロ シートがないため、意味がありません。 先頭に等号 (**=**) を付けることはオプションであるため、次の例では省略します。
  
```C
int WINAPI evaluate_expression_example(void)
{
    wchar_t *expression = L"\022COUNT(!A1:IV65536)";
    XLOPER12 xExprText, xExprValue;
    xExprText.xltype = xltypeStr;
    xExprText.val.str = expression;
// Try to evaluate the formula.
    Excel12(xlfEvaluate, &xExprValue, 1, &xExprText);
// Attempt to convert the value to a string and display it in
// an alert dialog. Will fail if xExprValue is an error.
    Excel12(xlcAlert, 0, 1, &xExprValue);
// Not strictly necessary, as COUNT never returns a string
// but does no harm.
    Excel12(xlFree, 0, 1, &xExprValue);
    return 1;
}
```

また、**xlfEvaluate** 関数を使って、XLL 関数の登録 ID を登録されている名前から取得します。その後、[xlUDF 関数](xludf.md)を使ってその関数を呼び出すために、取得した XLL 関数の登録 ID を使うことができます。
  
> [!NOTE]
> 登録されている名前は、**xlUDF** 関数に直接渡すことができます。つまり、名前を評価して ID を取得せずに、**xlUDF** を呼び出すことができるということです。ただし、関数を何度も呼び出す場合、登録 ID を使って呼び出すほうが速くなります。 
  
## <a name="see-also"></a>関連項目

- [Excel ワークシートと式の評価](excel-worksheet-and-expression-evaluation.md)
- [時間のかかる操作でユーザーによる中断を許可する](permitting-user-breaks-in-lengthy-operations.md)
- [Excel XLL SDK の概要](getting-started-with-the-excel-xll-sdk.md)

