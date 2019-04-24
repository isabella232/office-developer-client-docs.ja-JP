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
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="5470f-102">EMailDatabaseObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5470f-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="5470f-103">**適用対象:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="5470f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="5470f-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span><span class="sxs-lookup"><span data-stu-id="5470f-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="5470f-105">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="5470f-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="5470f-106">設定</span><span class="sxs-lookup"><span data-stu-id="5470f-106">Settings</span></span>

<span data-ttu-id="5470f-107">"EMailDatabaseObject/データベースオブジェクトの電子メール送信" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5470f-107">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5470f-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="5470f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5470f-109">説明</span><span class="sxs-lookup"><span data-stu-id="5470f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5470f-110"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p101">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.  </span><span class="sxs-lookup"><span data-stu-id="5470f-p101">The type of object to include in the mail message. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't send a macro. If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5470f-115"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p102">メール メッセージに添付するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数と " <strong>Object Name/オブジェクト名</strong> " 引数を両方とも指定しない場合は、データベース オブジェクトが添付されていないメッセージがメール アプリケーションに送信されます。 ライブラリ データベースで " <strong>EMailDatabaseObject/ データベースオブジェクトの電子メール送信</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="5470f-p102">The name of the object to include in the mail message. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object. If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5470f-120"><strong>Output Format/出力ファイル形式</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-121">The type of format you want used for the included object.</span><span class="sxs-lookup"><span data-stu-id="5470f-121">The type of format you want used for the included object.</span></span> <span data-ttu-id="5470f-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span><span class="sxs-lookup"><span data-stu-id="5470f-122">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="5470f-123">使用可能な形式には、excel <strong>97-excel 2003 ブック (\* .xls</strong>)、 <strong>excel バイナリブック (\* .xlsb)</strong>、 <strong>excel ブック (\* .xlsx)</strong>、 <strong>HTML (\* .htm、\* .html)</strong>、 <strong>Microsoft Excel 5.0/95 ブック (\* .xls</strong>)、 <strong>PDF 形式</strong>、<strong>リッチテキスト fomat (\* .rtf)</strong>、<strong>テキストファイル (\* .txt</strong>)、 <strong>xps 形式 (\* .xps)</strong>。</span><span class="sxs-lookup"><span data-stu-id="5470f-123">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="5470f-124">in the <strong>Output Format</strong> box.</span><span class="sxs-lookup"><span data-stu-id="5470f-124">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="5470f-125">Modules can be sent only in text format.</span><span class="sxs-lookup"><span data-stu-id="5470f-125">Modules can be sent only in text format.</span></span> <span data-ttu-id="5470f-126">Data access pages can only be sent in HTML format.</span><span class="sxs-lookup"><span data-stu-id="5470f-126">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="5470f-127">If you leave this argument blank, Access prompts you for the output format.</span><span class="sxs-lookup"><span data-stu-id="5470f-127">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5470f-128"><strong>To/宛先</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-128"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p104">メール メッセージの [ <strong>宛先</strong>] 行に含める、メッセージの受信者名を指定します。この引数を指定しないと、受信者名を確認するダイアログ ボックスが表示されます。 この引数、" <strong>Cc/CC</strong>" 引数、および " <strong>Bcc/BCC</strong>" 引数で複数の受信者の名前を指定する場合は、セミコロン (;)、または Microsoft Windows <strong>コントロール パネル</strong>の [ <strong>地域のオプションのカスタマイズ</strong>] ダイアログ ボックスの [ <strong>数値</strong>] タブで設定した区切り記号で区切ります。メール アプリケーションで受信者名を識別できない場合は、メッセージが送信されずにエラーが発生します。  </span><span class="sxs-lookup"><span data-stu-id="5470f-p104">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5470f-133"><strong>Cc/CC</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-133"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-134">メールメッセージの [ <strong>Cc</strong> ] (&quot;カーボンコピー&quot;) 行に登録するメッセージの受信者名を入力します。</span><span class="sxs-lookup"><span data-stu-id="5470f-134">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="5470f-135">この引数を指定しない場合、メール メッセージの [ <strong>CC</strong>] 行が空白になります。</span><span class="sxs-lookup"><span data-stu-id="5470f-135">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5470f-136"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-136"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-137">メールメッセージの<strong>Bcc</strong> (&quot;ブラインドカーボンコピー&quot;) 行に配置するメッセージの受信者名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5470f-137">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="5470f-138">この引数を指定しない場合、メール メッセージの [ <strong>BCC</strong>] 行が空白になります。</span><span class="sxs-lookup"><span data-stu-id="5470f-138">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5470f-139"><strong>Subject/件名</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-139"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p107">メッセージの件名を指定します。このテキストはメール メッセージの [ <strong>件名</strong>] 行に表示されます。この引数を指定しない場合、メール メッセージの [ <strong>件名</strong>] 行が空白になります。  </span><span class="sxs-lookup"><span data-stu-id="5470f-p107">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5470f-143"><strong>Message Text/メッセージ</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-143"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p108">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.  </span><span class="sxs-lookup"><span data-stu-id="5470f-p108">Any text you want to include in the message in addition to the database object. This text appears in the main body of the mail message, after the object. If you leave this argument blank, no additional text is included in the mail message. If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5470f-148"><strong>Edit Message/メッセージの編集</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-148"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p109">メッセージを送信する前に編集できるかどうかを指定します。[ <strong>はい</strong>] を選択すると、電子メール アプリケーションが自動的に起動し、メッセージを編集できるようになります。[ <strong>いいえ</strong>] を選択すると、送信前にメッセージを編集できなくなります。既定値は [ <strong>はい</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="5470f-p109">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5470f-153"><strong>Template File/テンプレート ファイル</strong></span><span class="sxs-lookup"><span data-stu-id="5470f-153"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="5470f-p110">HTML ファイルのテンプレートとして使用するファイルのパスとファイル名を指定します。テンプレート ファイルとは、HTML タグを含むファイルです。</span><span class="sxs-lookup"><span data-stu-id="5470f-p110">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5470f-156">注釈</span><span class="sxs-lookup"><span data-stu-id="5470f-156">Remarks</span></span>

