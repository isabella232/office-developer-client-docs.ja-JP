---
title: Microsoft Office Excel ドライバーの初期化
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291436"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="75c07-102">Microsoft Office Excel ドライバーの初期化</span><span class="sxs-lookup"><span data-stu-id="75c07-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="75c07-103">**適用**対象: Excel 2016 |Access 2016 |Access 2013 |Office 2013 |Excel 2013 |Office for business Access 2013 |Excel 2010 |Access 2010</span><span class="sxs-lookup"><span data-stu-id="75c07-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="75c07-104">Excel ドライバーをインストールすると、セットアッププログラムによって、エンジンおよび ISAM 形式のサブキーに、Windows レジストリに既定値のセットが書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="75c07-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="75c07-105">これらの設定は直接変更しないでください。アプリケーションのセットアッププログラムを使用して、これらの設定を追加、削除、または変更します。</span><span class="sxs-lookup"><span data-stu-id="75c07-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="75c07-106">次のセクションでは、Microsoft Excel データベースドライバーの初期化と ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="75c07-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="75c07-107">Excel の初期化設定</span><span class="sxs-lookup"><span data-stu-id="75c07-107">Excel initialization settings</span></span>

<span data-ttu-id="75c07-108">**access Connectivity Engine Engine\\\\Excel**フォルダーには、Microsoft excel ワークシートへの外部アクセスに使用される Aceexcl ドライバーの初期化設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="75c07-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="75c07-109">通常、このキーのエントリの設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="75c07-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="75c07-110">Microsoft Access データベース エンジンで使用される、Excel キーのエントリを次に示します。</span><span class="sxs-lookup"><span data-stu-id="75c07-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75c07-111">値</span><span class="sxs-lookup"><span data-stu-id="75c07-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="75c07-112">説明</span><span class="sxs-lookup"><span data-stu-id="75c07-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75c07-113">win32</span><span class="sxs-lookup"><span data-stu-id="75c07-113">win32</span></span></p></td>
<td><p><span data-ttu-id="75c07-p103">Msexcl40.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="75c07-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="75c07-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="75c07-118">データ型を調べる行の数です。</span><span class="sxs-lookup"><span data-stu-id="75c07-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="75c07-119">データ型は、最も多いデータ型によって決められます。</span><span class="sxs-lookup"><span data-stu-id="75c07-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="75c07-120">同数の場合は、数値型 (Number)、通貨型 (Currency)、日付型 (Date)、テキスト型 (Text)、ブール型 (Boolean) の順に決められます。</span><span class="sxs-lookup"><span data-stu-id="75c07-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="75c07-121">列のデータ型に一致しないデータがある場合、そのデータは <strong>Null</strong> 値として返されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="75c07-122">インポート時に、列内に複数のデータ型が混在している場合は、その列全体が ImportMixedTypes の設定に従ってキャストされます。</span><span class="sxs-lookup"><span data-stu-id="75c07-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="75c07-123">調べる行数の既定値は 8 です。</span><span class="sxs-lookup"><span data-stu-id="75c07-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="75c07-124">値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="75c07-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="75c07-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="75c07-p105">MajorityType または Text のどちらかを設定できます。MajorityType を設定した場合、データ型が混在している列は、インポート時に最も数の多いデータ型にキャストされます。Text を設定した場合、データ型が混在している列は、インポート時にテキスト型 (Text) にキャストされます。既定値は Text です。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="75c07-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-131">append空白行</span><span class="sxs-lookup"><span data-stu-id="75c07-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="75c07-p106">Microsoft Jet 3.5 または 4.0 で、新しいデータを追加する前にワークシートの末尾に付加される空行の数です。たとえば、AppendBlankRows を 4 に設定すると、Microsoft Jet データベース エンジンはワークシートの末尾に 4 つの空行を付加してから、その後にデータのある行を付加します。このエントリには、0 ～ 16 の範囲の整数値を設定します。既定値は 01 (1 行の付加) です。値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="75c07-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="75c07-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="75c07-p107">テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</span><span class="sxs-lookup"><span data-stu-id="75c07-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="75c07-142">**access Connectivity Engine Engine\\\\Excel 8.0**フォルダーには次のエントリが含まれています。これは、Microsoft Excel 97 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75c07-143">エントリ名</span><span class="sxs-lookup"><span data-stu-id="75c07-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="75c07-144">型</span><span class="sxs-lookup"><span data-stu-id="75c07-144">Type</span></span></p></th>
<th><p><span data-ttu-id="75c07-145">値</span><span class="sxs-lookup"><span data-stu-id="75c07-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75c07-146">Engine</span><span class="sxs-lookup"><span data-stu-id="75c07-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="75c07-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75c07-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75c07-148">Excel</span><span class="sxs-lookup"><span data-stu-id="75c07-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-149">exportfilter</span><span class="sxs-lookup"><span data-stu-id="75c07-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="75c07-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75c07-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75c07-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="75c07-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-152">canlink</span><span class="sxs-lookup"><span data-stu-id="75c07-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="75c07-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75c07-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75c07-154">atl-fs-01</span><span class="sxs-lookup"><span data-stu-id="75c07-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-155">onetableperfile</span><span class="sxs-lookup"><span data-stu-id="75c07-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="75c07-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75c07-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75c07-157">+</span><span class="sxs-lookup"><span data-stu-id="75c07-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-158">isamtype</span><span class="sxs-lookup"><span data-stu-id="75c07-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="75c07-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="75c07-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="75c07-160">1-d</span><span class="sxs-lookup"><span data-stu-id="75c07-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-161">indexdialog</span><span class="sxs-lookup"><span data-stu-id="75c07-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="75c07-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75c07-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75c07-163">+</span><span class="sxs-lookup"><span data-stu-id="75c07-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-164">createdbonexport</span><span class="sxs-lookup"><span data-stu-id="75c07-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="75c07-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75c07-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75c07-166">atl-fs-01</span><span class="sxs-lookup"><span data-stu-id="75c07-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75c07-167">resulttextexport</span><span class="sxs-lookup"><span data-stu-id="75c07-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="75c07-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="75c07-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="75c07-p108">カレント データベースから Microsoft Excel 97 ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="75c07-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75c07-171">supportslongnames</span><span class="sxs-lookup"><span data-stu-id="75c07-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="75c07-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="75c07-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="75c07-173">atl-fs-01</span><span class="sxs-lookup"><span data-stu-id="75c07-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="75c07-174">Excel ドライバーの TypeGuessRows 設定を使用する</span><span class="sxs-lookup"><span data-stu-id="75c07-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="75c07-175">Microsoft Excel ドライバーを使用する場合は、 **TypeGuessRows**レジストリ値を使用して、データ型をチェックする行の数を構成できます。</span><span class="sxs-lookup"><span data-stu-id="75c07-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="75c07-176">**TypeGuessRows**の値は、次のレジストリサブキーの下にあります。</span><span class="sxs-lookup"><span data-stu-id="75c07-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016taboffice-2016"></a>[<span data-ttu-id="75c07-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="75c07-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="75c07-178">Office の MSI インストールの場合</span><span class="sxs-lookup"><span data-stu-id="75c07-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="75c07-179">32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="75c07-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="75c07-181">32ビット版 Office 用の64ビット版の Windows の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="75c07-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="75c07-183">Office のクイック実行インストールの場合</span><span class="sxs-lookup"><span data-stu-id="75c07-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="75c07-184">32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="75c07-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="75c07-186">32ビット版 Office 用の64ビット版の Windows の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="75c07-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="75c07-188">チェックする既定の行数は**8** (8) です。</span><span class="sxs-lookup"><span data-stu-id="75c07-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="75c07-189">**TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。</span><span class="sxs-lookup"><span data-stu-id="75c07-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="75c07-190">16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="75c07-191">すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="75c07-192">データ型は、検出されたデータの種類の最大数によって決まります。</span><span class="sxs-lookup"><span data-stu-id="75c07-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="75c07-193">が関連付けられている場合、データ型は次の順序で決定されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="75c07-194">番号</span><span class="sxs-lookup"><span data-stu-id="75c07-194">Number</span></span>
- <span data-ttu-id="75c07-195">通貨</span><span class="sxs-lookup"><span data-stu-id="75c07-195">Currency</span></span>
- <span data-ttu-id="75c07-196">日付</span><span class="sxs-lookup"><span data-stu-id="75c07-196">Date</span></span>
- <span data-ttu-id="75c07-197">テキスト</span><span class="sxs-lookup"><span data-stu-id="75c07-197">Text</span></span>
- <span data-ttu-id="75c07-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="75c07-198">Boolean</span></span>

