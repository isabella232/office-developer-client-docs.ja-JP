---
title: ExportWithFormatting マクロ アクション
TOCTitle: ExportWithFormatting Macro Action
ms:assetid: 8926dfa3-bf11-30ab-0f85-46f0a4961784
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197066(v=office.15)
ms:contentKeyID: 48546152
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm159503
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8a0ca9d2dde2ae5d39fb9159655f37b5140eee3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868021"
---
# <a name="exportwithformatting-macro-action"></a><span data-ttu-id="2d925-102">ExportWithFormatting マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2d925-102">ExportWithFormatting Macro Action</span></span>


<span data-ttu-id="2d925-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2d925-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d925-104">**ExportWithFormatting** アクションを使用すると、指定した Microsoft Access データベース オブジェクト (データシート、フォーム、レポート、モジュール、またはデータ アクセス ページ) のデータを複数の出力形式で出力できます。</span><span class="sxs-lookup"><span data-stu-id="2d925-104">You can use the **ExportWithFormatting** action to output the data in the specified Microsoft Access database object (a datasheet, form, report, module, or data access page) to several output formats.</span></span>

## <a name="settings"></a><span data-ttu-id="2d925-105">設定値</span><span class="sxs-lookup"><span data-stu-id="2d925-105">Settings</span></span>

