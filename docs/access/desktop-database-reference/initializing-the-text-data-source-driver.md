---
title: テキスト データ ソース ドライバーを初期化しています。
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709139"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="81807-102">テキスト データ ソース ドライバーを初期化しています。</span><span class="sxs-lookup"><span data-stu-id="81807-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="81807-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="81807-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81807-104">両方のデータ ソースのテキストと HTML データ ソースは、同じデータベース ドライバーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="81807-105">テキスト データ ソースのデータベース ドライバーをインストールすると、セットアップ プログラムは、一連の既定値をエンジンと ISAM 形式のサブキーで、Microsoft Windows レジストリに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="81807-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="81807-106">これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="81807-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="81807-107">次のセクションでは、初期設定とテキスト データ ソースのデータベース ドライバーの ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="81807-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="81807-108">テキスト データ ソースの初期設定</span><span class="sxs-lookup"><span data-stu-id="81807-108">Text data source initialization settings</span></span>

<span data-ttu-id="81807-109">**アクセス接続エンジン\\ISAM 形式\\テキスト フォルダー**のテキスト データ ファイルへの外部アクセスに使用される Acetxt.dll ドライバーの初期設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81807-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="81807-110">通常、このキーのエントリの設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="81807-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

<span data-ttu-id="81807-111">Microsoft Access データベース エンジンで使用される、Text キーのエントリを次に示します。</span><span class="sxs-lookup"><span data-stu-id="81807-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81807-112">エントリ</span><span class="sxs-lookup"><span data-stu-id="81807-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="81807-113">説明</span><span class="sxs-lookup"><span data-stu-id="81807-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81807-114">win32</span><span class="sxs-lookup"><span data-stu-id="81807-114">win32</span></span></p></td>
<td><p><span data-ttu-id="81807-p103">Acetxt.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-p103">The location of Acetxt.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="81807-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="81807-p104">列のデータ型を推測する場合にスキャンする行の数です。0 に設定した場合はファイル全体が検索されます。既定値は 25 です。値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-p104">The number of rows to be scanned when guessing the column types. If set to 0, the entire file will be searched. The default is 25. Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-123">消えて</span><span class="sxs-lookup"><span data-stu-id="81807-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="81807-p105">テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p105">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-126">文字セット</span><span class="sxs-lookup"><span data-stu-id="81807-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="81807-p106">テキスト ページの格納方法を示すインジケーターです。設定可能な値は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="81807-p106">An indicator of how text pages are stored. Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="81807-p107">ANSI - ANSI コード ページで格納します。AnsiToUnicode および UnicodeToAnsi による変換が行われます</span><span class="sxs-lookup"><span data-stu-id="81807-p107">ANSI — The ANSI code page of the machine. AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="81807-p108">OEM - OEM コード ページで格納します。OemToUnicode および UnicodeToOem による変換が行われます。</span><span class="sxs-lookup"><span data-stu-id="81807-p108">OEM — The OEM code page of the machine. OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="81807-133">Unicode - コード ページの変換は行われません。</span><span class="sxs-lookup"><span data-stu-id="81807-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="81807-p109">&lt;10 進数&gt; - 特定の文字セットのコード ページ番号です。Unicode との変換が行われます。</span><span class="sxs-lookup"><span data-stu-id="81807-p109">&lt;decimal number&gt; — The code page number of a specific character set. Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="81807-p110">既定値は ANSI です。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-p110">The default is ANSI. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-138">形式</span><span class="sxs-lookup"><span data-stu-id="81807-138">Format</span></span></p></td>
<td><p><span data-ttu-id="81807-139">TabDelimited、CSVDelimited、Delimited (&lt;1 文字&gt;) のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="81807-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="81807-140">区切り記号付きの形式で単一の文字の区切り文字は、二重引用符を除く任意の 1 文字を使用できます (&quot;)。</span><span class="sxs-lookup"><span data-stu-id="81807-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="81807-141">既定値は CSVDelimited です。</span><span class="sxs-lookup"><span data-stu-id="81807-141">The default is CSVDelimited.</span></span> <span data-ttu-id="81807-142">値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-143">拡張機能</span><span class="sxs-lookup"><span data-stu-id="81807-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="81807-p112">テキスト ベースのデータを探す場合に参照されるファイルの拡張子です。既定値は、txt、csv、tab、および asc です。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-p112">The extension of any files to be browsed when looking for text-based data. The default is txt, csv, tab, asc. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="81807-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="81807-p113">通貨フィールドをエクスポートする場合に、適切な通貨記号を追加するかどうかを示すバイナリ値です。値 01 は通貨記号を追加することを示し、値 00 は数値データのみをエクスポートすることを示します。既定値は 01 です。値の型は REG_BINARY 型です。</span><span class="sxs-lookup"><span data-stu-id="81807-p113">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported. A value of 01 indicates that the symbol is included. A value of 00 indicates that only the numeric data is exported. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="81807-153">テキスト データ ソースの ISAM 形式</span><span class="sxs-lookup"><span data-stu-id="81807-153">Text data source ISAM formats</span></span>