<span data-ttu-id="75c07-199">列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="75c07-200">インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。</span><span class="sxs-lookup"><span data-stu-id="75c07-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013taboffice-2013"></a>[<span data-ttu-id="75c07-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="75c07-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="75c07-202">32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="75c07-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="75c07-204">32ビット版 Office 用の64ビット版の Windows の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="75c07-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="75c07-206">チェックする既定の行数は**8** (8) です。</span><span class="sxs-lookup"><span data-stu-id="75c07-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="75c07-207">**TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。</span><span class="sxs-lookup"><span data-stu-id="75c07-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="75c07-208">16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="75c07-209">すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="75c07-210">データ型は、検出されたデータの種類の最大数によって決まります。</span><span class="sxs-lookup"><span data-stu-id="75c07-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="75c07-211">が関連付けられている場合、データ型は次の順序で決定されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="75c07-212">番号</span><span class="sxs-lookup"><span data-stu-id="75c07-212">Number</span></span>
- <span data-ttu-id="75c07-213">通貨</span><span class="sxs-lookup"><span data-stu-id="75c07-213">Currency</span></span>
- <span data-ttu-id="75c07-214">日付</span><span class="sxs-lookup"><span data-stu-id="75c07-214">Date</span></span>
- <span data-ttu-id="75c07-215">テキスト</span><span class="sxs-lookup"><span data-stu-id="75c07-215">Text</span></span>
- <span data-ttu-id="75c07-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="75c07-216">Boolean</span></span>

<span data-ttu-id="75c07-217">列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="75c07-218">インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。</span><span class="sxs-lookup"><span data-stu-id="75c07-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010taboffice-2010"></a>[<span data-ttu-id="75c07-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="75c07-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="75c07-220">32ビット版の windows または64ビット版の office (64 ビット版の windows) の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="75c07-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="75c07-222">32ビット版 Office 用の64ビット版の Windows の場合:</span><span class="sxs-lookup"><span data-stu-id="75c07-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="75c07-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="75c07-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="75c07-224">チェックする既定の行数は**8** (8) です。</span><span class="sxs-lookup"><span data-stu-id="75c07-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="75c07-225">**TypeGuessRows**値を**0** (ゼロ) に設定すると、Excel ドライバーはデータ型の最初の16384行をチェックします。</span><span class="sxs-lookup"><span data-stu-id="75c07-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="75c07-226">16384を超える行数をチェックする場合は、 **TypeGuessRows**を目的の範囲に基づく値に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="75c07-227">すべての行をチェックするには、 **TypeGuessRows**を 1048576 (Excel で許可される最大行数) に設定します。</span><span class="sxs-lookup"><span data-stu-id="75c07-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="75c07-228">データ型は、検出されたデータの種類の最大数によって決まります。</span><span class="sxs-lookup"><span data-stu-id="75c07-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="75c07-229">が関連付けられている場合、データ型は次の順序で決定されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="75c07-230">番号</span><span class="sxs-lookup"><span data-stu-id="75c07-230">Number</span></span>
- <span data-ttu-id="75c07-231">通貨</span><span class="sxs-lookup"><span data-stu-id="75c07-231">Currency</span></span>
- <span data-ttu-id="75c07-232">日付</span><span class="sxs-lookup"><span data-stu-id="75c07-232">Date</span></span>
- <span data-ttu-id="75c07-233">テキスト</span><span class="sxs-lookup"><span data-stu-id="75c07-233">Text</span></span>
- <span data-ttu-id="75c07-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="75c07-234">Boolean</span></span>

<span data-ttu-id="75c07-235">列の予想されるデータ型と一致しないデータが検出された場合、そのデータは**Null**値として返されます。</span><span class="sxs-lookup"><span data-stu-id="75c07-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="75c07-236">インポート時に、列のデータ型が混在している場合は、 **ImportMixedTypes**設定によって設定されたデータ型に列全体がキャストされます。</span><span class="sxs-lookup"><span data-stu-id="75c07-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="75c07-237">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75c07-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="75c07-238">関連項目</span><span class="sxs-lookup"><span data-stu-id="75c07-238">See also</span></span>

- [<span data-ttu-id="75c07-239">Excel ドライバーの TypeGuessRows 設定を使用する</span><span class="sxs-lookup"><span data-stu-id="75c07-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

