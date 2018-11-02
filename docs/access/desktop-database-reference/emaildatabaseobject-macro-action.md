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
ms.openlocfilehash: f0c0ba73274d6f27a9e2a857aea1061416168f3a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922917"
---
# <a name="emaildatabaseobject-macro-action"></a><span data-ttu-id="15e53-102">EMailDatabaseObject マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="15e53-102">EMailDatabaseObject macro action</span></span>

<span data-ttu-id="15e53-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="15e53-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="15e53-104">**EMailDatabaseObject**アクションを使用すると、指定した Access データシート、フォーム、レポート、モジュール、またはデータ アクセス ページは、メール メッセージを表示および転送できます。</span><span class="sxs-lookup"><span data-stu-id="15e53-104">You can use the **EMailDatabaseObject** action to include the specified Microsoft Access datasheet, form, report, module, or data access page in an electronic mail message, where it can be viewed and forwarded.</span></span>

> [!NOTE]
> <span data-ttu-id="15e53-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="15e53-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="15e53-107">設定値</span><span class="sxs-lookup"><span data-stu-id="15e53-107">Settings</span></span>

<span data-ttu-id="15e53-108">**EMailDatabaseObject**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="15e53-108">The **EMailDatabaseObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15e53-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="15e53-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="15e53-110">説明</span><span class="sxs-lookup"><span data-stu-id="15e53-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15e53-111"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-112">メール メッセージに添付するオブジェクトの型。</span><span class="sxs-lookup"><span data-stu-id="15e53-112">The type of object to include in the mail message.</span></span> <span data-ttu-id="15e53-113"><strong>テーブル</strong>(テーブル: データシートの場合)、<strong>クエリ</strong>(クエリ データシートの場合)、(フォームまたはフォームのデータシートの場合) の<strong>フォーム</strong>、<strong>レポート</strong>、<strong>モジュール</strong>、または<strong>データ アクセス ページ</strong>、<strong>サーバー ビュー</strong>、<strong>ストアド プロシージャ</strong>、または<strong>をクリックします。関数</strong>、[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの<strong>オブジェクトの種類</strong>ボックスにします。</span><span class="sxs-lookup"><span data-stu-id="15e53-113">Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, or <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Stored Procedures</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="15e53-114">マクロを送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="15e53-114">You can't send a macro.</span></span> <span data-ttu-id="15e53-115">アクティブ オブジェクトを添付する場合は、この引数でオブジェクトの種類を選択が、<strong>オブジェクト名</strong>の引数を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="15e53-115">If you want to include the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15e53-116"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-p103">メール メッセージに添付するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数と " <strong>Object Name/オブジェクト名</strong> " 引数を両方とも指定しない場合は、データベース オブジェクトが添付されていないメッセージがメール アプリケーションに送信されます。 ライブラリ データベースで " <strong>EMailDatabaseObject/ データベースオブジェクトの電子メール送信</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="15e53-p103">The name of the object to include in the mail message. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave both the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, Access sends a message to the mail application without any database object. If you run a macro containing the <strong>EMailDatabaseObject</strong> action in a library database, Access looks for the object with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15e53-121"><strong>Output Format/出力ファイル形式</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-121"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-122">含まれているオブジェクトを使用形式の種類。</span><span class="sxs-lookup"><span data-stu-id="15e53-122">The type of format you want used for the included object.</span></span> <span data-ttu-id="15e53-123">選択できる形式の一覧は、<strong>オブジェクトの型</strong>引数で選択した種類に応じて変更されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-123">The list of formats you can select from will change depending on what you select for the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="15e53-124">使用可能な形式は、 <strong>Excel 97 - 2003年ブック (*.xls)</strong>、 <strong>Excel バイナリ ブック (*.xlsb)</strong>、 <strong>Excel ブック (*.xlsx)</strong>を含めることが<strong>HTML (*.htm、\* .html)</strong>、 <strong>Microsoft Excel 5.0/95 ブック (*.xls)</strong>、PDF 形式の<strong></strong>、<strong>リッチ テキスト書式 (の式 *.rtf)</strong>、<strong>テキスト ファイル (*.txt)</strong>、または<strong>XPS 形式 (*.xps)</strong>。</span><span class="sxs-lookup"><span data-stu-id="15e53-124">Available formats may include <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm, *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format</strong>, <strong>Rich Text Fomat (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (\*.xps)</strong>.</span></span> <span data-ttu-id="15e53-125"><strong>出力形式</strong>] ボックスにします。</span><span class="sxs-lookup"><span data-stu-id="15e53-125">in the <strong>Output Format</strong> box.</span></span> <span data-ttu-id="15e53-126">モジュールはテキスト形式でのみ送信できます。</span><span class="sxs-lookup"><span data-stu-id="15e53-126">Modules can be sent only in text format.</span></span> <span data-ttu-id="15e53-127">データ アクセス ページは HTML 形式でのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-127">Data access pages can only be sent in HTML format.</span></span> <span data-ttu-id="15e53-128">この引数を指定しないと、出力形式を確認するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-128">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15e53-129"><strong>To/宛先</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-129"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-p105">メール メッセージの [ <strong>宛先</strong>] 行に含める、メッセージの受信者名を指定します。この引数を指定しないと、受信者名を確認するダイアログ ボックスが表示されます。 この引数、" <strong>Cc/CC</strong>" 引数、および " <strong>Bcc/BCC</strong>" 引数で複数の受信者の名前を指定する場合は、セミコロン (;)、または Microsoft Windows <strong>コントロール パネル</strong>の [ <strong>地域のオプションのカスタマイズ</strong>] ダイアログ ボックスの [ <strong>数値</strong>] タブで設定した区切り記号で区切ります。メール アプリケーションで受信者名を識別できない場合は、メッセージが送信されずにエラーが発生します。  </span><span class="sxs-lookup"><span data-stu-id="15e53-p105">The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15e53-134"><strong>Cc/CC</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-134"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-135">受信者名を<strong>[cc]</strong>に追加する (&quot;カーボン コピー&quot;)、メール メッセージ内の行です。</span><span class="sxs-lookup"><span data-stu-id="15e53-135">The message recipients whose names you want to put on the <strong>Cc</strong> (&quot;carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="15e53-136">この引数を指定しない場合、メール メッセージの [ <strong>CC</strong>] 行が空白になります。</span><span class="sxs-lookup"><span data-stu-id="15e53-136">If you leave this argument blank, the <strong>Cc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15e53-137"><strong>Bcc/BCC</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-137"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-138">メッセージの受信者に<strong>Bcc</strong>を追加する名前 (&quot;ブラインド カーボン コピー&quot;)、メール メッセージ内の行です。</span><span class="sxs-lookup"><span data-stu-id="15e53-138">The message recipients whose names you want to put on the <strong>Bcc</strong> (&quot;blind carbon copy&quot;) line in the mail message.</span></span> <span data-ttu-id="15e53-139">この引数を指定しない場合、メール メッセージの [ <strong>BCC</strong>] 行が空白になります。</span><span class="sxs-lookup"><span data-stu-id="15e53-139">If you leave this argument blank, the <strong>Bcc</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15e53-140"><strong>Subject/件名</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-140"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-p108">メッセージの件名を指定します。このテキストはメール メッセージの [ <strong>件名</strong>] 行に表示されます。この引数を指定しない場合、メール メッセージの [ <strong>件名</strong>] 行が空白になります。  </span><span class="sxs-lookup"><span data-stu-id="15e53-p108">The subject of the message. This text appears on the <strong>Subject</strong> line in the mail message. If you leave this argument blank, the <strong>Subject</strong> line in the mail message is blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15e53-144"><strong>Message Text/メッセージ</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-144"><strong>Message Text</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-145">データベース オブジェクトと共にメール メッセージに含めるテキストです。</span><span class="sxs-lookup"><span data-stu-id="15e53-145">Any text you want to include in the message in addition to the database object.</span></span> <span data-ttu-id="15e53-146">オブジェクトの後に、メール メッセージの本文にこのテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-146">This text appears in the main body of the mail message, after the object.</span></span> <span data-ttu-id="15e53-147">この引数を空白のままにする場合追加のテキストが含まれていないメール メッセージにします。</span><span class="sxs-lookup"><span data-stu-id="15e53-147">If you leave this argument blank, no additional text is included in the mail message.</span></span> <span data-ttu-id="15e53-148"><strong>オブジェクト型</strong>および<strong>オブジェクト名</strong>の引数を空白のままにする場合は、データベース オブジェクトにメッセージを送信するのにはこの引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="15e53-148">If you leave the <strong>Object Type</strong> and <strong>Object Name</strong> arguments blank, you can use this argument to send a mail message without a database object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15e53-149"><strong>Edit Message/メッセージの編集</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-149"><strong>Edit Message</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-p110">メッセージを送信する前に編集できるかどうかを指定します。[ <strong>はい</strong>] を選択すると、電子メール アプリケーションが自動的に起動し、メッセージを編集できるようになります。[ <strong>いいえ</strong>] を選択すると、送信前にメッセージを編集できなくなります。既定値は [ <strong>はい</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="15e53-p110">Specifies whether the message can be edited before it's sent. If you select <strong>Yes</strong>, the electronic mail application starts automatically, and the message can be edited. If you select <strong>No</strong>, the message is sent without the user having a chance to edit the message. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15e53-154"><strong>Template File/テンプレート ファイル</strong></span><span class="sxs-lookup"><span data-stu-id="15e53-154"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="15e53-p111">HTML ファイルのテンプレートとして使用するファイルのパスとファイル名を指定します。テンプレート ファイルとは、HTML タグを含むファイルです。</span><span class="sxs-lookup"><span data-stu-id="15e53-p111">The path and file name of a file you want to use as a template for an HTML file. The template file is a file containing HTML tags.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="15e53-157">解説</span><span class="sxs-lookup"><span data-stu-id="15e53-157">Remarks</span></span>

<span data-ttu-id="15e53-p112">メール メッセージのオブジェクトは、指定した出力形式で出力されます。オブジェクトをダブルクリックすると、対応するソフトウェアが起動し、オブジェクトが開きます。</span><span class="sxs-lookup"><span data-stu-id="15e53-p112">The object in the mail message is in the selected output format. When you double-click the object, the appropriate software starts with the object opened.</span></span>

<span data-ttu-id="15e53-160">**EMailDatabaseObject**アクションを使用するデータベース オブジェクトをメール メッセージに挿入するときは、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-160">The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:</span></span>

- <span data-ttu-id="15e53-p113">テーブル、クエリ、およびフォームの各データシートを送信できます。添付されるオブジェクトには、OLE オブジェクトを含むフィールドを除くデータシートのすべてのフィールドが出力されます。OLE オブジェクトを含むフィールドの列もオブジェクトに出力されますが、フィールド値は空白になります。</span><span class="sxs-lookup"><span data-stu-id="15e53-p113">You can send table, query, and form datasheets. In the included object, all fields in the datasheet look as they do in Access, except fields containing OLE objects. The columns for these fields are included in the object, but the fields are blank.</span></span>

- <span data-ttu-id="15e53-164">Yes/No 型フィールド (トグル ボタン、オプション ボタン、チェック ボックス) に連結されたコントロールの場合、出力ファイルには \uc1\u8211 ?1 (Yes) または 0 (No) の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-164">For a control bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

- <span data-ttu-id="15e53-165">ハイパーリンク型 (Hyperlink) フィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが出力されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして出力されます)。</span><span class="sxs-lookup"><span data-stu-id="15e53-165">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats except MS-DOS text (in this case, the hyperlink is just displayed as normal text).</span></span>

