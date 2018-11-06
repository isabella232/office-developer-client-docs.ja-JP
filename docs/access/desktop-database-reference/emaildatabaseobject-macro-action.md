---
title: EMailDatabaseObject マクロ アクション
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 84d5b9c5f65e032523be8c646cdea18890744367
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997449"
---
# <a name="emaildatabaseobject-macro-action"></a>EMailDatabaseObject マクロ アクション

**に適用されます:** Access 2013 |Office 2013

**EMailDatabaseObject**アクションを使用すると、指定した Access データシート、フォーム、レポート、モジュール、またはデータ アクセス ページは、メール メッセージを表示および転送できます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="settings"></a>設定値

**EMailDatabaseObject**アクションには、次の引数があります。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>メール メッセージに添付するオブジェクトの型。 <strong>テーブル</strong>(テーブル: データシートの場合)、<strong>クエリ</strong>(クエリ データシートの場合)、(フォームまたはフォームのデータシートの場合) の<strong>フォーム</strong>、<strong>レポート</strong>、<strong>モジュール</strong>、または<strong>データ アクセス ページ</strong>、<strong>サーバー ビュー</strong>、<strong>ストアド プロシージャ</strong>、または<strong>をクリックします。関数</strong>、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの<strong>オブジェクトの種類</strong>ボックスにします。 マクロを送信することはできません。 アクティブ オブジェクトを添付する場合は、この引数でオブジェクトの種類を選択が、<strong>オブジェクト名</strong>の引数を空白のままにします。</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>メール メッセージに添付するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数と " <strong>Object Name/オブジェクト名</strong> " 引数を両方とも指定しない場合は、データベース オブジェクトが添付されていないメッセージがメール アプリケーションに送信されます。 ライブラリ データベースで " <strong>EMailDatabaseObject/ データベースオブジェクトの電子メール送信</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Output Format/出力ファイル形式</strong></p></td>
<td><p>含まれているオブジェクトを使用形式の種類。 選択できる形式の一覧は、<strong>オブジェクトの型</strong>引数で選択した種類に応じて変更されます。 使用可能な形式は、 <strong>Excel 97 - 2003年ブック (*.xls)</strong>、 <strong>Excel バイナリ ブック (*.xlsb)</strong>、 <strong>Excel ブック (*.xlsx)</strong>を含めることが<strong>HTML (*.htm、* .html)</strong>、 <strong>Microsoft Excel 5.0/95 ブック (*.xls)</strong>、PDF 形式の<strong></strong>、<strong>リッチ テキスト書式 (の式 *.rtf)</strong>、<strong>テキスト ファイル (*.txt)</strong>、または<strong>XPS 形式 (*.xps)</strong>。 <strong>出力形式</strong>] ボックスにします。 モジュールはテキスト形式でのみ送信できます。 データ アクセス ページは HTML 形式でのみ送信されます。 この引数を指定しないと、出力形式を確認するダイアログ ボックスが表示されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>To/宛先</strong></p></td>
<td><p>メール メッセージの [ <strong>宛先</strong>] 行に含める、メッセージの受信者名を指定します。この引数を指定しないと、受信者名を確認するダイアログ ボックスが表示されます。 この引数、" <strong>Cc/CC</strong>" 引数、および " <strong>Bcc/BCC</strong>" 引数で複数の受信者の名前を指定する場合は、セミコロン (;)、または Microsoft Windows <strong>コントロール パネル</strong>の [ <strong>地域のオプションのカスタマイズ</strong>] ダイアログ ボックスの [ <strong>数値</strong>] タブで設定した区切り記号で区切ります。メール アプリケーションで受信者名を識別できない場合は、メッセージが送信されずにエラーが発生します。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc/CC</strong></p></td>
<td><p>受信者名を<strong>[cc]</strong>に追加する (&quot;カーボン コピー&quot;)、メール メッセージ内の行です。 この引数を指定しない場合、メール メッセージの [ <strong>CC</strong>] 行が空白になります。</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc/BCC</strong></p></td>
<td><p>メッセージの受信者に<strong>Bcc</strong>を追加する名前 (&quot;ブラインド カーボン コピー&quot;)、メール メッセージ内の行です。 この引数を指定しない場合、メール メッセージの [ <strong>BCC</strong>] 行が空白になります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Subject/件名</strong></p></td>
<td><p>メッセージの件名を指定します。このテキストはメール メッセージの [ <strong>件名</strong>] 行に表示されます。この引数を指定しない場合、メール メッセージの [ <strong>件名</strong>] 行が空白になります。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Message Text/メッセージ</strong></p></td>
<td><p>データベース オブジェクトと共にメール メッセージに含めるテキストです。 オブジェクトの後に、メール メッセージの本文にこのテキストが表示されます。 この引数を空白のままにする場合追加のテキストが含まれていないメール メッセージにします。 <strong>オブジェクト型</strong>および<strong>オブジェクト名</strong>の引数を空白のままにする場合は、データベース オブジェクトにメッセージを送信するのにはこの引数を使用できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Edit Message/メッセージの編集</strong></p></td>
<td><p>メッセージを送信する前に編集できるかどうかを指定します。[ <strong>はい</strong>] を選択すると、電子メール アプリケーションが自動的に起動し、メッセージを編集できるようになります。[ <strong>いいえ</strong>] を選択すると、送信前にメッセージを編集できなくなります。既定値は [ <strong>はい</strong>] です。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Template File/テンプレート ファイル</strong></p></td>
<td><p>HTML ファイルのテンプレートとして使用するファイルのパスとファイル名を指定します。テンプレート ファイルとは、HTML タグを含むファイルです。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