<span data-ttu-id="81807-154">**アクセス接続エンジン\\ISAM 形式\\テキスト**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="81807-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81807-155">エントリ名</span><span class="sxs-lookup"><span data-stu-id="81807-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="81807-156">型</span><span class="sxs-lookup"><span data-stu-id="81807-156">Type</span></span></p></th>
<th><p><span data-ttu-id="81807-157">値</span><span class="sxs-lookup"><span data-stu-id="81807-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81807-158">Engine</span><span class="sxs-lookup"><span data-stu-id="81807-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="81807-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-160">テキスト</span><span class="sxs-lookup"><span data-stu-id="81807-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="81807-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="81807-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-163">テキスト ファイル (*.txt、*.csv、\*.tab、および \*.asc)</span><span class="sxs-lookup"><span data-stu-id="81807-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="81807-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="81807-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-166">テキスト ファイル (*.txt、*.csv、\*.tab、および \*.asc)</span><span class="sxs-lookup"><span data-stu-id="81807-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="81807-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="81807-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-169">01</span><span class="sxs-lookup"><span data-stu-id="81807-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="81807-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="81807-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-172">01</span><span class="sxs-lookup"><span data-stu-id="81807-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="81807-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="81807-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="81807-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="81807-175">2</span><span class="sxs-lookup"><span data-stu-id="81807-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="81807-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="81807-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-178">00</span><span class="sxs-lookup"><span data-stu-id="81807-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="81807-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="81807-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-181">00</span><span class="sxs-lookup"><span data-stu-id="81807-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="81807-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="81807-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p114">外部ファイルのデータをカレント データベースにインポートします。カレント データベースのデータを変更しても、外部ファイルのデータは変更されません。</span><span class="sxs-lookup"><span data-stu-id="81807-p114">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="81807-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="81807-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p115">外部ファイルにリンクされているテーブルをカレント データベース内に作成します。カレント データベースのデータを変更すると、外部ファイルのデータも変更されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p115">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="81807-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="81807-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p116">カレント データベースからテキスト ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="81807-p116">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="81807-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="81807-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-196">01</span><span class="sxs-lookup"><span data-stu-id="81807-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="81807-197">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81807-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="81807-198">インポート ISAM 形式の HTML</span><span class="sxs-lookup"><span data-stu-id="81807-198">HTML import ISAM formats</span></span>

<span data-ttu-id="81807-199">**アクセス接続エンジン\\ISAM 形式\\HTML インポート**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="81807-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81807-200">エントリ名</span><span class="sxs-lookup"><span data-stu-id="81807-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="81807-201">型</span><span class="sxs-lookup"><span data-stu-id="81807-201">Type</span></span></p></th>
<th><p><span data-ttu-id="81807-202">値</span><span class="sxs-lookup"><span data-stu-id="81807-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81807-203">Engine</span><span class="sxs-lookup"><span data-stu-id="81807-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="81807-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-205">テキスト</span><span class="sxs-lookup"><span data-stu-id="81807-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="81807-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="81807-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-208">HTML ファイル (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="81807-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="81807-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="81807-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-211">01</span><span class="sxs-lookup"><span data-stu-id="81807-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="81807-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="81807-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-214">00</span><span class="sxs-lookup"><span data-stu-id="81807-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="81807-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="81807-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="81807-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="81807-217">2</span><span class="sxs-lookup"><span data-stu-id="81807-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="81807-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="81807-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-220">00</span><span class="sxs-lookup"><span data-stu-id="81807-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="81807-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="81807-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-223">00</span><span class="sxs-lookup"><span data-stu-id="81807-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="81807-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="81807-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p117">外部ファイルのデータをカレント データベースにインポートします。カレント データベースのデータを変更しても、外部ファイルのデータは変更されません。</span><span class="sxs-lookup"><span data-stu-id="81807-p117">Import data from the external file into the current database. Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="81807-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="81807-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p118">外部ファイルにリンクされているテーブルをカレント データベース内に作成します。カレント データベースのデータを変更すると、外部ファイルのデータも変更されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p118">Create a table in the current database that is linked to the external file. Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="81807-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="81807-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-234">01</span><span class="sxs-lookup"><span data-stu-id="81807-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="81807-235">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81807-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="81807-236">エクスポート ISAM 形式の HTML</span><span class="sxs-lookup"><span data-stu-id="81807-236">HTML export ISAM formats</span></span>

