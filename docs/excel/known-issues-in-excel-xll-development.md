---
title: Excel アドイン (XLL) 開発における既知の問題
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- known issues [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685180"
---
# <a name="known-issues-in-excel-xll-development"></a>Excel アドイン (XLL) 開発における既知の問題

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
このトピックでは、Microsoft Excel での XLL 開発で遭遇する可能性のある既知の問題について説明します。
  
## <a name="unregistering-xll-commands-and-functions"></a>XLL のコマンドおよび関数を登録解除する

XLL で関数やコマンドを登録すると、Excel 上で新しいリソース名が作成され、そのリソース名を持つ DLL 関数の参照と関連付けられます。 このリソース名は、[xlfRegister](xlfregister-form-1.md) 関数の 4 番目の引数である *pxFunctionText* から取得されます。 また、このリソース名は、ワークシート名を管理する標準のダイアログ ボックスからは非表示になっています。 関数やコマンドを登録解除するには、[xlfSetName](xlfsetname.md) 関数を使用してリソース名を削除する必要があります。この際、リソース名を渡しますが、定義は渡しません。 ただし、バグがあると、この関数ウィザードの一覧からリソース名を削除することができません。 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>関数ウィザードにおける引数の説明文字列の切り捨て

*PxArgumentHelp1* パラメーターと、その後の **xlfRegister** 関数のパラメーターはすべて、XLL 関数の引数に相当し、文字列は省略することができます。 引数作成ダイアログ ボックスにヘルプを表示するために、関数ウィザードにはこれらのパラメータが表示されます。 ダイアログ ボックスに表示する際、最後の引数に相当する文字列が Excel 上で 1 文字または 2 文字切り捨てられる場合があります。 これを回避するために、関数登録の最後の「引数ヘルプ」パラメーターとして付加的な「空の文字列」を追加できます。
  
## <a name="binary-name-scope-limitation"></a>バイナリ名のスコープ制限

バイナリ名とそのデータは、作成された時点でアクティブだったワークシートが再度アクティブになったときにのみ取得できます。ワークシート関数では、ワークブック内のワークシートをアクティブにすることはできないため (コマンドでのみ可能)、バイナリ名の適用は非常に制限されています。特定のワークシートからのみ呼び出されるコマンドがあれば、バイナリ名を使用してコマンドに関するデータを格納することもできます。
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet と配列数式を含むワークブック

Excel 2003 以前のバージョンにおいて、作業中ではないワークシートの範囲に値を割り当てようとすると、[xlSet 関数](xlset.md) はエラーになり、作業中のシート上の同等範囲に配列数式が入ります。 この場合、「配列の一部を変更できません」というメッセージが表示されます。 この問題は、Excel 2007 で修正されました。 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>データ テーブルで循環参照が可能

Excel では現在、データ テーブルのベースとなる計算において、同テーブル上の値を参照している場合でもエラーになりません。このようなシナリオはまれなことですが、データ テーブルの値を計算する数式の作成や変更には注意が必要です。
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>整数 XLOPER12 を XLOPER に変換する

整数型 **xltypeInt** は、**XLOPER12** データ型では 32 ビットの符号付き整数ですが、**XLOPER** データ型では 16 ビット符号付き整数であるため、整数 **XLOPER12** の値の中には、整数 **XLOPER** に含められないものがある可能性があります。Excel 内部でこのデータ型を変換する場合は、データ型を浮動小数点 **xltypeNum** **XLOPER** に変換してこの問題を回避します。
  
フレームワーク関数 [XLOper12ToXLOper](xloper12toxloper.md) は、この動作を反映して、Excel 内部の動作と一致するようにします。この関数を呼び出す際、返される **XLOPER** が常に **xltypeInt** であると想定しないでください。**my_xloper** 型が **xltypeNum** の場合に **my_xloper.val.w** を読み出すと、false の値が返されます。
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>引数をインプレースで変更して XLOPER または XLOPER12 を返す

Excel では引数をインプレースで変更して、**XLOPER** または **XLOPER12** を返すように関数を登録することができます。しかし、**XLOPER**/ **XLOPER12** 引数がメモリをポイントしており、そのポインターが DLL 関数の戻り値で上書きされると、Excel でメモリ リークが発生する可能性があります。Excel でエラーは表示されませんが、結果的にクラッシュする恐れがあります。また、DLL で戻り値用のメモリが割り当てられている場合、Excel はそのメモリを解放しようとするため、すぐにアプリケーションがクラッシュする恐れがあります。そのため、**XLOPER**/ **XLOPER12** 引数はインプレースで変更しないでください。**XLOPER** 引数や **XLOPER12** 引数はすべて、必ず読み取り専用として扱ってください。 
  
詳細については、「[Excel のメモリ管理](memory-management-in-excel.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[XLOper12ToXLOper](xloper12toxloper.md)


[Excel XLL の開発](developing-excel-xlls.md)
  
[Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)
  
[Excel のメモリ管理](memory-management-in-excel.md)