メール メッセージのオブジェクトは、指定した出力形式で出力されます。オブジェクトをダブルクリックすると、対応するソフトウェアが起動し、オブジェクトが開きます。

**EMailDatabaseObject**アクションを使用するデータベース オブジェクトをメール メッセージに挿入するときは、次の規則が適用されます。

- テーブル、クエリ、およびフォームの各データシートを送信できます。添付されるオブジェクトには、OLE オブジェクトを含むフィールドを除くデータシートのすべてのフィールドが出力されます。OLE オブジェクトを含むフィールドの列もオブジェクトに出力されますが、フィールド値は空白になります。

- Yes/No 型フィールド (トグル ボタン、オプション ボタン、チェック ボックス) に連結されたコントロールの場合、出力ファイルには \uc1\u8211 ?1 (Yes) または 0 (No) の値が表示されます。

- ハイパーリンク型 (Hyperlink) フィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが出力されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして出力されます)。

- フォーム ビューのフォームを送信する場合、添付されるオブジェクトには常にフォームのデータシート ビューが含まれます。

- レポートを送信する場合のみ、オブジェクトに含まれるコントロールはテキスト ボックスといくつかの場合) のラベルです。 他のすべてのコントロールは無視されます。 ヘッダーとフッターの情報も含まれていません。 唯一の例外は、Excel 形式でレポートを送信するときに、 **Sum**関数を使った式が含まれているグループ フッターのテキスト ボックスがオブジェクトに含まれています。 オブジェクトでは、ヘッダー、フッターおよび関数**Sum**以外の集計関数) には、他のコントロールが含まれていません。

- サブレポートはオブジェクトに取り込まれます。

- HTML 形式のデータシート、フォーム、またはデータ アクセス ページを送信する場合は, .html ファイルが 1 つ作成されます。HTML 形式のレポートを送信する場合は, .html ファイルがレポートのページごとに 1 つずつ作成されます。

Visual Basic for Applications (VBA) モジュールに**EMailDatabaseObject**アクションを実行するには、 **DoCmd**オブジェクトの**SendObject**メソッドを使用します。

### <a name="about-the-contributor"></a>共同作成者について

**によってリンクが提供されます。** Luke Chung [FMS, Inc.](https://www.fmsinc.com/)、創設者で、FMS, Inc. は、カスタム データベース ソリューションと開発ツールのリーディング ・ プロバイダーの社長です。

- [送信用の SendObject メソッドの使用に関する機能と制限](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





