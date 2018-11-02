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
ms.openlocfilehash: 847f23c429b06fee51b42aa211d672b051accb7c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920397"
---
# <a name="importexportdata-macro-action"></a><span data-ttu-id="a65bb-102">ImportExportData マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a65bb-102">ImportExportData macro action</span></span>

<span data-ttu-id="a65bb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a65bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a65bb-104">インポートまたは現在の Access データベース (.mdb または .accdb) または Access プロジェクト (.adp) と他のデータベース間でデータをエクスポートするのには、 **ImportExportData**アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-104">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database.</span></span> <span data-ttu-id="a65bb-105">Microsoft Access データベースでは、他のデータベースからカレント データベースにテーブルをリンクすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-105">For Microsoft Access databases, you can also link a table to the current Access database from another database.</span></span> <span data-ttu-id="a65bb-106">テーブルをリンクすると、テーブル自体は他のデータベース内にあっても、そのテーブルのデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-106">With a linked table, you have access to the table's data while the table itself remains in the other database.</span></span>

> [!NOTE]
> <span data-ttu-id="a65bb-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="settings"></a><span data-ttu-id="a65bb-109">設定値</span><span class="sxs-lookup"><span data-stu-id="a65bb-109">Settings</span></span>

<span data-ttu-id="a65bb-110">**ImportExportData**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="a65bb-110">The **ImportExportData** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a65bb-111">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="a65bb-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a65bb-112">説明</span><span class="sxs-lookup"><span data-stu-id="a65bb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a65bb-113"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-113"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p103">変換の種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>変換の種類</strong>] ボックスで、[ <strong>インポート</strong>]、[ <strong>エクスポート</strong>]、または [ <strong>リンク</strong>] を選択します。既定値は [ <strong>インポート</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="a65bb-117">[**リンク**] は、Access プロジェクト (.adp) ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a65bb-117">The **Link** transfer type is not supported for Access projects (.adp).</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65bb-118"><strong>Database Type/データベースの種類</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-118"><strong>Database Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p104">インポート元、エクスポート先、またはリンク先のデータベースの種類を指定します。[ <strong>データベースの種類</strong>] ボックスでは、[ <strong>Microsoft Access</strong>] などの多数のデータベースの種類から選択できます。既定値は [ <strong>Microsoft Access</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p104">The type of database to import from, export to, or link to. You can select <strong>Microsoft Access</strong> or one of a number of other database types in the <strong>Database Type</strong> box. The default is <strong>Microsoft Access</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65bb-122"><strong>Database Name/データベース名</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-122"><strong>Database Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p105">インポート元、エクスポート先、またはリンク先のデータベースの名前を指定します。この引数は省略できません。FoxPro、Paradox、dBASE など、テーブルごとにファイルを作成するデータベースの場合は、ファイルを含むディレクトリを入力します。ファイル名は、" <strong>Source/オブジェクト名</strong> " 引数 (インポートまたはリンクの場合) または " <strong>Destination/変換先名</strong> " 引数 (エクスポートの場合) に入力します。ODBC データベースの場合は、完全な ODBC (Open Database Connectivity) 接続文字列を入力します。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p105">The name of the database to import from, export to, or link to. Include the full path. This is a required argument. For types of databases that use separate files for each table, such as FoxPro, Paradox, and dBASE, enter the directory containing the file. Enter the file name in the <strong>Source</strong> argument (to import or link) or the <strong>Destination</strong> argument (to export). For ODBC databases, type the full Open Database Connectivity (ODBC) connection string.</span></span></p>
<p><span data-ttu-id="a65bb-129">接続文字列の例を参照するには、次の手順で、外部テーブルを Access にリンクします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-129">To see an example of a connection string, link an external table to Access:</span></span></p>
<ol>
<li><p><span data-ttu-id="a65bb-130">[ <strong>外部データの取り込み</strong>] ダイアログ ボックスで、[ <strong>ファイル名</strong>] ボックスにソース データベースのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-130">In the <strong>Get External Data</strong> dialog box, enter the path of your source database in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="a65bb-131">[ <strong>リンク テーブルを作成してソース データにリンクする</strong>] をクリックし、[ <strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-131">Click <strong>Link to the data source by creating a linked table</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a65bb-132">[ <strong>テーブルのリンク</strong>] ダイアログ ボックスでテーブルを選択し、[ <strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-132">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="a65bb-133">新しくリンクしたテーブルをデザイン ビューで開きし、[<strong>デザイン</strong>] タブの [<strong>ツール</strong> <strong>] プロパティ ・ シート</strong>をクリックしてテーブルのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-133">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>.</span></span> <span data-ttu-id="a65bb-134"><strong>説明</strong>プロパティの設定値のテキストは、このテーブルの接続文字列です。</span><span class="sxs-lookup"><span data-stu-id="a65bb-134">The text in the <strong>Description</strong> property setting is the connection string for this table.</span></span></p>
<p><span data-ttu-id="a65bb-135">ODBC 接続文字列の詳細については、ヘルプ ファイルまたは ODBC ドライバーの ODBC データベースには、この種類の他の資料を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a65bb-135">For more information about ODBC connection strings, see the Help file or other documentation for the ODBC driver of this type of ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65bb-136"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-136"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p107">インポートまたはエクスポートするオブジェクトの種類を指定します。" <strong>Database Type/データベースの種類</strong> " 引数に [ <strong>Microsoft Access</strong>] を指定した場合は、[ <strong>オブジェクトの種類</strong>] ボックスで、[ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、または [ <strong>関数</strong>] を選択できます。既定値は [ <strong>テーブル</strong>] です。その他の種類のデータベースを選択した場合、または [ <strong>変換の種類</strong>] ボックスで [ <strong>リンク</strong>] を選択した場合、この引数は無視されます。選択クエリを Access データベースにエクスポートする場合、クエリの結果セットをエクスポートするには [ <strong>テーブル</strong>] を選択し、クエリ自体をエクスポートするには [ <strong>クエリ</strong>] を選択します。選択クエリを別の種類のデータベースにエクスポートする場合は、この引数が無視され、クエリの結果セットがエクスポートされます。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p107">The type of object to import or export. If you select <strong>Microsoft Access</strong> for the <strong>Database Type</strong> argument, you can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box. The default is <strong>Table</strong>. If you select any other type of database, or if you select <strong>Link</strong> in the <strong>Transfer Type</strong> box, this argument is ignored. If you are exporting a select query to an Access database, select <strong>Table</strong> in this argument to export the result set of the query, and select <strong>Query</strong> to export the query itself. If you are exporting a select query to another type of database, this argument is ignored and the result set of the query is exported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65bb-143"><strong>Source/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-143"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p108">インポート、エクスポート、またはリンクの対象となるテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p108">The name of the table, select query, or Access object that you want to import, export, or link. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a65bb-148"><strong>Destination/変換先名</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-148"><strong>Destination</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p109">変換先データベースにインポート、エクスポート、またはリンクした後のテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。 この引数は省略できません。 " <strong>Transfer Type (変換の種類)</strong> " 引数で [ <strong>インポート</strong>] を選択し、" <strong>Object Type (オブジェクトの種類)</strong> " 引数で <strong>テーブル</strong> を選択した場合、テーブルが新規作成され、指定したテーブルのデータがインポートされます。 テーブルまたはその他のオブジェクトをインポートしたときに既存の名前と競合する場合は、その名前に番号が追加されます。たとえば、"社員" テーブルをインポートしたときに "社員" という名前のテーブルが既に存在する場合、インポートしたテーブルの名前は "社員 1" に変更されます。 Access データベースまたはその他のデータベースにエクスポートした場合は、同じ名前の既存のテーブルあるいはその他のオブジェクトは自動的に置き換わります。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p109">The name of the imported, exported, or linked table, select query, or Access object in the destination database. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument and <strong>Table</strong> in the <strong>Object Type</strong> argument, Access creates a new table containing the data in the imported table. If you import a table or other object, Access adds a number to the name if it conflicts with an existing name. For example, if you import Employees and Employees already exists, Access renames the imported table or other object Employees1. If you export to an Access database or another database, Access automatically replaces any existing table or other object that has the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a65bb-157"><strong>Structure Only/テーブル構造のみ変換</strong></span><span class="sxs-lookup"><span data-stu-id="a65bb-157"><strong>Structure Only</strong></span></span></p></td>
<td><p><span data-ttu-id="a65bb-p110">データベース テーブルの構造のみ (データを除く) をインポートまたはエクスポートするかどうかを指定します。[ <strong>はい</strong>] または [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>いいえ</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="a65bb-p110">Specifies whether to import or export only the structure of a database table without any of its data. Select <strong>Yes</strong> or <strong>No</strong>. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a65bb-161">解説</span><span class="sxs-lookup"><span data-stu-id="a65bb-161">Remarks</span></span>

<span data-ttu-id="a65bb-p111">Access のデータベースと他のデータベースの間で、テーブルのインポートやエクスポートを行うことができます。また、Access の選択クエリを他のデータベースにエクスポートすることもできます。クエリの結果セットはテーブルとしてエクスポートされます。Access のデータベース間では、Access のあらゆるデータベース オブジェクトをインポートまたはエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p111">You can import and export tables between Access and other types of databases. You can also export Access select queries to other types of databases. Access exports the result set of the query in the form of a table. You can import and export any Access database object if both databases are Access databases.</span></span>

<span data-ttu-id="a65bb-p112">他の Access のデータベース (.mdb または .accdb) から、そのデータベース内でリンクされているテーブルをインポートした場合は、インポート後もリンクが維持されます。つまり、テーブル自体ではなく、リンクがインポートされます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p112">If you import a table from another Access database (.mdb or .accdb) that's a linked table in that database, it will still be linked after you import it. That is, the link is imported, not the table itself.</span></span>

<span data-ttu-id="a65bb-p113">アクセスしようとしているデータベースでパスワードが要求される場合は、マクロの実行時に表示されるダイアログ ボックスにパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p113">If the database you're accessing requires a password, a dialog box appears when you run the macro. Type the password in this dialog box.</span></span>

<span data-ttu-id="a65bb-170">**ImportExportData**アクションは、[**外部データ**] タブの [**インポート**または**エクスポート**のコマンドに似ています。</span><span class="sxs-lookup"><span data-stu-id="a65bb-170">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**.</span></span> <span data-ttu-id="a65bb-171">これらのコマンドを使用すると、Access データベースまたは別の種類のデータベース、スプレッドシート、またはテキスト ファイルなどのデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-171">You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file.</span></span> <span data-ttu-id="a65bb-172">データベースを選択する場合は、インポートまたはエクスポート (のデータベースにアクセス) するオブジェクトの種類、オブジェクト、およびデータベースからのインポートまたはエクスポートまたはリンクによって、その他のオプションの名前を選択する 1 つまたは複数のダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-172">If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to.</span></span> <span data-ttu-id="a65bb-173">**ImportExportData**アクションの引数は、これらのダイアログ ボックスでオプションを反映します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-173">The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span></span>

<span data-ttu-id="a65bb-174">リンクする dBASE テーブルにインデックス情報を指定する場合は、まず、次の手順でテーブルをリンクします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-174">If you want to supply index information for a linked dBASE table, first link the table:</span></span>

1.  <span data-ttu-id="a65bb-175">[ **dBASE ファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-175">Click **dBASE File**.</span></span>

2.  <span data-ttu-id="a65bb-176">[ **外部データの取り込み**] ダイアログ ボックスで、[ **ファイル名**] ボックスに dBASE ファイルのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-176">In the **Get External Data** dialog box, enter the path for the dBASE file in the **File name** box.</span></span>

3.  <span data-ttu-id="a65bb-177">[ **リンク テーブルを作成してソース データにリンクする**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a65bb-177">Click **Link to the data source by creating a linked table**, then click **OK**.</span></span>

4.  <span data-ttu-id="a65bb-p115">このコマンドのダイアログ ボックスでインデックスを指定します。インデックス情報は、Microsoft Office フォルダーにある特別な情報 (.inf) ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-p115">Specify the indexes in the dialog boxes for this command. Access stores the index information in a special information (.inf) file, located in the Microsoft Office folder.</span></span>

5.  <span data-ttu-id="a65bb-180">この時点で、リンク テーブルへのリンクを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-180">You can then delete the link to the linked table.</span></span>

<span data-ttu-id="a65bb-181">この dBASE テーブルをリンクする**ImportExportData**アクションを使用する次の時間は、指定したインデックス情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-181">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span></span>

> [!NOTE]
> <span data-ttu-id="a65bb-182">[!メモ] リンクしたテーブルに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="a65bb-182">If you query or filter a linked table, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="a65bb-183">Visual Basic for Applications (VBA) モジュールに**ImportExportData**アクションを実行するには、 **DoCmd**オブジェクトの**TransferDatabase**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a65bb-183">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span></span>

