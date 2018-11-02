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
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="b8da1-102">ImportExportSpreadsheet マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b8da1-102">ImportExportSpreadsheet macro action</span></span>


<span data-ttu-id="b8da1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b8da1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8da1-p101">**ImportExportSpreadsheet** アクションを使用すると、カレントの Access データベース (.mdb または .accdb) または Access プロジェクト (.adp) とワークシート ファイルとの間でデータをインポートまたはエクスポートできます。Microsoft Excel のワークシートのデータを Microsoft Access のカレント データベースにリンクすることもできます。ワークシートをリンクすると、Access でワークシート データを表示したり編集することができると同時に、Excel のワークシート プログラムからそのデータにアクセスできます。Lotus 1-2-3 のワークシート ファイルのデータにもリンクできますが、そのファイルは Access では読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p101">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file. You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database. With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program. You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8da1-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="b8da1-110">設定</span><span class="sxs-lookup"><span data-stu-id="b8da1-110">Setting</span></span>

<span data-ttu-id="b8da1-111">**TransferSpreadsheet** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b8da1-111">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8da1-112">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b8da1-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b8da1-113">説明</span><span class="sxs-lookup"><span data-stu-id="b8da1-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8da1-114"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p103">変換の種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>変換の種類</strong>] ボックスで、[ <strong>インポート</strong>]、[ <strong>エクスポート</strong>]、または [ <strong>リンク</strong>] を選択します。既定値は [ <strong>インポート</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="b8da1-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b8da1-118">[<STRONG>リンク</STRONG>] は、Access プロジェクト (.adp) ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b8da1-118">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8da1-119"><strong>Spreadsheet Type/ワークシートの種類</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-119"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p104">インポート元、エクスポート先、またはリンク先のワークシートの種類を指定します。このボックスでは、多数のワークシートの種類から 1 つを選択できます。既定値は [ <strong>Excel ブック</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="b8da1-p104">The type of spreadsheet to import from, export to, or link to. You can select one of a number of spreadsheet types in the box. The default is <strong>Excel Workbook</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b8da1-p105">インポート元およびリンク (読み取り専用) 先として Lotus .WK4 ファイルを指定できますが、Access のデータをこのワークシート形式にエクスポートすることはできません。Access では、このアクションによる Lotus .WKS または Excel Version 2.0 のワークシートのデータのインポート、エクスポート、またはリンクはサポートされなくなりました。Excel Version 2.0 形式または Lotus .WKS 形式のワークシート データをインポートまたはリンクする場合は、ワークシート データを Excel または Lotus 1-2-3 の新しいバージョンに変換してから、Access にデータをインポートまたはリンクします。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p105">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format. Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action. If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8da1-126"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p106">ワークシート データのインポート先、エクスポート元、またはリンク先となる Access のテーブル名を指定します。また、データのエクスポート元として Access の選択クエリ名を入力することもできます。この引数は省略できません。 <strong>Transfer Type/変換の種類</strong> 引数で [ <strong>インポート</strong>] を選択すると、テーブルが既に存在する場合は、ワークシートのデータがこのテーブルに追加されます。テーブルが存在しない場合は、新しいテーブルが作成され、指定したワークシートのデータがインポートされます。Access では、 <strong>ImportExportSpreadsheet</strong> アクションを使用するときに、エクスポートするデータを SQL ステートメントを使って指定することができません。SQL ステートメントを使うのではなく、クエリを作成してから、 <strong>Table Name/テーブル名</strong> 引数にそのクエリの名前を指定する必要があります。  </span><span class="sxs-lookup"><span data-stu-id="b8da1-p106">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to. You can also type the name of the Access select query you want to export data from. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists. Otherwise, Access creates a new table containing the spreadsheet data. In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action. Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8da1-134"><strong>ファイル名</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-134"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p107">インポート元、エクスポート先、またはリンク先のワークシート ファイルの名前を指定します。ファイル名が既存のワークシートの名前と同じ場合、既存のワークシートが置き換えられます。この引数は省略できません。Access のデータをエクスポートすると、新しいワークシートが作成されます。ファイル名が既存のワークシートの名前と同じ場合、既存のワークシートが置き換えられます。ただし、Excel 5.0 以降のバージョンのブックをエクスポートする場合は、エクスポートされたデータがブック内の次に使用できる新しいワークシートにコピーされます。Excel 5.0 以降のバージョンのワークシートのデータをインポートまたはリンクする場合、 <strong>Range/範囲</strong> 引数を使用して特定のワークシートを指定できます。  </span><span class="sxs-lookup"><span data-stu-id="b8da1-p107">The name of the spreadsheet file to import from, export to, or link to. Include the full path. This is a required argument. Access creates a new spreadsheet when you export data from Access. If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook. In that case, Access copies the exported data to the next available new worksheet in the workbook. If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8da1-142"><strong>Has Field Names/フィールド名の設定</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-142"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p108">ワークシートの先頭行にフィールド名を含めるかどうかを指定します。[ <strong>はい</strong>] を選択した場合は、ワークシートのデータをインポートまたはリンクするときに、先頭行の名前が Access のテーブルのフィールド名として使用されます。[ <strong>いいえ</strong>] を選択した場合は、先頭行が通常のデータ行として処理されます。既定値は [ <strong>いいえ</strong>] です。Access のテーブルや選択クエリをワークシートにエクスポートした場合は、この引数の値に関係なく、ワークシートの先頭行にフィールド名が挿入されます。  </span><span class="sxs-lookup"><span data-stu-id="b8da1-p108">Specifies whether the first row of the spreadsheet contains the names of the fields. If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data. If you select <strong>No</strong>, Access treats the first row as a normal row of data. The default is <strong>No</strong>. When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8da1-148"><strong>Range/範囲</strong></span><span class="sxs-lookup"><span data-stu-id="b8da1-148"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="b8da1-p109">インポートまたはリンクするセルの範囲を指定します。この引数を指定しないと、ワークシート全体がインポートまたはリンクされます。インポートまたはリンクするワークシートの範囲名を入力するか、A1:E25 のようにセル範囲を指定することができます。Access 97 以降のバージョンでは、A1..E25 の構文は使用できないことに注意してください。Excel 5.0 以降のバージョンのワークシートのデータをインポートまたはリンクする場合は、範囲の前にワークシート名と感嘆符を付けることができます (たとえば、<ワークシート名>!A1:C7)。 



</span><span class="sxs-lookup"><span data-stu-id="b8da1-p109">The range of cells to import or link. Leave this argument blank to import or link the entire spreadsheet. You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later). If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b8da1-p110">ワークシートにエクスポートする際は、この引数を空白のままにしておきます。範囲を入力すると、エクスポートは失敗します。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p110">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b8da1-155">解説</span><span class="sxs-lookup"><span data-stu-id="b8da1-155">Remarks</span></span>

<span data-ttu-id="b8da1-p111">Access の選択クエリのデータをワークシートにエクスポートできます。クエリの結果セットもテーブルと同じようにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p111">You can export the data in Access select queries to spreadsheets. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="b8da1-158">既存の Access のテーブルに追加するワークシートのデータは、テーブルの構造との互換性が必要です。</span><span class="sxs-lookup"><span data-stu-id="b8da1-158">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

  - <span data-ttu-id="b8da1-159">ワークシートの各フィールドのデータ型は、テーブルの対応するフィールドのデータ型と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8da1-159">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

  - <span data-ttu-id="b8da1-160">フィールドは同じ順序にする必要があります (ただし、 **Has Field Names/フィールド名の設定** 引数を [ **はい**] に設定した場合は、ワークシートのフィールド名とテーブルのフィールド名を同じにする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b8da1-160">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="b8da1-p112">このアクションの動作は、[ **外部データ**] タブをクリックし、[ **インポート**] または [ **エクスポート**] で [ **Excel**] をクリックした場合や、[ **インポート**] または [ **エクスポート**] で [ **その他**] をクリックして、[ **Lotus 1-2-3 ファイル**] をクリックした場合と同じです。これらのコマンドを使用して、Access やその他のデータベース、ワークシート、またはテキスト ファイルなどの変換元のデータを選択できます。ワークシートを選択した場合は、ワークシートの名前やその他のオプションを選択する一連のダイアログ ボックス (Access のウィザード) が実行されます)。 **ImportExportSpreadsheet** アクションの引数は、このようなダイアログ ボックスやウィザードのオプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="b8da1-p112">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**. You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file. If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options. The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8da1-165">[!メモ] リンクしたワークシートに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="b8da1-165">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span></P>



<span data-ttu-id="b8da1-166">編集モードで開いている Excel ワークシートにリンクする場合は、Excel ワークシートの編集モードが終了するまで待機してから、リンクします。タイムアウトが発生することはありません。</span><span class="sxs-lookup"><span data-stu-id="b8da1-166">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="b8da1-167">Visual Basic for Applications (VBA) モジュールで **ImportExportSpreadsheet** アクションを実行するには、 **DoCmd** オブジェクトの **TransferSpreadsheet** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b8da1-167">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>

