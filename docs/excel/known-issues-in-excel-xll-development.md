---
title: Excel アドイン (XLL) 開発における既知の問題
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- known issues [excel 2007]
ms.localizationpriority: medium
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d44a006802bfbb2e86d04e672253c1ad26a71b1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568174"
---
# <a name="known-issues-in-excel-xll-development"></a>Excel アドイン (XLL) 開発における既知の問題

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
このトピックでは、Microsoft Excel での XLL 開発で遭遇する可能性のある既知の問題について説明します。
  
## <a name="unregistering-xll-commands-and-functions"></a>XLL のコマンドおよび関数を登録解除する

When an XLL registers a function or command, Excel creates a new name for the resource and associates a reference to the DLL function with that name. The name is taken from the fourth argument,  *pxFunctionText*  , of the [xlfRegister](xlfregister-form-1.md) function. This name is hidden from the normal dialog boxes for managing worksheet names. To unregister a function or command, you must delete the name by using the [xlfSetName](xlfsetname.md) function, passing the name but not passing a definition. However, a bug prevents this from removing the name from the Function Wizard lists. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>関数ウィザードにおける引数の説明文字列の切り捨て

*PxArgumentHelp1* パラメーターと、その後の **xlfRegister** 関数のパラメーターはすべて、XLL 関数の引数に相当し、文字列は省略することができます。 引数作成ダイアログ ボックスにヘルプを表示するために、関数ウィザードにはこれらのパラメータが表示されます。 ダイアログ ボックスに表示する際、最後の引数に相当する文字列が Excel 上で 1 文字または 2 文字切り捨てられる場合があります。 これを回避するために、関数登録の最後の「引数ヘルプ」パラメーターとして付加的な「空の文字列」を追加できます。
  
## <a name="binary-name-scope-limitation"></a>バイナリ名のスコープ制限

バイナリ名とそのデータは、作成された時点でアクティブだったワークシートが再度アクティブになったときにのみ取得できます。ワークシート関数では、ワークブック内のワークシートをアクティブにすることはできないため (コマンドでのみ可能)、バイナリ名の適用は非常に制限されています。特定のワークシートからのみ呼び出されるコマンドがあれば、バイナリ名を使用してコマンドに関するデータを格納することもできます。
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet と配列数式を含むワークブック

In Excel 2003 and earlier versions, the [xlSet function](xlset.md) fails if you try to assign values to a range on a worksheet that is not the active worksheet, where the equivalent range on the active sheet contains an array formula. In this case, Excel displays the message "You cannot change part of an array." This was fixed in Excel 2007. 
  
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