<span data-ttu-id="81807-237">**アクセス接続エンジン\\ISAM 形式\\HTML のエクスポート**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="81807-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81807-238">エントリ名</span><span class="sxs-lookup"><span data-stu-id="81807-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="81807-239">型</span><span class="sxs-lookup"><span data-stu-id="81807-239">Type</span></span></p></th>
<th><p><span data-ttu-id="81807-240">値</span><span class="sxs-lookup"><span data-stu-id="81807-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81807-241">Engine</span><span class="sxs-lookup"><span data-stu-id="81807-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="81807-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-243">テキスト</span><span class="sxs-lookup"><span data-stu-id="81807-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="81807-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="81807-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-246">HTML ファイル (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="81807-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="81807-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="81807-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-249">00</span><span class="sxs-lookup"><span data-stu-id="81807-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="81807-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="81807-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-252">01</span><span class="sxs-lookup"><span data-stu-id="81807-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="81807-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="81807-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="81807-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="81807-255">2</span><span class="sxs-lookup"><span data-stu-id="81807-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="81807-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="81807-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-258">00</span><span class="sxs-lookup"><span data-stu-id="81807-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="81807-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="81807-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-261">00</span><span class="sxs-lookup"><span data-stu-id="81807-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="81807-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="81807-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="81807-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="81807-p119">カレント データベースからテキスト ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="81807-p119">Export data from the current database into a text file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="81807-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="81807-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="81807-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="81807-268">01</span><span class="sxs-lookup"><span data-stu-id="81807-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="81807-269">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81807-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="81807-270">テキストと HTML データの Schema.ini ファイルをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="81807-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="81807-p120">テキスト データと HTML データの読み取り、インポート、またはエクスポートを行うには、Schema.ini ファイルを作成してその中にテキストの ISAM 情報を追加する必要があります。Schema.ini には、テキスト ファイルの書式化方法、インポート時の読み取り方法、ファイルへの既定のエクスポート書式など、データ ソースの仕様を記述します。次の例では、固定長のファイルである Filename.txt に対するレイアウトを示しています。</span><span class="sxs-lookup"><span data-stu-id="81807-p120">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file. Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files. The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

<span data-ttu-id="81807-274">同様に、区切り記号付きファイルの書式は次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="81807-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

<span data-ttu-id="81807-275">データを区切り記号付きテキスト ファイルにエクスポートする場合は、そのファイルに対して同様に次の書式を指定します。</span><span class="sxs-lookup"><span data-stu-id="81807-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

