---
title: 名前と他のワークシートの数式を評価する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],worksheets [Excel 2007], name evaluation,evaluating expressions [Excel 2007],evaluating worksheet names [Excel 2007],expressions [Excel 2007], evaluating,names [Excel 2007], evaluating,name evaluation [Excel 2007],strings [Excel 2007], converting to values,xlfEvaluate function [Excel 2007],worksheets [Excel 2007], expression evaluation
localization_priority: Normal
ms.assetid: 2b23c75e-2a95-4f26-8714-2a73f5e326a7
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9d726d89c859e2f7428b459971d5d13586f144e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798796"
---
# <a name="evaluating-names-and-other-worksheet-formula-expressions"></a><span data-ttu-id="ebaf0-104">名前と他のワークシートの数式を評価する</span><span class="sxs-lookup"><span data-stu-id="ebaf0-104">Evaluating Names and Other Worksheet Formula Expressions</span></span>

<span data-ttu-id="ebaf0-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ebaf0-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ebaf0-p101">Excel が、C API で公開する最も重要な機能の 1 つは、ワークシートに合法的に入力できる文字列式を単一の値や値の配列に変換する機能です。これは、定義された名前のコンテンツを読み取る必要がある XLL 関数とコマンドなどにとって不可欠です。この機能は、以下の例に示すように、[xlfEvaluate 関数](xlfevaluate.md)で公開されます。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p101">One of the most important features that Excel exposes through the C API is the ability to convert any string formula that can legally be entered into a worksheet to a value, or array of values. This is essential for XLL functions and commands that must read the contents of defined names, for example. This ability is exposed through the [xlfEvaluate function](xlfevaluate.md), as shown in this example.</span></span>
  
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

<span data-ttu-id="ebaf0-p102">ワークシート名を、それ自体か式で評価する場合、少なくとも、名前は ‘!’ というプレフィックスで始める必要があります。そうしないと、Excel は Dll 用に予約されている非表示の名前空間内でその名前を見つけようとします。[xlfSetName 関数](xlfsetname.md)を使って、非表示の DLL 名の作成と削除ができます。非表示の DLL 名かワークシート名かに関係なく、**xlfGetDef** 関数を使って、定義されたどの名前の定義でも取得できます。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p102">Note that when you are evaluating a worksheet name, either on its own or in a formula, you must prefix the name with '!', at least. Otherwise, Excel tries to find the name in a hidden namespace reserved for DLLs. You can create and delete hidden DLL names using the [xlfSetName function](xlfsetname.md). You can get the definition of any defined name, whether it is a hidden DLL name or a worksheet name, using the **xlfGetDef** function.</span></span> 
  
<span data-ttu-id="ebaf0-113">ワークシート名全体の指定は、次のような形式です。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-113">The full specification for a worksheet name takes the following form:</span></span>
  
`='C:\example folder\[Book1.xls]Sheet1'!Name`
  
<span data-ttu-id="ebaf0-p103">Excel 2007 では、いくつかの新しいファイル拡張子が導入されました。この Excel セッションで開いているブック間にあいまいな箇所がない場合は、パス、ブック名、シート名を省略することができます。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p103">Note that Excel 2007 introduced a number of new file extensions. You can omit the path, the workbook name, and the sheet name where there is no ambiguity among the open workbooks in this Excel session.</span></span> 
  
<span data-ttu-id="ebaf0-p104">次の例は、作業中のワークシートの式 `COUNT(A1:IV65536)` を評価して、結果を表示します。範囲アドレスは '!' というプレフィックスで始める必要があることに注意してください。これは、XLM マクロ シートの範囲参照の規則と一致しています。C API XLM は、この規則に従っています。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p104">The next example evaluates the formula  `COUNT(A1:IV65536)` for the active worksheet and displays the result. Note the need to prefix the range address with '!', which is consistent with the range reference convention on XLM macro sheets. The C API XLM follows this convention:</span></span> 
  
- <span data-ttu-id="ebaf0-p105">`=A1` 現在のマクロ シートのセル A1 への参照 (XLL に対しては定義されていません)。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p105">`=A1` A reference to cell A1 on the current macro sheet. (Not defined for XLLs).</span></span> 
  
- <span data-ttu-id="ebaf0-121">`=!A1` 作業中のシート (ワークシートまたはマクロ シートを指定できます) のセル A1 への参照。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-121">`=!A1` A reference to cell A1 on the active sheet (which could be a worksheet or macro sheet)</span></span> 
  
- <span data-ttu-id="ebaf0-122">`=Sheet1!A1` 指定されたシート (この場合は Sheet1) のセル A1 への参照。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-122">`=Sheet1!A1` A reference to cell A1 on the specified sheet, Sheet1 in this case.</span></span> 
  
- <span data-ttu-id="ebaf0-123">`=[Book1.xls]Sheet1!A1` 指定されたブックの指定されたシートのセル A1 への参照。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-123">`=[Book1.xls]Sheet1!A1` A reference to cell A1 on the specified sheet in the specified workbook.</span></span> 
  
<span data-ttu-id="ebaf0-124">XLL では、先頭に感嘆符 (**!**) がない参照を値に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-124">In an XLL, a reference without a leading exclamation point (**!**) cannot be converted to a value.</span></span> <span data-ttu-id="ebaf0-125">現在のマクロ シートがないため、意味がありません。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-125">It has no meaning because there is no current macro sheet.</span></span> <span data-ttu-id="ebaf0-126">先頭に等号 (**=**) を付けることはオプションであるため、次の例では省略します。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-126">Note that a leading equals sign (**=**) is optional and is omitted in the next example.</span></span>
  
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

<span data-ttu-id="ebaf0-127">また、**xlfEvaluate** 関数を使って、XLL 関数の登録 ID を登録されている名前から取得します。その後、[xlUDF 関数](xludf.md)を使ってその関数を呼び出すために、取得した XLL 関数の登録 ID を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-127">You can also use the **xlfEvaluate** function to retrieve the registration ID of an XLL function from its registered name, which can then be used to call that function using the [xlUDF function](xludf.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ebaf0-p107">登録されている名前は、**xlUDF** 関数に直接渡すことができます。つまり、名前を評価して ID を取得せずに、**xlUDF** を呼び出すことができるということです。ただし、関数を何度も呼び出す場合、登録 ID を使って呼び出すほうが速くなります。</span><span class="sxs-lookup"><span data-stu-id="ebaf0-p107">The registered name can be passed directly to the **xlUDF** function. This means that you can avoid having to evaluate the name to get the ID before calling **xlUDF**. However, if the function is to be called many times, calling it by using the registration ID is faster.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ebaf0-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebaf0-131">See also</span></span>

- [<span data-ttu-id="ebaf0-132">Excel ワークシートと式の評価</span><span class="sxs-lookup"><span data-stu-id="ebaf0-132">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)
- [<span data-ttu-id="ebaf0-133">時間のかかる操作でユーザーによる中断を許可する</span><span class="sxs-lookup"><span data-stu-id="ebaf0-133">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="ebaf0-134">Excel XLL SDK の概要</span><span class="sxs-lookup"><span data-stu-id="ebaf0-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