- <span data-ttu-id="15e53-166">フォーム ビューのフォームを送信する場合、添付されるオブジェクトには常にフォームのデータシート ビューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="15e53-166">If you send a form in Form view, the included object always contains the form's Datasheet view.</span></span>

- <span data-ttu-id="15e53-167">レポートを送信する場合のみ、オブジェクトに含まれるコントロールはテキスト ボックスといくつかの場合) のラベルです。</span><span class="sxs-lookup"><span data-stu-id="15e53-167">If you send a report, the only controls that are included in the object are text boxes and (in some cases) labels.</span></span> <span data-ttu-id="15e53-168">他のすべてのコントロールは無視されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-168">All other controls are ignored.</span></span> <span data-ttu-id="15e53-169">ヘッダーとフッターの情報も含まれていません。</span><span class="sxs-lookup"><span data-stu-id="15e53-169">Header and footer information is also not included.</span></span> <span data-ttu-id="15e53-170">唯一の例外は、Excel 形式でレポートを送信するときに、 **Sum**関数を使った式が含まれているグループ フッターのテキスト ボックスがオブジェクトに含まれています。</span><span class="sxs-lookup"><span data-stu-id="15e53-170">The only exception to this is that when you send a report in Excel format, a text box in a group footer containing an expression with the **Sum** function is included in the object.</span></span> <span data-ttu-id="15e53-171">オブジェクトでは、ヘッダー、フッターおよび関数**Sum**以外の集計関数) には、他のコントロールが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="15e53-171">No other control in a header or footer (and no aggregate function other than **Sum**) is included in the object.</span></span>

