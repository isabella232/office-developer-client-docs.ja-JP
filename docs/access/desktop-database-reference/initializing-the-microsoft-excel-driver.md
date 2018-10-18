---
title: Microsoft Office Excel ドライバーを初期化する
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7c9a3282f3bb508a4c68ecbd3f2c0465cfee9bac
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603099"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="b4188-102">Microsoft Office Excel ドライバーを初期化する</span><span class="sxs-lookup"><span data-stu-id="b4188-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="b4188-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4188-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b4188-104"><<<<<<< ヘッドと、Microsoft® Excel ドライバーをインストールすると、セットアップ プログラムは、エンジンと ISAM 形式のサブキーで、Microsoft Windows® レジストリに一連の既定値を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b4188-104"><<<<<<< HEAD When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="b4188-105">これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4188-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="b4188-106">次のセクションでは、初期化し、Microsoft Excel のデータベース ドライバーの ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="b4188-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="b4188-107">Excel の初期設定</span><span class="sxs-lookup"><span data-stu-id="b4188-107">Microsoft Excel Initialization Settings</span></span>
<span data-ttu-id="b4188-108">=== と、Excel ドライバーをインストールすると、セットアップ プログラムは、エンジンと ISAM 形式のサブキーで、Windows レジストリに一連の既定値を書き込みます。</span><span class="sxs-lookup"><span data-stu-id="b4188-108">======= When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="b4188-109">これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4188-109">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="b4188-110">次のセクションでは、初期化し、Microsoft Excel のデータベース ドライバーの ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="b4188-110">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="b4188-111">Excel の初期設定</span><span class="sxs-lookup"><span data-stu-id="b4188-111">Excel Initialization Settings</span></span>
>>>>>>> <span data-ttu-id="b4188-112">master</span><span class="sxs-lookup"><span data-stu-id="b4188-112">master</span></span>

<span data-ttu-id="b4188-113">**アクセス接続エンジン\\エンジン\\Excel**フォルダーには、Microsoft Excel ワークシートへの外部アクセスの使用、Aceexcl.dll のドライバーの初期設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4188-113">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="b4188-114">通常、このキーのエントリの設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="b4188-114">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="b4188-115">Microsoft Access データベース エンジンで使用される、Excel キーのエントリを次に示します。</span><span class="sxs-lookup"><span data-stu-id="b4188-115">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4188-116">エントリ</span><span class="sxs-lookup"><span data-stu-id="b4188-116">Entry</span></span></p></th>
<th><p><span data-ttu-id="b4188-117">説明</span><span class="sxs-lookup"><span data-stu-id="b4188-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4188-118">win32</span><span class="sxs-lookup"><span data-stu-id="b4188-118">win32</span></span></p></td>
<td><p><span data-ttu-id="b4188-p104">Msexcl40.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="b4188-p104">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-122">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="b4188-122">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="b4188-123">データ型を調べる行の数です。</span><span class="sxs-lookup"><span data-stu-id="b4188-123">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="b4188-124">検出されたデータの種類の最大数を指定したデータ型が決定されます。</span><span class="sxs-lookup"><span data-stu-id="b4188-124">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="b4188-125">データ型は次の順序で決定は、同順がある場合は、: 数値、通貨、日付、文字列、ブール値です。</span><span class="sxs-lookup"><span data-stu-id="b4188-125">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="b4188-126">列のデータ型に一致しないデータが検出された場合は<strong>Null</strong>値として返されます。</span><span class="sxs-lookup"><span data-stu-id="b4188-126">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="b4188-127">インポート時に [列のデータ型が混在している場合列全体は、ImportMixedTypes の設定に従ってキャストされます。</span><span class="sxs-lookup"><span data-stu-id="b4188-127">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="b4188-128">チェックする行の既定数は、8 です。</span><span class="sxs-lookup"><span data-stu-id="b4188-128">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="b4188-129">値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="b4188-129">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-130">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="b4188-130">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="b4188-p106">MajorityType または Text のどちらかを設定できます。MajorityType を設定した場合、データ型が混在している列は、インポート時に最も数の多いデータ型にキャストされます。Text を設定した場合、データ型が混在している列は、インポート時にテキスト型 (Text) にキャストされます。既定値は Text です。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="b4188-p106">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-136">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="b4188-136">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="b4188-p107">Microsoft Jet 3.5 または 4.0 で、新しいデータを追加する前にワークシートの末尾に付加される空行の数です。たとえば、AppendBlankRows を 4 に設定すると、Microsoft Jet データベース エンジンはワークシートの末尾に 4 つの空行を付加してから、その後にデータのある行を付加します。このエントリには、0 ～ 16 の範囲の整数値を設定します。既定値は 01 (1 行の付加) です。値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="b4188-p107">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-141">消えて</span><span class="sxs-lookup"><span data-stu-id="b4188-141">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="b4188-p108">テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</span><span class="sxs-lookup"><span data-stu-id="b4188-p108">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4188-147">**アクセス接続エンジン\\エンジン\\Excel 8.0**フォルダーには、Microsoft Excel 97 に適用されますが、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4188-147">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4188-148">エントリ名</span><span class="sxs-lookup"><span data-stu-id="b4188-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="b4188-149">種類</span><span class="sxs-lookup"><span data-stu-id="b4188-149">Type</span></span></p></th>
<th><p><span data-ttu-id="b4188-150">値</span><span class="sxs-lookup"><span data-stu-id="b4188-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4188-151">Engine</span><span class="sxs-lookup"><span data-stu-id="b4188-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="b4188-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b4188-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b4188-153">Excel</span><span class="sxs-lookup"><span data-stu-id="b4188-153">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-154">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="b4188-154">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="b4188-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b4188-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b4188-156">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="b4188-156">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="b4188-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="b4188-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4188-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b4188-159">01</span><span class="sxs-lookup"><span data-stu-id="b4188-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="b4188-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="b4188-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4188-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b4188-162">00</span><span class="sxs-lookup"><span data-stu-id="b4188-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="b4188-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="b4188-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b4188-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="b4188-165">1</span><span class="sxs-lookup"><span data-stu-id="b4188-165">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="b4188-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="b4188-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4188-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b4188-168">00</span><span class="sxs-lookup"><span data-stu-id="b4188-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="b4188-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="b4188-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4188-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b4188-171">01</span><span class="sxs-lookup"><span data-stu-id="b4188-171">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4188-172">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="b4188-172">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="b4188-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b4188-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="b4188-p109">カレント データベースから Microsoft Excel 97 ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="b4188-p109">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4188-176">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="b4188-176">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="b4188-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4188-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="b4188-178">01</span><span class="sxs-lookup"><span data-stu-id="b4188-178">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="b4188-179">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4188-179">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

<span data-ttu-id="b4188-180"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="b4188-180"><<<<<<< HEAD</span></span>

=======
## <a name="see-also"></a><span data-ttu-id="b4188-181">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4188-181">See also</span></span>

[<span data-ttu-id="b4188-182">Excel ドライバーで TypeGuessRows 設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="b4188-182">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
>>>>>>> <span data-ttu-id="b4188-183">master</span><span class="sxs-lookup"><span data-stu-id="b4188-183">master</span></span>
