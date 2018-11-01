---
title: ImportExportText マクロ アクション
TOCTitle: ImportExportText Macro Action
ms:assetid: 366fa095-6f09-7c22-e734-bfa585cfe79e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192475(v=office.15)
ms:contentKeyID: 48544171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168097
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5ded11512def101bc27dfb843d2315f9f4105fb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891227"
---
# <a name="importexporttext-macro-action"></a><span data-ttu-id="c0f6e-102">ImportExportText マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="c0f6e-102">ImportExportText Macro Action</span></span>

<span data-ttu-id="c0f6e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0f6e-104">**ImportExportText**アクションは、インポートまたはエクスポートする現在の Microsoft Access データベース (.mdb または .accdb) または Access プロジェクト (.adp) とテキスト ファイルの間のテキストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-104">You can use the **ImportExportText** action to import or export text between the current Microsoft Access database (.mdb or .accdb) or Access project (.adp) and a text file.</span></span> <span data-ttu-id="c0f6e-105">現在の Access データベースにテキスト ファイル内のデータをリンクすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-105">You can also link the data in a text file to the current Access database.</span></span> <span data-ttu-id="c0f6e-106">リンクしたテキスト ファイルをアクセスを許可する完全なデータをワード プロセッシング プログラムの中に Access でテキスト データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-106">With a linked text file, you can view the text data with Access while still allowing complete access to the data from your word processing program.</span></span> <span data-ttu-id="c0f6e-107">インポート、エクスポート、およびリンクできますテーブルまたは HTML ファイル内のリストに (\*.html)。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-107">You can also import from, export to, and link to a table or list in an HTML file (\*.html).</span></span>

> [!NOTE]
> <span data-ttu-id="c0f6e-108">テキスト ファイルまたは HTML ファイルのデータにリンクする場合、Access ではデータが読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-108">If you link to data in a text file or an HTML file, the data is read-only in Access.</span></span>
> 
> <span data-ttu-id="c0f6e-109">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-109">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="c0f6e-110">設定</span><span class="sxs-lookup"><span data-stu-id="c0f6e-110">Setting</span></span>

