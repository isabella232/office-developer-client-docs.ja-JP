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
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293568"
---
# <a name="emaildatabaseobject-macro-action"></a>EMailDatabaseObject マクロ アクション

**適用対象:** Access 2013 |Office 2013

You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="settings"></a>設定

"EMailDatabaseObject/データベースオブジェクトの電子メール送信" アクションの引数は次のとおりです。

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
<td><p>The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>メール メッセージに添付するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数と " <strong>Object Name/オブジェクト名</strong> " 引数を両方とも指定しない場合は、データベース オブジェクトが添付されていないメッセージがメール アプリケーションに送信されます。 ライブラリ データベースで " <strong>EMailDatabaseObject/ データベースオブジェクトの電子メール送信</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Output Format/出力ファイル形式</strong></p></td>
<td><p>The type of format you want used for the included object. The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument. 使用可能な形式には、excel <strong>97-excel 2003 ブック (* .xls</strong>)、 <strong>excel バイナリブック (* .xlsb)</strong>、 <strong>excel ブック (* .xlsx)</strong>、 <strong>HTML (* .htm、* .html)</strong>、 <strong>Microsoft Excel 5.0/95 ブック (* .xls</strong>)、 <strong>PDF 形式</strong>、<strong>リッチテキスト fomat (* .rtf)</strong>、<strong>テキストファイル (* .txt</strong>)、 <strong>xps 形式 (* .xps)</strong>。 in the <strong>Output Format</strong> box. Modules can be sent only in text format. Data access pages can only be sent in HTML format. If you leave this argument blank, Access prompts you for the output format.</p></td>
</tr>
<tr class="even">
<td><p><strong>To/宛先</strong></p></td>
<td><p>メール メッセージの [ <strong>宛先</strong>] 行に含める、メッセージの受信者名を指定します。この引数を指定しないと、受信者名を確認するダイアログ ボックスが表示されます。 この引数、" <strong>Cc/CC</strong>" 引数、および " <strong>Bcc/BCC</strong>" 引数で複数の受信者の名前を指定する場合は、セミコロン (;)、または Microsoft Windows <strong>コントロール パネル</strong>の [ <strong>地域のオプションのカスタマイズ</strong>] ダイアログ ボックスの [ <strong>数値</strong>] タブで設定した区切り記号で区切ります。メール アプリケーションで受信者名を識別できない場合は、メッセージが送信されずにエラーが発生します。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Cc/CC</strong></p></td>
<td><p>メールメッセージの [ <strong>Cc</strong> ] (&quot;カーボンコピー&quot;) 行に登録するメッセージの受信者名を入力します。 この引数を指定しない場合、メール メッセージの [ <strong>CC</strong>] 行が空白になります。</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc</strong></p></td>
<td><p>メールメッセージの<strong>Bcc</strong> (&quot;ブラインドカーボンコピー&quot;) 行に配置するメッセージの受信者名を指定します。 この引数を指定しない場合、メール メッセージの [ <strong>BCC</strong>] 行が空白になります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Subject/件名</strong></p></td>
<td><p>メッセージの件名を指定します。このテキストはメール メッセージの [ <strong>件名</strong>] 行に表示されます。この引数を指定しない場合、メール メッセージの [ <strong>件名</strong>] 行が空白になります。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Message Text/メッセージ</strong></p></td>
<td><p>Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.  </p></td>
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


## <a name="remarks"></a>注釈

メール メッセージのオブジェクトは、指定した出力形式で出力されます。オブジェクトをダブルクリックすると、対応するソフトウェアが起動し、オブジェクトが開きます。

The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:

- テーブル、クエリ、およびフォームの各データシートを送信できます。添付されるオブジェクトには、OLE オブジェクトを含むフィールドを除くデータシートのすべてのフィールドが出力されます。OLE オブジェクトを含むフィールドの列もオブジェクトに出力されますが、フィールド値は空白になります。

- yes/No 型フィールド (トグルボタン、オプションボタン、チェックボックス) に連結されたコントロールの場合、出力ファイルには-1 (Yes) または 0 (No) の値が表示されます。

- ハイパーリンク型 (Hyperlink) フィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが出力されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして出力されます)。

- フォーム ビューのフォームを送信する場合、添付されるオブジェクトには常にフォームのデータシート ビューが含まれます。

- If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.

- サブレポートはオブジェクトに取り込まれます。

- HTML 形式のデータシート、フォーム、またはデータ アクセス ページを送信する場合は, .html ファイルが 1 つ作成されます。HTML 形式のレポートを送信する場合は, .html ファイルがレポートのページごとに 1 つずつ作成されます。

To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.

### <a name="about-the-contributor"></a>共同作成者について

**リンクの提供**元Luke Chung、 [fms、inc.](https://www.fmsinc.com/)、FMS、inc. の創設者および社長。これは、カスタムデータベースソリューションおよび開発者ツールのリーディングプロバイダーです。

- [送信用の SendObject メソッドの使用に関する機能と制限](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