<span data-ttu-id="2d925-106">**ExportWithFormatting** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2d925-106">The **ExportWithFormatting** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d925-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="2d925-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2d925-108">説明</span><span class="sxs-lookup"><span data-stu-id="2d925-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d925-109"><strong>Object Type/オブジェクトの種類</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-p101">出力するデータが格納されているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスで、[ <strong>テーブル</strong>] (テーブルのデータシートの場合)、[ <strong>クエリ</strong>] (クエリのデータシートの場合)、[ <strong>フォーム</strong>] (フォームまたはフォームのデータシートの場合)、[ <strong>レポート</strong>]、[ <strong>モジュール</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ストアド プロシージャ</strong>]、または [ <strong>関数</strong>] をクリックします。マクロは出力できません。アクティブ オブジェクトを出力する場合は、この引数でオブジェクトの種類を選択し、 <strong>Object Name/オブジェクト名</strong> 引数は指定しません。この引数は省略できません。既定値は [ <strong>テーブル</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="2d925-p101">The type of object containing the data to output. Click <strong>Table</strong> (for a table datasheet), <strong>Query</strong> (for a query datasheet), <strong>Form</strong> (for a form or form datasheet), <strong>Report</strong>, <strong>Module</strong>, <strong>Server View</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can't output a macro. If you want to output the active object, select its type with this argument, but leave the <strong>Object Name</strong> argument blank. This is a required argument. The default is <strong>Table</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d925-116"><strong>Object Name/オブジェクト名</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-p102">出力するデータが格納されているオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。ライブラリ データベースで <strong>ExportWithFormatting</strong> アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </span><span class="sxs-lookup"><span data-stu-id="2d925-p102">The name of the object containing the data to output. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you run a macro containing the <strong>ExportWithFormatting</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d925-120"><strong>Output Format/出力ファイル形式</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-120"><strong>Output Format</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-121">データの出力に使用するファイル形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d925-121">The type of format you want to use to output the data.</span></span> <span data-ttu-id="2d925-122"><strong>Excel 97 - 2003年ブック (*.xls)</strong>、 <strong>Excel バイナリ ブック (*.xlsb)</strong>、 <strong>Excel ブック (*.xlsx)</strong>を選択することができます<strong>HTML (*.htm \* .html)</strong>、 <strong>Microsoft Excel 5.0/95 ブック (*.xls)</strong>、 <strong>PDF 形式 (ロールバック)</strong>、 <strong>リッチ テキスト形 (式 *.rtf)</strong>、<strong>テキスト ファイル (*.txt)</strong>、または<strong>XPS 形式 (*.xps)</strong>。</span><span class="sxs-lookup"><span data-stu-id="2d925-122">You can select <strong>Excel 97 - Excel 2003 Workbook (*.xls)</strong>, <strong>Excel Binary Workbook (*.xlsb)</strong>, <strong>Excel Workbook (*.xlsx)</strong>, <strong>HTML (*.htm; *.html)</strong>, <strong>Microsoft Excel 5.0/95 Workbook (*.xls)</strong>, <strong>PDF Format (*.pdf)</strong>, <strong>Rich Text Format (*.rtf)</strong>, <strong>Text Files (*.txt)</strong>, or <strong>XPS Format (*.xps)</strong>.</span></span> <span data-ttu-id="2d925-123">この引数を指定しないと、出力形式を確認するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d925-123">If you leave this argument blank, Access prompts you for the output format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d925-124"><strong>Output File/出力ファイル</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-124"><strong>Output File</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-p104">データの出力先となるファイルを、完全パスを含めて指定します。 <strong>Output Format出力ファイル形式</strong> 引数で選択した出力ファイル形式の標準のファイル名拡張子を含めることができますが、この拡張子は省略できます。 <strong>Output File/出力ファイル</strong> 引数を指定しないと、出力ファイル名を確認するダイアログ ボックスが表示されます。  </span><span class="sxs-lookup"><span data-stu-id="2d925-p104">The file to which you want to output the data, including the full path. You can include the standard file name extension for the output format you select with the <strong>Output Format</strong> argument, but it is not required. If you leave the <strong>Output File</strong> argument blank, Access prompts you for an output file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d925-128"><strong>Auto Start/自動起動</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-128"><strong>Auto Start</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-129"><strong>ExportWithFormatting</strong> アクションを実行した直後に適切なソフトウェアを起動して、 <strong>Output File/出力ファイル</strong> 引数で指定したファイルを開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2d925-129">Specifies whether you want the appropriate software to start immediately after the <strong>ExportWithFormatting</strong> action runs, with the file specified by the <strong>Output File</strong> argument opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d925-130"><strong>Template File/テンプレート ファイル</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-130"><strong>Template File</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-p105">HTML ファイルのテンプレートとして使用するファイルのパスとファイル名を指定します。テンプレート ファイルとは、Access に固有の HTML タグおよびトークンを含むテキスト ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2d925-p105">The path and file name of a file you want to use as a template for HTML files. The template file is a text file that includes HTML tags and tokens that are unique to Access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d925-133"><strong>Encoding/エンコード</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-133"><strong>Encoding</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-p106">テキストまたは HTML データを出力する際に使用する文字エンコード形式の種類を指定します。[ <strong>MS-DOS</strong>]、[ <strong>Unicode</strong>]、または [ <strong>Unicode (UTF-8)</strong>] を選択できます。引数の設定値 [ <strong>MS-DOS</strong>] は、テキスト ファイルの場合にのみ選択できます。この引数を指定しない場合、テキスト ファイルに対しては Windows の既定のエンコード方法を使用し、HTML ファイルに対してはシステムの既定のエンコード方法を使用して、データが出力されます。  </span><span class="sxs-lookup"><span data-stu-id="2d925-p106">The type of character encoding format you want used to output the text or HTML data. You can select <strong>MS-DOS</strong>, <strong>Unicode</strong>, or <strong>Unicode (UTF-8)</strong>. The <strong>MS-DOS</strong> argument setting is available only for text files. If you leave this argument blank, Access outputs the data by using the Windows default encoding for text files and the default system encoding for HTML files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d925-138"><strong>Output Quality/出力品質</strong></span><span class="sxs-lookup"><span data-stu-id="2d925-138"><strong>Output Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="2d925-139">印刷の出力を最適化する場合は [ <strong>印刷</strong>]、画面上に表示する出力を最適化する場合は [ <strong>スクリーン</strong>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d925-139">Select <strong>Print</strong> to optimize the output for printing, or <strong>Screen</strong> to optimize the output for display on a screen.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2d925-140">解説</span><span class="sxs-lookup"><span data-stu-id="2d925-140">Remarks</span></span>

<span data-ttu-id="2d925-p107">Access のデータは形式を指定して出力すると、同じ形式を使用するプログラムでそのまま読み取ることができます。たとえば、Access のレポートをリッチ テキスト形式の文書に出力すると、その文書を Microsoft Word で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="2d925-p107">The Access data is output in the selected format and can be read by any program that uses the same format. For example, you can output an Access report with its formatting to a Rich Text Format document and then open the document in Microsoft Word.</span></span>

<span data-ttu-id="2d925-p108">データベース オブジェクトを HTML 形式で出力すると、そのオブジェクトのデータを含む HTML 形式のファイルが作成されます。 **Template File/テンプレート ファイル** 引数を使用すると, .html ファイルのテンプレートとして使用するファイルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2d925-p108">If you output the database object to HTML format, Access creates a file in HTML format containing the data from the object. You can use the **Template File** argument to specify a file to be used as a template for the .html file.</span></span>

<span data-ttu-id="2d925-145">**ExportWithFormatting** アクションを使用してデータベース オブジェクトをいずれかの出力形式で出力する場合は、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="2d925-145">The following rules apply when you use the **ExportWithFormatting** action to output a database object to any of the output formats:</span></span>

  - <span data-ttu-id="2d925-p109">テーブル、クエリ、およびフォームの各データシートのデータを出力できます。出力ファイルには、OLE オブジェクトが含まれているフィールドを除き、データシートのすべてのフィールドがそのまま出力されます。OLE オブジェクトが含まれているフィールドの列もファイルに出力されますが、そのフィールド値は空白になります。</span><span class="sxs-lookup"><span data-stu-id="2d925-p109">You can output data in table, query, and form datasheets. In the output file, all fields in the datasheet appear as they do in Access, with the exception of fields containing OLE objects. The columns for OLE object fields are included in the output file, but the fields are blank.</span></span>

  - <span data-ttu-id="2d925-149">はい/いいえ型フィールドにバインドされているコントロール (トグル ボタン、オプション ボタン、またはチェック ボックスをオン)、出力ファイルには-1 (Yes) または 0 (No) の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d925-149">For a control that is bound to a Yes/No field (a toggle button, option button, or check box), the output file displays the value –1 (Yes) or 0 (No).</span></span>

  - <span data-ttu-id="2d925-150">ハイパーリンク型のフィールドに連結されたテキスト ボックスの場合、出力ファイルには MS-DOS テキストを除くすべての出力形式のハイパーリンクが表示されます (MS-DOS テキストの場合、ハイパーリンクは通常のテキストとして表示されます)。</span><span class="sxs-lookup"><span data-stu-id="2d925-150">For a text box bound to a Hyperlink field, the output file displays the hyperlink for all output formats with the exception of MS-DOS text (in this case, the hyperlink is displayed as normal text).</span></span>

  - <span data-ttu-id="2d925-151">フォーム ビューに表示されたフォームのデータを出力する場合、出力ファイルには常にフォームのデータシート ビューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2d925-151">If you output the data in a form in Form view, the output file always contains the form's Datasheet view.</span></span>

  - <span data-ttu-id="2d925-p110">データシート、フォーム、またはデータ アクセス ページを HTML 形式で出力する場合は, .html ファイルが 1 つ作成されます。レポートを HTML 形式で出力する場合は、レポートのページごとに .html ファイルが 1 つずつ作成されます。</span><span class="sxs-lookup"><span data-stu-id="2d925-p110">When you output a datasheet, form, or data access page in HTML format, one .html file is created. When you output a report in HTML format, one .html file is created for each page in the report.</span></span>

<span data-ttu-id="2d925-154">**ExportWithFormatting** アクションの実行結果は、[ **外部データ**] タブの [ **エクスポート**] にあるオプションのいずれかをクリックしたときと似ています。このアクションの引数は [ **エクスポート**] ダイアログ ボックスの設定に対応しています。</span><span class="sxs-lookup"><span data-stu-id="2d925-154">The result of running the **ExportWithFormatting** action is similar to clicking one of the options in the **Export** group on the **External Data** tab. The action arguments correspond to the settings in the **Export** dialog box.</span></span>

<span data-ttu-id="2d925-155">Visual Basic for Applications (VBA) モジュールで **ExportWithFormatting** アクションを実行するには、 **DoCmd** オブジェクトの **OutputTo** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d925-155">To run the **ExportWithFormatting** action in a Visual Basic for Applications (VBA) module, use the **OutputTo** method of the **DoCmd** object.</span></span>

