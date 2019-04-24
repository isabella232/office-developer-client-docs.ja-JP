---
title: ImportExportData マクロ アクション
TOCTitle: ImportExportData macro action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e0cdf85461276d26005bc3066a387031a1086691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291888"
---
# <a name="importexportdata-macro-action"></a>ImportExportData マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="settings"></a>設定

"ImportExportData/データのインポート/エクスポート" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Transfer Type/変換の種類</strong></p></td>
<td><p>変換の種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>変換の種類</strong>] ボックスで、[ <strong>インポート</strong>]、[ <strong>エクスポート</strong>]、または [ <strong>リンク</strong>] を選択します。既定値は [ <strong>インポート</strong>] です。  </p><p><strong>注意</strong>: Access プロジェクト (.adp) では、転送の種類 <strong>[リンク]</strong> はサポートされていません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Database Type/データベースの種類</strong></p></td>
<td><p>インポート元、エクスポート先、またはリンク先のデータベースの種類を指定します。[ <strong>データベースの種類</strong>] ボックスでは、[ <strong>Microsoft Access</strong>] などの多数のデータベースの種類から選択できます。既定値は [ <strong>Microsoft Access</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Database Name/データベース名</strong></p></td>
<td><p>インポート元、エクスポート先、またはリンク先のデータベースの名前を指定します。この引数は省略できません。FoxPro、Paradox、dBASE など、テーブルごとにファイルを作成するデータベースの場合は、ファイルを含むディレクトリを入力します。ファイル名は、" <strong>Source/オブジェクト名</strong> " 引数 (インポートまたはリンクの場合) または " <strong>Destination/変換先名</strong> " 引数 (エクスポートの場合) に入力します。ODBC データベースの場合は、完全な ODBC (Open Database Connectivity) 接続文字列を入力します。  </p>
<p>接続文字列の例を参照するには、次の手順で、外部テーブルを Access にリンクします。</p>
<ol>
<li><p>[ <strong>外部データの取り込み</strong>] ダイアログ ボックスで、[ <strong>ファイル名</strong>] ボックスにソース データベースのパスを入力します。</p></li>
<li><p>[ <strong>リンク テーブルを作成してソース データにリンクする</strong>] をクリックし、[ <strong>OK</strong>] をクリックします。</p></li>
<li><p>[ <strong>テーブルのリンク</strong>] ダイアログ ボックスでテーブルを選択し、[ <strong>OK</strong>] をクリックします。</p></li>
</ol>
<p>Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.  </p>
<p>odbc 接続文字列の詳細については、この odbc データベースの odbc ドライバーのヘルプファイルまたはその他のドキュメントを参照してください。</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>インポートまたはエクスポートするオブジェクトの種類を指定します。" <strong>Database Type/データベースの種類</strong> " 引数に [ <strong>Microsoft Access</strong>] を指定した場合は、[ <strong>オブジェクトの種類</strong>] ボックスで、[ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、または [ <strong>関数</strong>] を選択できます。既定値は [ <strong>テーブル</strong>] です。その他の種類のデータベースを選択した場合、または [ <strong>変換の種類</strong>] ボックスで [ <strong>リンク</strong>] を選択した場合、この引数は無視されます。選択クエリを Access データベースにエクスポートする場合、クエリの結果セットをエクスポートするには [ <strong>テーブル</strong>] を選択し、クエリ自体をエクスポートするには [ <strong>クエリ</strong>] を選択します。選択クエリを別の種類のデータベースにエクスポートする場合は、この引数が無視され、クエリの結果セットがエクスポートされます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Source/オブジェクト名</strong></p></td>
<td><p>インポート、エクスポート、またはリンクの対象となるテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Destination/変換先名</strong></p></td>
<td><p>変換先データベースにインポート、エクスポート、またはリンクした後のテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。 この引数は省略できません。 " <strong>Transfer Type (変換の種類)</strong> " 引数で [ <strong>インポート</strong>] を選択し、" <strong>Object Type (オブジェクトの種類)</strong> " 引数で <strong>テーブル</strong> を選択した場合、テーブルが新規作成され、指定したテーブルのデータがインポートされます。 テーブルまたはその他のオブジェクトをインポートしたときに既存の名前と競合する場合は、その名前に番号が追加されます。たとえば、"社員" テーブルをインポートしたときに "社員" という名前のテーブルが既に存在する場合、インポートしたテーブルの名前は "社員 1" に変更されます。 Access データベースまたはその他のデータベースにエクスポートした場合は、同じ名前の既存のテーブルあるいはその他のオブジェクトは自動的に置き換わります。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Structure Only/テーブル構造のみ変換</strong></p></td>
<td><p>データベース テーブルの構造のみ (データを除く) をインポートまたはエクスポートするかどうかを指定します。[ <strong>はい</strong>] または [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>いいえ</strong>] です。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Access のデータベースと他のデータベースの間で、テーブルのインポートやエクスポートを行うことができます。また、Access の選択クエリを他のデータベースにエクスポートすることもできます。クエリの結果セットはテーブルとしてエクスポートされます。Access のデータベース間では、Access のあらゆるデータベース オブジェクトをインポートまたはエクスポートできます。

他の Access のデータベース (.mdb または .accdb) から、そのデータベース内でリンクされているテーブルをインポートした場合は、インポート後もリンクが維持されます。つまり、テーブル自体ではなく、リンクがインポートされます。

アクセスしようとしているデータベースでパスワードが要求される場合は、マクロの実行時に表示されるダイアログ ボックスにパスワードを入力します。

The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.

リンクする dBASE テーブルにインデックス情報を指定する場合は、まず、次の手順でテーブルをリンクします。

1.  [ **dBASE ファイル**] をクリックします。

2.  [ **外部データの取り込み**] ダイアログ ボックスで、[ **ファイル名**] ボックスに dBASE ファイルのパスを入力します。

3.  [ **リンク テーブルを作成してソース データにリンクする**] をクリックし、[ **OK**] をクリックします。

4.  このコマンドのダイアログ ボックスでインデックスを指定します。インデックス情報は、Microsoft Office フォルダーにある特別な情報 (.inf) ファイルに保存されます。

5.  この時点で、リンク テーブルへのリンクを削除できます。

The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.

> [!NOTE]
> [!メモ] リンクしたテーブルに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。

To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.

