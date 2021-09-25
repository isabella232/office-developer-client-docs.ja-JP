---
title: Microsoft Access テーブル、フォーム、およびレポートの変換
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Microsoft Access 2002 によって導入された変更は、バージョン 1.x または 2.0 アプリケーションの動作に影響を与える可能性があります。
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7a3eec5e642f4a307fc9f0e812206d1360560f4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569280"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Microsoft Access テーブル、フォーム、およびレポートの変換

**適用先:** Access 2013、Office 2013

Access 2002 で導入された変更点が、Access Version 1.1 または 2.0 のアプリケーションの動作に影響を与える場合があります。以下に、変更の詳細を説明します。

## <a name="indexes-and-relationships"></a>インデックスとリレーションシップ

Microsoft Access テーブルに含めることができるインデックスは最大 32 個です。リレーションシップの "多" 側の複雑なテーブルでは、インデックスの制限値を超える可能性があり、このようなテーブルを含むデータベースは、変換することができません。Microsoft Access データベース エンジンはリレーションシップの両側のテーブルにインデックスを作成します。データベースを変換できない場合は、いくつかのリレーションシップを削除してからデータベースを変換し直してください。

## <a name="the-limittolist-property-of-combo-boxes"></a>コンボ ボックスの LimitToList プロパティ

Microsoft Access 2002 以降では、リストにNull 値が含まれているかどうかに関して **、LimitToList** プロパティが **True** (–1) に設定されている場合、コンボ ボックスは Null 値を受け入れる。  In version 2.0, a combo box that has the **LimitToList** property set to **True** won't accept a **Null** value unless the list contains a **Null** value. If you want to prevent users from entering a **Null** value by using a combo box, set the **Required** property of the field in the table to **Yes**.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>OLE オブジェクトのメニューとインプレイス アクティブ化

OLE オブジェクトをアクティブ化する際に追加の機能を利用するには、OLE サーバーをアクティブ化するときに、一部のメニュー コマンドがメニューに移動され、置き換えられません。

この変更は、以前のバージョンのアプリケーションのマクロを変換するときには影響しません。以前のバージョンのマクロで、OLE サーバーがアクティブになったときに "DoMenuItem/メニューの実行" アクションを使って Version 2.0 のメニュー コマンドを実行していた場合、アプリケーションを変換すると、Version 2.0 のコマンドは新しいバージョンの Access の同等のコマンドと置き換えられます。

## <a name="referencing-a-control-on-a-read-only-form"></a>読み取り専用フォームでコントロールを参照する

Access 2002 以降では、空のレコード ソースに連結されている読み取り専用フォームのコントロールの値を、式を使って参照することはできません。以前のバージョンでは、このような式は **Null** 値を返しました。読み取り専用フォームのコントロールを参照するときは、フォームのレコード ソースにレコードが含まれているかどうかを確認する必要があります。

## <a name="date-fields-and-data-entry"></a>日付フィールドとデータ入力

If you enter **3/3** in a field of type Date on a form or a table datasheet, the current year is automatically added in Microsoft Access 2002 or later. However, if you enter **3/3/** in the same field, Microsoft Access returns an error message. You must omit the last date delimiter so that Microsoft Access can translate the date into the proper format.

## <a name="buttons-created-with-the-command-button-wizard"></a>コマンド ボタン ウィザードで作成されたボタン

Access Version 2.0 または 7.0 のコマンド ボタン ウィザードを使って、別のアプリケーションを呼び出すコードが記述されたボタンを作成した場合、そのボタンを削除し、Access 2002 以降のコマンド ボタン ウィザードを使って作成し直す必要があります。

## <a name="form-and-report-class-modules"></a>フォーム クラスモジュールとレポート クラス モジュール

In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object. In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**. When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.

## <a name="converted-version-20-report-has-different-margins"></a>変換されたバージョン 2.0 レポートの余白が異なる

Access 2.0 から変換された Access 2002 以降のレポートの印刷またはプレビューを試みたときに、"0" に設定した余白がレポートにあると問題が発生する場合があります。Access 2.0 のレポートを変換する場合、余白が 0 に設定されず、既定のプリンターで有効な最小の余白が設定されます。これは、レポートのデータがプリンターで印刷できない位置に印刷されるのを防ぐためです。

この問題を解決するには、列幅と既定値の余白の幅を加えると用紙の幅と同じかまたはそれに収まる幅になるように、レポートの列幅、列の間隔、または列数を減らします。

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Format プロパティを使用して Null 値と長さ 0 の文字列を区別できない

バージョン 1 の場合。*x* および 2.0 では、コントロールの **Format** プロパティを使用して **、Null** 値と長さ 0 の文字列 (" ") に対して異なる値を表示できます。 In Microsoft Access 2002 or later, to distinguish between **Null** values and zero-length strings in a control on a form, set the control's **ControlSource** property to an expression that tests for the **Null** value case. For example, to display "Null" or "ZLS" in a control, set its **ControlSource** property to the following expression:

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