<span data-ttu-id="81807-p121">My Special Export の例では、特定のエクスポート オプションについて説明しています。接続時にはさまざまなエクスポート オプションを指定できます。また、この最後の例は、接続時に必要に応じて渡すことのできるデータ ソース名 (DSN) にも対応しています。この 3 つの書式セクションは、すべて同じ .ini ファイルに追加できます。</span><span class="sxs-lookup"><span data-stu-id="81807-p121">The My Special Export example refers to a specific export option; you can specify any variation of export options at connect time. This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time. All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="81807-279">Microsoft Access データベース エンジンで使用される、Schema.ini のエントリを次に示します。</span><span class="sxs-lookup"><span data-stu-id="81807-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81807-280">エントリ</span><span class="sxs-lookup"><span data-stu-id="81807-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="81807-281">説明</span><span class="sxs-lookup"><span data-stu-id="81807-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81807-282">は</span><span class="sxs-lookup"><span data-stu-id="81807-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="81807-283">データの最初のレコードを列名に指定する <strong>True</strong> 、または <strong>False</strong> を設定できます。</span><span class="sxs-lookup"><span data-stu-id="81807-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-284">Format</span><span class="sxs-lookup"><span data-stu-id="81807-284">Format</span></span></p></td>
<td><p><span data-ttu-id="81807-285">TabDelimited、CSVDelimited、Delimited (&lt;1 文字&gt;)、FixedLength のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="81807-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="81807-286">Delimited ファイル書式には、二重引用符を除く任意の 1 文字に指定された区切り記号 (&quot;)。</span><span class="sxs-lookup"><span data-stu-id="81807-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="81807-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="81807-p123">Format を FixedLength に指定した場合にのみ使用します。RaggedEdge は、行を復帰改行文字で終えるようにします。RaggedEdge は、行を復帰改行文字で終えるようにします。TrueFixedLength は、各行が決まった文字数になるようにします。復帰改行文字は、行の境界には存在せず、フィールドに埋め込まれていると見なされます。この設定がない場合、既定値は RaggedEdge です。</span><span class="sxs-lookup"><span data-stu-id="81807-p123">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength. RaggedEdge allows rows to be terminated with a Carriage Return character. TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field. If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="81807-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="81807-p124">列のデータ型を推測する場合にスキャンする行の数です。0 に設定した場合はファイル全体が検索されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p124">Indicates the number of rows to be scanned when guessing the column data types. If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-295">文字セット</span><span class="sxs-lookup"><span data-stu-id="81807-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="81807-296">OEM、ANSI、UNICODE、または有効なコード ページの 10 進数の番号を設定できます。ソース ファイルの文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="81807-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="81807-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="81807-p125">日付と時刻を示す書式文字列を設定できます。このエントリは、インポートまたはエクスポート時にすべての "日付/時刻" フィールドを同じ書式で処理する場合に指定します。AM と PM を除くすべての Microsoft Jet データベース エンジンの書式がサポートされています。書式文字列を省略した場合は、Windows コントロール パネルで設定されている時刻の形式と日付の短い形式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p125">Can be set to a format string indicating dates and times. This entry should be specified if all date/time fields in the import/export are handled with the same format. All of the Microsoft Jet database engine formats except AM and PM are supported. In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="81807-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="81807-p126">テキスト ファイルの通貨数値に使われる通貨記号を示します。ドル記号 ($) や Dm などがあります。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p126">Indicates the currency symbol to be used for currency values in the text file. Examples include the dollar sign ($) and Dm. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="81807-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="81807-307">次のいずれかの値を設定できます: 空白のない通貨記号プレフィックス ($1)、空白のない通貨記号サフィックス (1$)、空白が 1 文字分ある通貨記号プレフィックス ($ 1)、Curren空白が 1 文字分ある通貨記号サフィックス (1 $)。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="81807-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="81807-p127">通貨値の端数部分の桁数を指定します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p127">Specifies the number of digits used for the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="81807-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="81807-312">次の値のいずれか: ($1) – $1 $1: $1-(1$) – 1$ 1: $ 1$ – – 1 $-$ 1 1 $-$ 1: $ – 1 1 – $ ($ 1) (1 $) この例では、ドル記号が表示されますが、実際のプログラムで適切な CurrencySymbol 値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="81807-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="81807-313">このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="81807-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="81807-p129">テキスト ファイルの通貨値を 3 桁ごとに区切る場合に使用する 1 文字の記号を示します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p129">Indicates the single-character symbol to be used for separating currency values by thousands in the text file. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="81807-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="81807-p130">通貨値の整数部分と端数部分を区切るために使用する任意の 1 文字を設定できます。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p130">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="81807-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="81807-p131">数値の整数部分と端数部分を区切るために使用する任意の 1 文字を設定できます。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p131">Can be set to any single character that is used to separate the integer from the fractional part of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="81807-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="81807-p132">数値の端数部分の桁数を示します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-p132">Indicates the number of decimal digits in the fractional portion of a number. If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="81807-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="81807-327">-1 を超え、1 未満の 10 進値の先頭に 0 を付けるかどうかを指定します。値は False (先頭に 0 を付けない) または True を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81807-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81807-328">Col1, Col2, …</span><span class="sxs-lookup"><span data-stu-id="81807-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="81807-329">読み込まれるテキスト ファイル内の列を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="81807-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="81807-330">このエントリの形式である必要があります: <em>Coln</em>=<em>columnName</em>型 [幅<em>#</em>] <em>columnName</em>: 埋め込みスペースを含む列名を引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="81807-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="81807-331"><em>タイプ</em>: ビット、バイト、短時間の長いは、10 進型、通貨、単一、二重、DateTime。</span><span class="sxs-lookup"><span data-stu-id="81807-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="81807-332">バイナリでは、OLE、テキスト、またはメモ型です。</span><span class="sxs-lookup"><span data-stu-id="81807-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="81807-333">さらに、次の ODBC テキスト ドライバー型がサポートされている: (テキストと同じ) の文字 (二重と同じ) 浮動小数点数 (短い形式と同じ) の整数 LongChar (メモ型と同じ)<em>日付の形式</em>メモ型の場合、追加の書式設定マーカー [ハイパーリンクの属性] は、Microsoft Access で Url をアクティブにする必要がある列を指定する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="81807-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="81807-334">10 進数型 (Decimal) の場合、追加の形式指定 [Scale #] または [Precision #] が使用できます。</span><span class="sxs-lookup"><span data-stu-id="81807-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81807-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="81807-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="81807-336">特殊文字を含む文字列を区切るために使用する 1 つの文字を設定できます。
</span><span class="sxs-lookup"><span data-stu-id="81807-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="81807-337">例:</span><span class="sxs-lookup"><span data-stu-id="81807-337">E.g.</span></span> <span data-ttu-id="81807-338">&quot;abc&quot;、&quot;xyz、pqr&quot;、&quot;hij&quot;既定の区切り文字は二重引用符でこのエントリが存在しない場合。</span><span class="sxs-lookup"><span data-stu-id="81807-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="81807-339">このエントリが文字列である場合&quot;なし&quot;の区切り記号として扱われる文字はないし。</span><span class="sxs-lookup"><span data-stu-id="81807-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="81807-340">[!メモ] Schema.ini ファイルの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81807-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


