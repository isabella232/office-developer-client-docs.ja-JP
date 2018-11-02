---
title: ImportExportSpreadsheet マクロ アクション
TOCTitle: ImportExportSpreadsheet macro action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d630602d7b81fe44427d892d62275f4509dbdc2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923974"
---
# <a name="importexportspreadsheet-macro-action"></a>ImportExportSpreadsheet マクロ アクション


**適用されます**Access 2013、Office 2013。

**ImportExportSpreadsheet** アクションを使用すると、カレントの Access データベース (.mdb または .accdb) または Access プロジェクト (.adp) とワークシート ファイルとの間でデータをインポートまたはエクスポートできます。Microsoft Excel のワークシートのデータを Microsoft Access のカレント データベースにリンクすることもできます。ワークシートをリンクすると、Access でワークシート データを表示したり編集することができると同時に、Excel のワークシート プログラムからそのデータにアクセスできます。Lotus 1-2-3 のワークシート ファイルのデータにもリンクできますが、そのファイルは Access では読み取り専用になります。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定

**TransferSpreadsheet** アクションの引数は次のとおりです。

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
> <P>[<STRONG>リンク</STRONG>] は、Access プロジェクト (.adp) ではサポートされていません。</P>


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Spreadsheet Type/ワークシートの種類</strong></p></td>
<td><p>インポート元、エクスポート先、またはリンク先のワークシートの種類を指定します。このボックスでは、多数のワークシートの種類から 1 つを選択できます。既定値は [ <strong>Excel ブック</strong>] です。  </p>

> [!NOTE]
> <P>インポート元およびリンク (読み取り専用) 先として Lotus .WK4 ファイルを指定できますが、Access のデータをこのワークシート形式にエクスポートすることはできません。Access では、このアクションによる Lotus .WKS または Excel Version 2.0 のワークシートのデータのインポート、エクスポート、またはリンクはサポートされなくなりました。Excel Version 2.0 形式または Lotus .WKS 形式のワークシート データをインポートまたはリンクする場合は、ワークシート データを Excel または Lotus 1-2-3 の新しいバージョンに変換してから、Access にデータをインポートまたはリンクします。</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>Table Name/テーブル名</strong></p></td>
<td><p>ワークシート データのインポート先、エクスポート元、またはリンク先となる Access のテーブル名を指定します。また、データのエクスポート元として Access の選択クエリ名を入力することもできます。この引数は省略できません。 <strong>Transfer Type/変換の種類</strong> 引数で [ <strong>インポート</strong>] を選択すると、テーブルが既に存在する場合は、ワークシートのデータがこのテーブルに追加されます。テーブルが存在しない場合は、新しいテーブルが作成され、指定したワークシートのデータがインポートされます。Access では、 <strong>ImportExportSpreadsheet</strong> アクションを使用するときに、エクスポートするデータを SQL ステートメントを使って指定することができません。SQL ステートメントを使うのではなく、クエリを作成してから、 <strong>Table Name/テーブル名</strong> 引数にそのクエリの名前を指定する必要があります。  </p></td>
</tr>
<tr class="even">
<td><p><strong>ファイル名</strong></p></td>
<td><p>インポート元、エクスポート先、またはリンク先のワークシート ファイルの名前を指定します。ファイル名が既存のワークシートの名前と同じ場合、既存のワークシートが置き換えられます。この引数は省略できません。Access のデータをエクスポートすると、新しいワークシートが作成されます。ファイル名が既存のワークシートの名前と同じ場合、既存のワークシートが置き換えられます。ただし、Excel 5.0 以降のバージョンのブックをエクスポートする場合は、エクスポートされたデータがブック内の次に使用できる新しいワークシートにコピーされます。Excel 5.0 以降のバージョンのワークシートのデータをインポートまたはリンクする場合、 <strong>Range/範囲</strong> 引数を使用して特定のワークシートを指定できます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Has Field Names/フィールド名の設定</strong></p></td>
<td><p>ワークシートの先頭行にフィールド名を含めるかどうかを指定します。[ <strong>はい</strong>] を選択した場合は、ワークシートのデータをインポートまたはリンクするときに、先頭行の名前が Access のテーブルのフィールド名として使用されます。[ <strong>いいえ</strong>] を選択した場合は、先頭行が通常のデータ行として処理されます。既定値は [ <strong>いいえ</strong>] です。Access のテーブルや選択クエリをワークシートにエクスポートした場合は、この引数の値に関係なく、ワークシートの先頭行にフィールド名が挿入されます。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Range/範囲</strong></p></td>
<td><p>インポートまたはリンクするセルの範囲を指定します。この引数を指定しないと、ワークシート全体がインポートまたはリンクされます。インポートまたはリンクするワークシートの範囲名を入力するか、A1:E25 のようにセル範囲を指定することができます。Access 97 以降のバージョンでは、A1..E25 の構文は使用できないことに注意してください。Excel 5.0 以降のバージョンのワークシートのデータをインポートまたはリンクする場合は、範囲の前にワークシート名と感嘆符を付けることができます (たとえば、<ワークシート名>!A1:C7)。 



</p>

> [!NOTE]
> <P>ワークシートにエクスポートする際は、この引数を空白のままにしておきます。範囲を入力すると、エクスポートは失敗します。</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

Access の選択クエリのデータをワークシートにエクスポートできます。クエリの結果セットもテーブルと同じようにエクスポートされます。

既存の Access のテーブルに追加するワークシートのデータは、テーブルの構造との互換性が必要です。

  - ワークシートの各フィールドのデータ型は、テーブルの対応するフィールドのデータ型と同じにする必要があります。

  - フィールドは同じ順序にする必要があります (ただし、 **Has Field Names/フィールド名の設定** 引数を [ **はい**] に設定した場合は、ワークシートのフィールド名とテーブルのフィールド名を同じにする必要があります)。

このアクションの動作は、[ **外部データ**] タブをクリックし、[ **インポート**] または [ **エクスポート**] で [ **Excel**] をクリックした場合や、[ **インポート**] または [ **エクスポート**] で [ **その他**] をクリックして、[ **Lotus 1-2-3 ファイル**] をクリックした場合と同じです。これらのコマンドを使用して、Access やその他のデータベース、ワークシート、またはテキスト ファイルなどの変換元のデータを選択できます。ワークシートを選択した場合は、ワークシートの名前やその他のオプションを選択する一連のダイアログ ボックス (Access のウィザード) が実行されます)。 **ImportExportSpreadsheet** アクションの引数は、このようなダイアログ ボックスやウィザードのオプションに対応しています。


> [!NOTE]
> <P>[!メモ] リンクしたワークシートに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。</P>



編集モードで開いている Excel ワークシートにリンクする場合は、Excel ワークシートの編集モードが終了するまで待機してから、リンクします。タイムアウトが発生することはありません。

Visual Basic for Applications (VBA) モジュールで **ImportExportSpreadsheet** アクションを実行するには、 **DoCmd** オブジェクトの **TransferSpreadsheet** メソッドを使用します。