<span data-ttu-id="5470f-p111">メール メッセージのオブジェクトは、指定した出力形式で出力されます。オブジェクトをダブルクリックすると、対応するソフトウェアが起動し、オブジェクトが開きます。</span><span class="sxs-lookup"><span data-stu-id="5470f-p111">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="5470f-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span><span class="sxs-lookup"><span data-stu-id="5470f-159">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="5470f-p112">テーブル、クエリ、およびフォームの各データシートを送信できます。添付されるオブジェクトには、OLE オブジェクトを含むフィールドを除くデータシートのすべてのフィールドが出力されます。OLE オブジェクトを含むフィールドの列もオブジェクトに出力されますが、フィールド値は空白になります。</span><span class="sxs-lookup"><span data-stu-id="5470f-p112">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="5470f-163">yes/No 型フィールド (トグルボタン、オプションボタン、チェックボックス) に連結されたコントロールの場合、出力ファイルには-1 (Yes) または 0 (No) の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5470f-163">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="5470f-164">ハイパーリンク型 (Hyperlink) フィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが出力されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして出力されます)。</span><span class="sxs-lookup"><span data-stu-id="5470f-164">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="5470f-165">フォーム ビューのフォームを送信する場合、添付されるオブジェクトには常にフォームのデータシート ビューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5470f-165">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="5470f-p113">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span><span class="sxs-lookup"><span data-stu-id="5470f-p113">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels. All other controls are ignored. Header and footer information is also not included. The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object. No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="5470f-171">サブレポートはオブジェクトに取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="5470f-171">Subreports are included in the object.</span></span>

- <span data-ttu-id="5470f-p114">HTML 形式のデータシート、フォーム、またはデータ アクセス ページを送信する場合は, .html ファイルが 1 つ作成されます。HTML 形式のレポートを送信する場合は, .html ファイルがレポートのページごとに 1 つずつ作成されます。</span><span class="sxs-lookup"><span data-stu-id="5470f-p114">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="5470f-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="5470f-174">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="5470f-175">共同作成者について</span><span class="sxs-lookup"><span data-stu-id="5470f-175">About the contributor</span></span>

<span data-ttu-id="5470f-176">**リンクの提供**元Luke Chung、 [fms、inc.](https://www.fmsinc.com/)、FMS、inc. の創設者および社長。これは、カスタムデータベースソリューションおよび開発者ツールのリーディングプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="5470f-176">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

- [<span data-ttu-id="5470f-177">送信用の SendObject メソッドの使用に関する機能と制限</span><span class="sxs-lookup"><span data-stu-id="5470f-177">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





