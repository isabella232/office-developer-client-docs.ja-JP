---
title: Microsoft Access のテーブル、フォーム、レポートの変換
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Microsoft Access 2002 で導入された変更のバージョンの動作に影響する可能性があります 1.x または 2.0 のアプリケーションです。
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 69bd93b84bb0bca768203933e64e385648d52730
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891073"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Microsoft Access のテーブル、フォーム、レポートの変換

**適用されます**Access 2013、Office 2013。

Microsoft Access 2002 で導入されたいくつかの変更、バージョン 1 の動作に影響を与える可能性があります。*x*または 2.0 のアプリケーションです。 次のセクションでは、これらの変更の詳細についてを説明します。

## <a name="indexes-and-relationships"></a>インデックスとリレーションシップ

Microsoft Access テーブルに含めることができるインデックスは最大 32 個です。リレーションシップの "多" 側の複雑なテーブルでは、インデックスの制限値を超える可能性があり、このようなテーブルを含むデータベースは、変換することができません。Microsoft Access データベース エンジンはリレーションシップの両側のテーブルにインデックスを作成します。データベースを変換できない場合は、いくつかのリレーションシップを削除してからデータベースを変換し直してください。

## <a name="the-limittolist-property-of-combo-boxes"></a>コンボ ボックスの LimitToList プロパティ

**Microsoft Access 2002 以降では、コンボ ボックス Null**値を受け入れるに**True** (-1)、**このプロパティ**が設定されている場合、リストに**Null**値が含まれているかどうか。 バージョン 2.0 では、**プロパティを**True**に設定**を持つコンボ ボックスを受け付けません**Null**値リストには、 **Null**値が含まれている場合を除き、します。 コンボ ボックスを使用して**Null**値を入力できないようにする場合は、 **[はい]** に、テーブルのフィールドの**ために必要な**プロパティを設定します。

## <a name="menus-and-in-place-activation-of-ole-objects"></a>メニューおよび OLE オブジェクトのインプレース アクティブ化

追加機能が使用できるようにする保存されている OLE オブジェクトをアクティブ化中に、一部のメニュー コマンドを OLE サーバーをアクティブ化するときにも置き換えられないメニューに移動が場合があります。

この変更は、以前のバージョンのアプリケーションのマクロを変換するときには影響しません。以前のバージョンのマクロで、OLE サーバーがアクティブになったときに "DoMenuItem/メニューの実行" アクションを使って Version 2.0 のメニュー コマンドを実行していた場合、アプリケーションを変換すると、Version 2.0 のコマンドは新しいバージョンの Access の同等のコマンドと置き換えられます。

## <a name="referencing-a-control-on-a-read-only-form"></a>読み取り専用フォーム上のコントロールを参照します。

Access 2002 以降では、空のレコード ソースに連結されている読み取り専用フォームのコントロールの値を、式を使って参照することはできません。以前のバージョンでは、このような式は **Null** 値を返しました。読み取り専用フォームのコントロールを参照するときは、フォームのレコード ソースにレコードが含まれているかどうかを確認する必要があります。

## <a name="date-fields-and-data-entry"></a>日付フィールドおよびデータの入力

フォームまたはテーブルのデータシートで、日付型のフィールドに**3/3**を入力すると Access 2002 以降で現在の年は自動的に追加します。 ただし、入力する場合は**3/3/** 同じフィールドに、Microsoft Access がエラー メッセージを返します。 Microsoft Access は適切な形式に、日付を変換できるように、最後の日付の区切り記号を省略する必要があります。

## <a name="buttons-created-with-the-command-button-wizard"></a>コマンド ボタン ウィザードで作成したボタン

Access Version 2.0 または 7.0 のコマンド ボタン ウィザードを使って、別のアプリケーションを呼び出すコードが記述されたボタンを作成した場合、そのボタンを削除し、Access 2002 以降のコマンド ボタン ウィザードを使って作成し直す必要があります。

## <a name="form-and-report-class-modules"></a>フォームやレポートのクラス モジュール

以前のバージョンの Microsoft Access 2002 での**フォーム**および**レポート**のオブジェクトが関連付けられているクラス モジュールのオブジェクトの背後のコードがない場合でも。 Microsoft Access 2002 以降では、 **false を指定**する**フォームやレポートのプロパティ**を設定できます。 **HasModule**プロパティを**False**に設定するときに必要なディスク領域が少なく、フォームまたはレポートと読み込みが速くなります、関連付けられたクラス モジュールがある不要になったため。

## <a name="converted-version-20-report-has-different-margins"></a>変換されたバージョン 2.0 のレポートに別の余白があります。

Access 2.0 から変換された Access 2002 以降のレポートの印刷またはプレビューを試みたときに、"0" に設定した余白がレポートにあると問題が発生する場合があります。Access 2.0 のレポートを変換する場合、余白が 0 に設定されず、既定のプリンターで有効な最小の余白が設定されます。これは、レポートのデータがプリンターで印刷できない位置に印刷されるのを防ぐためです。

この問題を解決するには、列幅と既定値の余白の幅を加えると用紙の幅と同じかまたはそれに収まる幅になるように、レポートの列幅、列の間隔、または列数を減らします。

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Null 値と長さ 0 の文字列を区別するために、[書式] プロパティを使用することはできません。

バージョン 1 です。**Null**値と長さ 0 の文字列に異なる値を表示するコントロールの**書式**プロパティを使用するには*x*と 2.0 では、("")。 Microsoft Access 2002 以降では、 **Null**値と長さ 0 の文字列では、フォーム上のコントロールを区別するに、 **Null**値である場合をテストする式をコントロールの**ControlSource**プロパティを設定します。 などのコントロールに"Null"または"ZLS"を表示するのには次のように、[**コントロール ソース**] プロパティを設定します。

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