- <span data-ttu-id="15e53-172">サブレポートはオブジェクトに取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="15e53-172">Subreports are included in the object.</span></span>

- <span data-ttu-id="15e53-p115">HTML 形式のデータシート、フォーム、またはデータ アクセス ページを送信する場合は, .html ファイルが 1 つ作成されます。HTML 形式のレポートを送信する場合は, .html ファイルがレポートのページごとに 1 つずつ作成されます。</span><span class="sxs-lookup"><span data-stu-id="15e53-p115">When you send a datasheet, form, or data access page in HTML format, one .html file is created. When you send a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="15e53-175">Visual Basic for Applications (VBA) モジュールに**EMailDatabaseObject**アクションを実行するには、 **DoCmd**オブジェクトの**SendObject**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="15e53-175">To run the **EMailDatabaseObject** action in a Visual Basic for Applications (VBA) module, use the **SendObject** method of the **DoCmd** object.</span></span>

### <a name="about-the-contributor"></a><span data-ttu-id="15e53-176">投稿者について</span><span class="sxs-lookup"><span data-stu-id="15e53-176">About the contributor</span></span>

<span data-ttu-id="15e53-177">**によってリンクが提供されます。** Luke Chung [FMS, Inc.](https://www.fmsinc.com/)、創設者で、FMS, Inc. は、カスタム データベース ソリューションと開発ツールのリーディング ・ プロバイダーの社長です。</span><span class="sxs-lookup"><span data-stu-id="15e53-177">**Link provided by** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), the founder and president of FMS, Inc., a leading provider of custom database solutions and developer tools.</span></span>

  - [<span data-ttu-id="15e53-178">送信用の SendObject メソッドの使用に関する機能と制限</span><span class="sxs-lookup"><span data-stu-id="15e53-178">Features and Limits of Using the SendObject Method to Send</span></span>](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





