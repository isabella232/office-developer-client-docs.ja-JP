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
# <a name="importexportdata-macro-action"></a><span data-ttu-id="baaf4-102">ImportExportData マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="baaf4-102">ImportExportData macro action</span></span>

<span data-ttu-id="baaf4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="baaf4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baaf4-p101">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.</span><span class="sxs-lookup"><span data-stu-id="baaf4-p101">You can use the **ImportExportData** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and another database. For Microsoft Access databases, you can also link a table to the current Access database from another database. With a linked table, you have access to the table's data while the table itself remains in the other database.</span></span>

> [!NOTE]
> <span data-ttu-id="baaf4-107">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="baaf4-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="settings"></a><span data-ttu-id="baaf4-108">設定</span><span class="sxs-lookup"><span data-stu-id="baaf4-108">Settings</span></span>

<span data-ttu-id="baaf4-109">"ImportExportData/データのインポート/エクスポート" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="baaf4-109">The **ImportExportData** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="baaf4-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="baaf4-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="baaf4-111">説明</span><span class="sxs-lookup"><span data-stu-id="baaf4-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="baaf4-112"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-112"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p102">変換の種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>変換の種類</strong>] ボックスで、[ <strong>インポート</strong>]、[ <strong>エクスポート</strong>]、または [ <strong>リンク</strong>] を選択します。既定値は [ <strong>インポート</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p102">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p><p><span data-ttu-id="baaf4-116"><strong>注意</strong>: Access プロジェクト (.adp) では、転送の種類 <strong>[リンク]</strong> はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="baaf4-116"><strong>NOTE</strong>: The <strong>Link</strong> transfer type is not supported for Access projects (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baaf4-117"><strong>Database Type/データベースの種類</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-117"><strong>Database Type</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p103">インポート元、エクスポート先、またはリンク先のデータベースの種類を指定します。[ <strong>データベースの種類</strong>] ボックスでは、[ <strong>Microsoft Access</strong>] などの多数のデータベースの種類から選択できます。既定値は [ <strong>Microsoft Access</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p103">The type of database to import from, export to, or link to. You can select <strong>Microsoft Access</strong> or one of a number of other database types in the <strong>Database Type</strong> box. The default is <strong>Microsoft Access</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baaf4-121"><strong>Database Name/データベース名</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-121"><strong>Database Name</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p104">インポート元、エクスポート先、またはリンク先のデータベースの名前を指定します。この引数は省略できません。FoxPro、Paradox、dBASE など、テーブルごとにファイルを作成するデータベースの場合は、ファイルを含むディレクトリを入力します。ファイル名は、" <strong>Source/オブジェクト名</strong> " 引数 (インポートまたはリンクの場合) または " <strong>Destination/変換先名</strong> " 引数 (エクスポートの場合) に入力します。ODBC データベースの場合は、完全な ODBC (Open Database Connectivity) 接続文字列を入力します。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p104">The name of the database to import from, export to, or link to. Include the full path. This is a required argument. For types of databases that use separate files for each table, such as FoxPro, Paradox, and dBASE, enter the directory containing the file. Enter the file name in the <strong>Source</strong> argument (to import or link) or the <strong>Destination</strong> argument (to export). For ODBC databases, type the full Open Database Connectivity (ODBC) connection string.</span></span></p>
<p><span data-ttu-id="baaf4-128">接続文字列の例を参照するには、次の手順で、外部テーブルを Access にリンクします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-128">To see an example of a connection string, link an external table to Access:</span></span></p>
<ol>
<li><p><span data-ttu-id="baaf4-129">[ <strong>外部データの取り込み</strong>] ダイアログ ボックスで、[ <strong>ファイル名</strong>] ボックスにソース データベースのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="baaf4-129">In the <strong>Get External Data</strong> dialog box, enter the path of your source database in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="baaf4-130">[ <strong>リンク テーブルを作成してソース データにリンクする</strong>] をクリックし、[ <strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-130">Click <strong>Link to the data source by creating a linked table</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="baaf4-131">[ <strong>テーブルのリンク</strong>] ダイアログ ボックスでテーブルを選択し、[ <strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-131">Select a table in the <strong>Link Tables</strong> dialog box, and click <strong>OK</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="baaf4-p105">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p105">Open the newly linked table in Design view and view the table properties by clicking <strong>Property Sheet</strong> on the <strong>Design</strong> tab, under <strong>Tools</strong>. The text in the <strong>Description</strong> property setting is the connection string for this table.</span></span></p>
<p><span data-ttu-id="baaf4-134">odbc 接続文字列の詳細については、この odbc データベースの odbc ドライバーのヘルプファイルまたはその他のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="baaf4-134">For more information about ODBC connection strings, see the Help file or other documentation for the ODBC driver of this type of ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baaf4-135"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-135"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p106">インポートまたはエクスポートするオブジェクトの種類を指定します。" <strong>Database Type/データベースの種類</strong> " 引数に [ <strong>Microsoft Access</strong>] を指定した場合は、[ <strong>オブジェクトの種類</strong>] ボックスで、[ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、または [ <strong>関数</strong>] を選択できます。既定値は [ <strong>テーブル</strong>] です。その他の種類のデータベースを選択した場合、または [ <strong>変換の種類</strong>] ボックスで [ <strong>リンク</strong>] を選択した場合、この引数は無視されます。選択クエリを Access データベースにエクスポートする場合、クエリの結果セットをエクスポートするには [ <strong>テーブル</strong>] を選択し、クエリ自体をエクスポートするには [ <strong>クエリ</strong>] を選択します。選択クエリを別の種類のデータベースにエクスポートする場合は、この引数が無視され、クエリの結果セットがエクスポートされます。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p106">The type of object to import or export. If you select <strong>Microsoft Access</strong> for the <strong>Database Type</strong> argument, you can select <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box. The default is <strong>Table</strong>. If you select any other type of database, or if you select <strong>Link</strong> in the <strong>Transfer Type</strong> box, this argument is ignored. If you are exporting a select query to an Access database, select <strong>Table</strong> in this argument to export the result set of the query, and select <strong>Query</strong> to export the query itself. If you are exporting a select query to another type of database, this argument is ignored and the result set of the query is exported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baaf4-142"><strong>Source/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-142"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p107">インポート、エクスポート、またはリンクの対象となるテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="baaf4-p107">The name of the table, select query, or Access object that you want to import, export, or link. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="baaf4-147"><strong>Destination/変換先名</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-147"><strong>Destination</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p108">変換先データベースにインポート、エクスポート、またはリンクした後のテーブル、選択クエリ、または Access オブジェクトの名前を指定します。FoxPro、Paradox、dBASE などのデータベースの場合は、ファイル名を指定します。このファイル名にはファイル名拡張子 (.dbf など) を含めます。 この引数は省略できません。 " <strong>Transfer Type (変換の種類)</strong> " 引数で [ <strong>インポート</strong>] を選択し、" <strong>Object Type (オブジェクトの種類)</strong> " 引数で <strong>テーブル</strong> を選択した場合、テーブルが新規作成され、指定したテーブルのデータがインポートされます。 テーブルまたはその他のオブジェクトをインポートしたときに既存の名前と競合する場合は、その名前に番号が追加されます。たとえば、"社員" テーブルをインポートしたときに "社員" という名前のテーブルが既に存在する場合、インポートしたテーブルの名前は "社員 1" に変更されます。 Access データベースまたはその他のデータベースにエクスポートした場合は、同じ名前の既存のテーブルあるいはその他のオブジェクトは自動的に置き換わります。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p108">The name of the imported, exported, or linked table, select query, or Access object in the destination database. For some types of databases, such as FoxPro, Paradox, or dBASE, this is a file name. Include the file name extension (such as .dbf) in the file name. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument and <strong>Table</strong> in the <strong>Object Type</strong> argument, Access creates a new table containing the data in the imported table. If you import a table or other object, Access adds a number to the name if it conflicts with an existing name. For example, if you import Employees and Employees already exists, Access renames the imported table or other object Employees1. If you export to an Access database or another database, Access automatically replaces any existing table or other object that has the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="baaf4-156"><strong>Structure Only/テーブル構造のみ変換</strong></span><span class="sxs-lookup"><span data-stu-id="baaf4-156"><strong>Structure Only</strong></span></span></p></td>
<td><p><span data-ttu-id="baaf4-p109">データベース テーブルの構造のみ (データを除く) をインポートまたはエクスポートするかどうかを指定します。[ <strong>はい</strong>] または [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>いいえ</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="baaf4-p109">Specifies whether to import or export only the structure of a database table without any of its data. Select <strong>Yes</strong> or <strong>No</strong>. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="baaf4-160">注釈</span><span class="sxs-lookup"><span data-stu-id="baaf4-160">Remarks</span></span>

<span data-ttu-id="baaf4-p110">Access のデータベースと他のデータベースの間で、テーブルのインポートやエクスポートを行うことができます。また、Access の選択クエリを他のデータベースにエクスポートすることもできます。クエリの結果セットはテーブルとしてエクスポートされます。Access のデータベース間では、Access のあらゆるデータベース オブジェクトをインポートまたはエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="baaf4-p110">You can import and export tables between Access and other types of databases. You can also export Access select queries to other types of databases. Access exports the result set of the query in the form of a table. You can import and export any Access database object if both databases are Access databases.</span></span>

<span data-ttu-id="baaf4-p111">他の Access のデータベース (.mdb または .accdb) から、そのデータベース内でリンクされているテーブルをインポートした場合は、インポート後もリンクが維持されます。つまり、テーブル自体ではなく、リンクがインポートされます。</span><span class="sxs-lookup"><span data-stu-id="baaf4-p111">If you import a table from another Access database (.mdb or .accdb) that's a linked table in that database, it will still be linked after you import it. That is, the link is imported, not the table itself.</span></span>

<span data-ttu-id="baaf4-p112">アクセスしようとしているデータベースでパスワードが要求される場合は、マクロの実行時に表示されるダイアログ ボックスにパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="baaf4-p112">If the database you're accessing requires a password, a dialog box appears when you run the macro. Type the password in this dialog box.</span></span>

<span data-ttu-id="baaf4-p113">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span><span class="sxs-lookup"><span data-stu-id="baaf4-p113">The **ImportExportData** action is similar to the commands on the **External Data** tab, under **Import** or **Export**. You can use these commands to select a source of data, such as an Access database or another type of database, a spreadsheet, or a text file. If you select a database, one or more dialog boxes appear in which you select the type of object to import or export (for Access databases), the name of the object, and other options, depending on the database you are importing from or exporting or linking to. The arguments for the **ImportExportData** action reflect the options in these dialog boxes.</span></span>

<span data-ttu-id="baaf4-173">リンクする dBASE テーブルにインデックス情報を指定する場合は、まず、次の手順でテーブルをリンクします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-173">If you want to supply index information for a linked dBASE table, first link the table:</span></span>

1.  <span data-ttu-id="baaf4-174">[ **dBASE ファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-174">Click **dBASE File**.</span></span>

2.  <span data-ttu-id="baaf4-175">[ **外部データの取り込み**] ダイアログ ボックスで、[ **ファイル名**] ボックスに dBASE ファイルのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="baaf4-175">In the **Get External Data** dialog box, enter the path for the dBASE file in the **File name** box.</span></span>

3.  <span data-ttu-id="baaf4-176">[ **リンク テーブルを作成してソース データにリンクする**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="baaf4-176">Click **Link to the data source by creating a linked table**, then click **OK**.</span></span>

4.  <span data-ttu-id="baaf4-p114">このコマンドのダイアログ ボックスでインデックスを指定します。インデックス情報は、Microsoft Office フォルダーにある特別な情報 (.inf) ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="baaf4-p114">Specify the indexes in the dialog boxes for this command. Access stores the index information in a special information (.inf) file, located in the Microsoft Office folder.</span></span>

5.  <span data-ttu-id="baaf4-179">この時点で、リンク テーブルへのリンクを削除できます。</span><span class="sxs-lookup"><span data-stu-id="baaf4-179">You can then delete the link to the linked table.</span></span>

<span data-ttu-id="baaf4-180">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span><span class="sxs-lookup"><span data-stu-id="baaf4-180">The next time you use the **ImportExportData** action to link this dBASE table, Access uses the index information that you've specified.</span></span>

> [!NOTE]
> <span data-ttu-id="baaf4-181">[!メモ] リンクしたテーブルに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="baaf4-181">If you query or filter a linked table, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="baaf4-182">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="baaf4-182">To run the **ImportExportData** action in a Visual Basic for Applications (VBA) module, use the **TransferDatabase** method of the **DoCmd** object.</span></span>

