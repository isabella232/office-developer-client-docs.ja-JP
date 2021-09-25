---
title: ExportWithFormatting マクロ アクション
TOCTitle: ExportWithFormatting macro action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 41c2be7b412bf043f392fb5d26ba5eb2cbc9971c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606780"
---
# <a name="exportwithformatting-macro-action"></a>ExportWithFormatting マクロ アクション


**適用先**: Access 2013、Office 2013


            **ExportWithFormatting** アクションを使用すると、指定した Microsoft Access データベース オブジェクト (データシート、フォーム、レポート、モジュール、またはデータ アクセス ページ) のデータを複数の出力形式で出力できます。

## <a name="settings"></a>設定値


            **ExportWithFormatting** アクションの引数は次のとおりです。

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
<td><p><strong>オブジェクトの種類</strong></p></td>
<td><p>出力するデータが格納されているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>] (テーブルのデータシートの場合)、[<strong>クエリ</strong>] (クエリのデータシートの場合)、[<strong>フォーム</strong>] (フォームまたはフォームのデータシートの場合)、[<strong>レポート</strong>]、[<strong>モジュール</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ストアド プロシージャ</strong>]、または [<strong>関数</strong>] をクリックします。マクロは出力できません。アクティブ オブジェクトを出力する場合は、この引数でオブジェクトの種類を選択し、<strong>Object Name/オブジェクト名</strong>引数は指定しません。この引数は省略できません。既定値は [<strong>テーブル</strong>] です。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクト名</strong></p></td>
<td><p>出力するデータが格納されているオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。ライブラリ データベースで <strong>ExportWithFormatting</strong> アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Output Format/出力ファイル形式</strong></p></td>
<td><p>データの出力に使用するファイル形式を指定します。[<strong>Excel 97-2003 ブック (*.xls)</strong>]、[<strong>Excel バイナリ ブック (*.xlsb)</strong>]、[<strong>Excel ブック (*.xlsx)</strong>]、[<strong>HTML (*.htm, *.html)</strong>]、[<strong>Microsoft Excel 5.0/95 ブック (*.xls)</strong>]、[<strong>PDF 形式 (*.pdf)</strong>]、[<strong>リッチ テキスト形式 (*.rtf)</strong>]、[<strong>テキスト ファイル (*.txt)</strong>]、または [<strong>XPS 形式 (*.xps)</strong>] を選択できます。この引数を指定しないと、出力形式を確認するダイアログ ボックスが表示されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Output File/出力ファイル</strong></p></td>
<td><p>データの出力先となるファイル (完全なパスを含めます)。 <strong>出力ファイル形式</strong>の引数で選んだ出力ファイル形式の標準のファイル名拡張子を含めることができますが、この拡張子は省略できます。 <strong>出力ファイル</strong>の引数を指定しない場合は、出力ファイル名を確認するダイアログ ボックスが表示されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>自動起動</strong></p></td>
<td><p>
            <strong>ExportWithFormatting</strong> アクションを実行した直後に適切なソフトウェアを起動して、<strong>Output File/出力ファイル</strong>引数で指定したファイルを開くかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Template File/テンプレート ファイル</strong></p></td>
<td><p>HTML ファイルのテンプレートとして使用するファイルのパスとファイル名を指定します。テンプレート ファイルとは、Access に固有の HTML タグおよびトークンを含むテキスト ファイルです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Encoding/エンコード</strong></p></td>
<td><p>テキストまたは HTML データを出力する際に使用する文字エンコード形式の種類を指定します。[<strong>MS-DOS</strong>]、[<strong>Unicode</strong>]、または [<strong>Unicode (UTF-8)</strong>] を選択できます。引数の設定値 [<strong>MS-DOS</strong>] は、テキスト ファイルの場合にのみ選択できます。この引数を指定しない場合、テキスト ファイルに対しては Windows の既定のエンコード方法を使用し、HTML ファイルに対してはシステムの既定のエンコード方法を使用して、データが出力されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Output Quality/出力品質</strong></p></td>
<td><p>印刷の出力を最適化する場合は [<strong>印刷</strong>]、画面上に表示する出力を最適化する場合は [<strong>スクリーン</strong>] を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

Access のデータは形式を指定して出力すると、同じ形式を使用するプログラムでそのまま読み取ることができます。たとえば、Access のレポートをリッチ テキスト形式の文書に出力すると、その文書を Microsoft Word で開くことができます。

データベース オブジェクトを HTML 形式で出力すると、そのオブジェクトのデータを含む HTML 形式のファイルが作成されます。**Template File/テンプレート ファイル** 引数を使用すると、.html ファイルのテンプレートとして使用するファイルを指定できます。


            **ExportWithFormatting** アクションを使用してデータベース オブジェクトをいずれかの出力形式で出力する場合は、次の規則が適用されます。

  - テーブル、クエリ、およびフォームの各データシートのデータを出力できます。出力ファイルには、OLE オブジェクトが含まれているフィールドを除き、データシートのすべてのフィールドがそのまま出力されます。OLE オブジェクトが含まれているフィールドの列もファイルに出力されますが、そのフィールド値は空白になります。

  - Yes/No 型フィールド (トグル ボタン、オプション ボタン、またはチェック ボックス) に連結されたコントロールの場合、出力ファイルには –1 (Yes) または 0 (No) の値が表示されます。

  - ハイパーリンク型のフィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが表示されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして表示されます)。

  - フォーム ビューに表示されたフォームのデータを出力する場合、出力ファイルには常にフォームのデータシート ビューが含まれます。

  - データシート、フォーム、またはデータ アクセス ページを HTML 形式で出力する場合は、.html ファイルが 1 つ作成されます。レポートを HTML 形式で出力する場合は、レポートのページごとに .html ファイルが 1 つずつ作成されます。


            **ExportWithFormatting** アクションの実行結果は、[**外部データ**] タブの [**エクスポート**] にあるオプションのいずれかをクリックしたときと似ています。このアクションの引数は [**エクスポート**] ダイアログ ボックスの設定に対応しています。

Visual Basic for Applications (VBA) モジュールで **ExportWithFormatting** アクションを実行するには、**DoCmd** オブジェクトの **OutputTo** メソッドを使用します。

