---
title: "\"ImportExportData/データのインポート/エクスポート\" マクロ アクション"
TOCTitle: ImportExportData Macro Action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c03811716e776663601fb9c2f9590e644417e3c1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860852"
---
# <a name="importexportdata-macro-action"></a>"ImportExportData/データのインポート/エクスポート" マクロ アクション

**適用されます**Access 2013 |。Office 2013

インポートまたは現在の Access データベース (.mdb または .accdb) または Access プロジェクト (.adp) と他のデータベース間でデータをエクスポートするのには、 **ImportExportData**アクションを使用できます。 Microsoft Access データベースでは、他のデータベースからカレント データベースにテーブルをリンクすることもできます。 テーブルをリンクすると、テーブル自体は他のデータベース内にあっても、そのテーブルのデータにアクセスできます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。

## <a name="settings"></a>設定値

**ImportExportData**アクションには、次の引数があります。

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
<td><p>変換の種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>変換の種類</strong>] ボックスで、[ <strong>インポート</strong>]、[ <strong>エクスポート</strong>]、または [ <strong>リンク</strong>] を選択します。既定値は [ <strong>インポート</strong>] です。  </p>

> [!NOTE]
> [**リンク**] は、Access プロジェクト (.adp) ではサポートされていません。


<p></p></td>
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
<p>新しくリンクしたテーブルをデザイン ビューで開きし、[<strong>デザイン</strong>] タブの [<strong>ツール</strong> <strong>] プロパティ ・ シート</strong>をクリックしてテーブルのプロパティを表示します。 <strong>説明</strong>プロパティの設定値のテキストは、このテーブルの接続文字列です。</p>
<p>ODBC 接続文字列の詳細については、ヘルプ ファイルまたは ODBC ドライバーの ODBC データベースには、この種類の他の資料を参照してください。</p></td>
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


## <a name="remarks"></a>解説

Access のデータベースと他のデータベースの間で、テーブルのインポートやエクスポートを行うことができます。また、Access の選択クエリを他のデータベースにエクスポートすることもできます。クエリの結果セットはテーブルとしてエクスポートされます。Access のデータベース間では、Access のあらゆるデータベース オブジェクトをインポートまたはエクスポートできます。

他の Access のデータベース (.mdb または .accdb) から、そのデータベース内でリンクされているテーブルをインポートした場合は、インポート後もリンクが維持されます。つまり、テーブル自体ではなく、リンクがインポートされます。

アクセスしようとしているデータベースでパスワードが要求される場合は、マクロの実行時に表示されるダイアログ ボックスにパスワードを入力します。

**ImportExportData**アクションは、[**外部データ**] タブの [**インポート**または**エクスポート**のコマンドに似ています。 これらのコマンドを使用すると、Access データベースまたは別の種類のデータベース、スプレッドシート、またはテキスト ファイルなどのデータ ソースを選択します。 データベースを選択する場合は、インポートまたはエクスポート (のデータベースにアクセス) するオブジェクトの種類、オブジェクト、およびデータベースからのインポートまたはエクスポートまたはリンクによって、その他のオプションの名前を選択する 1 つまたは複数のダイアログ ボックスが表示されます。 **ImportExportData**アクションの引数は、これらのダイアログ ボックスでオプションを反映します。

リンクする dBASE テーブルにインデックス情報を指定する場合は、まず、次の手順でテーブルをリンクします。

1.  [ **dBASE ファイル**] をクリックします。

2.  [ **外部データの取り込み**] ダイアログ ボックスで、[ **ファイル名**] ボックスに dBASE ファイルのパスを入力します。

3.  [ **リンク テーブルを作成してソース データにリンクする**] をクリックし、[ **OK**] をクリックします。

4.  このコマンドのダイアログ ボックスでインデックスを指定します。インデックス情報は、Microsoft Office フォルダーにある特別な情報 (.inf) ファイルに保存されます。

5.  この時点で、リンク テーブルへのリンクを削除できます。

この dBASE テーブルをリンクする**ImportExportData**アクションを使用する次の時間は、指定したインデックス情報が使用されます。

> [!NOTE]
> [!メモ] リンクしたテーブルに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。

Visual Basic for Applications (VBA) モジュールに**ImportExportData**アクションを実行するには、 **DoCmd**オブジェクトの**TransferDatabase**メソッドを使用します。