<span data-ttu-id="c0f6e-111">**ImportExportText** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-111">The **ImportExportText** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0f6e-112">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="c0f6e-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c0f6e-113">説明</span><span class="sxs-lookup"><span data-stu-id="c0f6e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0f6e-114"><strong>Transfer Type/変換の種類</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-115">変換の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-115">The type of transfer you want to make.</span></span> <span data-ttu-id="c0f6e-116">インポート、エクスポート、または区切り記号付きまたは固定長テキスト ファイルまたは HTML ファイルのデータにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-116">You can import data from, export data to, or link to data in delimited or fixed-width text files or HTML files.</span></span> <span data-ttu-id="c0f6e-117">定型書簡や宛名ラベルなどの差し込み文書を作成するのには Word の差し込み印刷機能を使用することができます、Microsoft Word の差し込み印刷のデータ ファイルにデータをエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-117">You can also export data to a Microsoft Word mail merge data file, which you can then use with the Word mail merge feature to create merged documents such as form letters and mailing labels.</span></span> <span data-ttu-id="c0f6e-118"><strong>インポートの区切り</strong><strong>インポートの幅を固定する</strong>、 <strong>HTML をインポート</strong>、<strong>区切り記号付きエクスポート</strong>、<strong>固定長エクスポート</strong> <strong>HTML をエクスポートする</strong>、 <strong>Windows の印刷用の Word にエクスポート</strong><strong>リンクの区切り</strong>を、選択して<strong>のリンクの幅を固定します。</strong>、または [マクロ ビルダー] ウィンドウの [<strong>転送の種類</strong>] ボックス、[<strong>アクションの引数</strong>] セクションで [<strong>リンクの HTML</strong>です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-118">Select <strong>Import Delimited</strong>, <strong>Import Fixed Width</strong>, <strong>Import HTML</strong>, <strong>Export Delimited</strong>, <strong>Export Fixed Width</strong>, <strong>Export HTML</strong>, <strong>Export Word for Windows Merge</strong>, <strong>Link Delimited</strong>, <strong>Link Fixed Width</strong>, or <strong>Link HTML</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="c0f6e-119">既定では、<strong>インポートの区切りです</strong>。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-119">The default is <strong>Import Delimited</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="c0f6e-120">Access プロジェクト (.adp) でサポートされている変換の種類は、[<STRONG>区切り記号付きインポート</STRONG>]、[<STRONG>固定長インポート</STRONG>]、[<STRONG>区切り記号付きエクスポート</STRONG>]、[<STRONG>固定長エクスポート</STRONG>]、または [<STRONG>Word 差し込みデータ エクスポート</STRONG>] だけです。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-120">Only <STRONG>Import Delimited</STRONG>, <STRONG>Import Fixed Width</STRONG>, <STRONG>Export Delimited</STRONG>, <STRONG>Export Fixed Width</STRONG>, or <STRONG>Export Word for Windows Merge</STRONG> transfer types are supported in an Access project (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0f6e-121"><strong>Specification Name/定義名</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-121"><strong>Specification Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-p103">テキスト ファイルをインポートまたはリンクする方法を決定するオプション セットの定義名を指定します。固定幅テキスト ファイルの場合、引数を指定するか、インポートまたはリンクするテキスト ファイルと同じフォルダーにある schema.ini ファイルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-p103">The specification name for the set of options that determines how a text file is imported or linked. For a fixed-width text file, you must either specify an argument or use a schema.ini file, which must be stored in the same folder as the imported or linked text file.</span></span></p>
<p><span data-ttu-id="c0f6e-124">テキスト ファイルをインポートまたはリンクするための定義を作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-124">To create a specification for importing or linking a text file:</span></span></p>
<ol>
<li><p><span data-ttu-id="c0f6e-125">[<strong>外部データの取り込み</strong>] ダイアログ ボックスで、[<strong>ファイル名</strong>] ボックスにソース テキスト ファイルのパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-125">In the <strong>Get External Data</strong> dialog box, enter the path of the source text file in the <strong>File name</strong> box.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-126">データの格納に必要なオプション (インポート、追加、またはリンク) をクリックし、[<strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-126">Click the option you want for storing the data (import, append, or link), and click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-127">[<strong>テキスト インポート ウィザード</strong>] ダイアログ ボックスの [<strong>設定</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-127">In the <strong>Import Text Wizard</strong> dialog box, click <strong>Advanced</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-128">この定義に必要なオプションを指定し、[<strong>名前を付けて保存</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-128">Specify the options you want for this specification, then click <strong>Save As</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-129">この定義の名前を入力し、[<strong>OK</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-129">Enter the name you want for the specification, then click <strong>OK</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-130">定義のダイアログ ボックスで [<strong>定義</strong>] をクリックすると、既存の定義を管理できます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-130">You can manage existing specifications by clicking <strong>Specs</strong> in the specification dialog box.</span></span></p></li>
<li><p><span data-ttu-id="c0f6e-131">[<strong>OK</strong>] をクリックして定義のダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-131">Click <strong>OK</strong> to close the specification dialog box.</span></span></p></li>
</ol>
<p></p>
<p><span data-ttu-id="c0f6e-132">次に、この引数に設定済みの定義名を入力すると、その定義に対応する形式のテキスト ファイルをインポートまたはエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-132">You can then type the specification name in this argument whenever you want to import or export the same type of text file.</span></span> <span data-ttu-id="c0f6e-133">インポート、エクスポート、または、この引数に定義名を入力しなくても区切り記号付きテキスト ファイルをリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-133">You can import, export, or link delimited text files without typing a specification name for this argument.</span></span> <span data-ttu-id="c0f6e-134">この例では、ウィザードのダイアログ ボックスの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-134">In this case, Access uses the defaults from the wizard dialog box.</span></span> <span data-ttu-id="c0f6e-135">これまででは、これらの種類のファイルをエクスポートする場合、この引数に定義名を入力する必要はありませんので、差し込み印刷データ ファイルの定義済みの形式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-135">Access uses a predetermined format for mail merge data files, so you don't ever need to type a specification name for this argument when you export these types of files.</span></span> <span data-ttu-id="c0f6e-136">HTML ファイルでは、インポート/エクスポート定義を使用することができますが、部分のみが適用される仕様は、データ型の書式の仕様です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-136">You can use import/export specifications with HTML files, but the only part of the specification that applies is the specification for data type formatting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0f6e-137"><strong>Table Name/テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-137"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-138">テキスト データをテキスト データのエクスポートまたはリンクするテキスト データをインポートするのには Access のテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-138">The name of the Access table to import text data to, export text data from, or link text data to.</span></span> <span data-ttu-id="c0f6e-139">データをエクスポートする Access クエリの名前を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-139">You can also type the name of the Access query you want to export data from.</span></span> <span data-ttu-id="c0f6e-140">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-140">This is a required argument.</span></span> <span data-ttu-id="c0f6e-141"><strong>インポートで区切られた</strong>、<strong>固定幅のインポート</strong>または<strong>転送の種類</strong>] ボックスで、 <strong>HTML のインポート</strong>をクリックするとアクセスはテーブルが既に存在する場合、このテーブルにテキスト データを追加します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-141">If you click <strong>Import Delimited</strong>, <strong>Import Fixed Width</strong>, or <strong>Import HTML</strong> in the <strong>Transfer Type</strong> box, Access appends the text data to this table if the table already exists.</span></span> <span data-ttu-id="c0f6e-142">それ以外の場合、テキスト データを含む新しいテーブルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-142">Otherwise, Access creates a new table containing the text data.</span></span> <span data-ttu-id="c0f6e-143"><strong>ImportExportText</strong>アクションを使用しているときにエクスポートするデータを指定するのには、SQL ステートメントを使うことはできません。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-143">You can't use an SQL statement to specify data to export when you are using the <strong>ImportExportText</strong> action.</span></span> <span data-ttu-id="c0f6e-144">SQL ステートメントを使うのではなく、クエリを作成してから、 <strong>Table Name/テーブル名</strong> 引数にそのクエリの名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-144">Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0f6e-145"><strong>ファイル名</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-145"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-146">インポート元、エクスポート先、またはリンクするテキスト ファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-146">The name of the text file to import from, export to, or link to.</span></span> <span data-ttu-id="c0f6e-147">ファイル名が既存のワークシートの名前と同じ場合、既存のワークシートが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-147">Include the full path.</span></span> <span data-ttu-id="c0f6e-148">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-148">This is a required argument.</span></span> <span data-ttu-id="c0f6e-149">アクセスからデータをエクスポートするときに、新しいテキスト ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-149">Access creates a new text file when you export data from Access.</span></span> <span data-ttu-id="c0f6e-150">ファイル名が既存のテキスト ファイルの名前と同じ場合は、アクセスには、既存のテキスト ファイルが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-150">If the file name is the same as the name of an existing text file, Access replaces the existing text file.</span></span> <span data-ttu-id="c0f6e-151">特定のテーブルまたはリストを HTML ファイルにインポートまたはリンクする場合は、 <strong>HTML テーブルの Name</strong>引数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-151">If you want to import or link a particular table or list in an HTML file, you can use the <strong>HTML Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0f6e-152"><strong>Has Field Names/フィールド名の設定</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-152"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-153">テキスト ファイルの最初の行にフィールドの名前が含まれているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-153">Specifies whether the first row of the text file contains the names of the fields.</span></span> <span data-ttu-id="c0f6e-154"><strong>[はい]</strong>を選択した場合に使用されます名この行 Access テーブルのフィールド名としてインポートまたはテキスト データをリンクする場合。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-154">If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the text data.</span></span> <span data-ttu-id="c0f6e-155">[ <strong>いいえ</strong>] を選択した場合は、先頭行が通常のデータ行として処理されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-155">If you select <strong>No</strong>, Access treats the first row as a normal row of data.</span></span> <span data-ttu-id="c0f6e-156">既定値は [ <strong>いいえ</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-156">The default is <strong>No</strong>.</span></span> <span data-ttu-id="c0f6e-157">この引数は、先頭行に必ずフィールド名を含む Word の差し込みデータ ファイルに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-157">Access ignores this argument for Word for Windows mail merge data files because the first row must contain the field names.</span></span> <span data-ttu-id="c0f6e-158">この引数に [<strong>はい</strong>] を指定した場合、Access のテーブルまたは選択クエリを区切り記号付きテキスト ファイルや固定幅テキスト ファイルにエクスポートすると、テーブルまたは選択クエリのフィールド名がテキスト ファイルの先頭行に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-158">When you export an Access table or select query to a delimited or fixed-width text file, Access inserts the field names of your table or select query into the first row of the text file if you've selected <strong>Yes</strong> for this argument.</span></span> <span data-ttu-id="c0f6e-159">インポートするか、固定幅テキスト ファイルとリンク [<strong>はい]</strong>このボックスに、フィールド名を含む最初の行はそのインポート/エクスポート定義されている区切り記号をフィールド名の区切りに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-159">If you are importing or linking a fixed-width text file and select <strong>Yes</strong> in this box, the first row containing the field names must use the field delimiter set in the import/export specification to separate the field names.</span></span> <span data-ttu-id="c0f6e-160">固定幅テキスト ファイルをエクスポートして、この引数に<strong>[はい]</strong>を選択すると場合、は、この区切り記号を含むテキスト ファイルの最初の行にフィールド名が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-160">If you are exporting to a fixed-width text file and select <strong>Yes</strong> for this argument, Access inserts the field names into the first row of the text file with this delimiter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0f6e-161"><strong>HTML Table Name/HTML テーブル名</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-161"><strong>HTML Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-162">テーブルまたはリストをインポートまたはリンクする HTML ファイル内の名前です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-162">The name of the table or list in the HTML file that you want to import or link.</span></span> <span data-ttu-id="c0f6e-163"><strong>転送の型</strong>引数は、HTML のインポートまたはリンクの HTML に設定されていない限り、この引数は無視されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-163">This argument is ignored unless the <strong>Transfer Type</strong> argument is set to Import HTML or Link HTML.</span></span> <span data-ttu-id="c0f6e-164">この引数を空白のままにすると、HTML ファイル内の最初のテーブルまたはリストがインポートまたはリンクされます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-164">If you leave this argument blank, the first table or list in the HTML file is imported or linked.</span></span> <span data-ttu-id="c0f6e-165">HTML ファイル内のテーブルまたはリストの名前は、指定した文字列によって決定されます、&lt;キャプション&gt;がある場合に、タグ付け、&lt;キャプション&gt;タグです。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-165">The table or list name in the HTML file is determined by the text specified by the &lt;CAPTION&gt; tag, if there's a &lt;CAPTION&gt; tag.</span></span> <span data-ttu-id="c0f6e-166">&lt;CAPTION&gt; タグが存在しない場合、この名前は &lt;TITLE&gt; タグで指定されたテキストによって決まります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-166">If there's no &lt;CAPTION&gt; tag, the name is determined by the text specified by the &lt;TITLE&gt; tag.</span></span> <span data-ttu-id="c0f6e-167">1 つ以上のテーブルまたはリストの名前が同じ場合、それぞれの名前の末尾に番号を追加することによって区別されます。たとえば、社員 1 と社員 2 になります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-167">If more than one table or list has the same name, Access distinguishes them by adding a number to the end of each name; for example, Employees1 and Employees2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0f6e-168"><strong>コード ページ</strong></span><span class="sxs-lookup"><span data-stu-id="c0f6e-168"><strong>Code Page</strong></span></span></p></td>
<td><p><span data-ttu-id="c0f6e-169">コード ページで使用する文字セットの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-169">The name of the character set used with the code page.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c0f6e-170">解説</span><span class="sxs-lookup"><span data-stu-id="c0f6e-170">Remarks</span></span>

<span data-ttu-id="c0f6e-p109">Access の選択クエリのデータをテキスト ファイルにエクスポートできます。クエリの結果セットもテーブルと同じようにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-p109">You can export the data in Access select queries to text files. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="c0f6e-173">既存の Access のテーブルに追加するテキスト データは、テーブルの構造との互換性が必要です。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-173">Text data that you append to an existing Access table must be compatible with the table's structure.</span></span>

- <span data-ttu-id="c0f6e-174">テキストの各フィールドのデータ型は、テーブルの対応するフィールドのデータ型と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-174">Each field in the text must be of the same data type as the corresponding field in the table.</span></span>

- <span data-ttu-id="c0f6e-175">フィールドは同じ順序にする必要があります (ただし、**Has Field Names/フィールド名の設定**引数を [**はい**] に設定した場合は、テキストのフィールド名とテーブルのフィールド名を同じにする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-175">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the text must match the field names in the table).</span></span>

<span data-ttu-id="c0f6e-176">このアクションの動作は、[**外部データ**] タブの [**インポート**] または [**エクスポート**] で [**テキスト ファイル**] をクリックした場合の動作と同じです。**ImportExportText** アクションの引数は、[**テキスト ファイル**] コマンドで開始するウィザードのオプションに対応しています。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-176">This action is similar to clicking **Text File** in the **Import** or **Export** group on the **External Data** tab. The arguments of the **ImportExportText** action reflect the options in the wizard started by the **Text File** command.</span></span>

> [!TIP]
> <span data-ttu-id="c0f6e-p110">インポート定義およびエクスポート定義には、テキスト ファイルをインポート、エクスポート、またはリンクするのに必要な情報が保存されます。保存した定義は、同じ形式のテキスト ファイルをインポート、エクスポート、またはリンクする際に使用できます。たとえば、毎週の売上高をメインフレーム コンピューターから取り出してテキスト ファイルに変換するとします。このような変換の定義を作成して保存しておくと、この定義を使っていつでも Access データベースにデータを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-p110">An import/export specification stores the information Access needs to import, export, or link a text file. You can use stored specifications to import, export, or link text data from or to similar text files. For example, you might receive weekly sales figures in a text file from a mainframe computer. You can create and save a specification for this type of data and then use the specification whenever you add this data to your Access database.</span></span>

> [!NOTE]
> <span data-ttu-id="c0f6e-181">リンクしたテキスト ファイルに対してクエリを実行するか、フィルターを適用する場合は、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-181">If you query or filter a linked text file, the query or filter is case-sensitive.</span></span>

<span data-ttu-id="c0f6e-182">Visual Basic for Applications (VBA) モジュールで **ImportExportText** アクションを実行するには、**DoCmd** オブジェクトの **TransferText** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c0f6e-182">To run the **ImportExportText** action in a Visual Basic for Applications (VBA) module, use the **TransferText** method of the **DoCmd** object.</span></span>

