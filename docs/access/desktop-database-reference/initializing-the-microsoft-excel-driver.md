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
ms.openlocfilehash: 12fb79f459024ed113007e6f764945ca9564cb3c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712933"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="2bdb7-102">Microsoft Office Excel ドライバーの初期化</span><span class="sxs-lookup"><span data-stu-id="2bdb7-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="2bdb7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bdb7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2bdb7-104">Excel ドライバーをインストールすると、セットアップ プログラムは、一連の既定値をエンジンと ISAM 形式のサブキーで、Windows レジストリに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="2bdb7-105">これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="2bdb7-106">次のセクションでは、初期化し、Microsoft Excel のデータベース ドライバーの ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="2bdb7-107">Excel の初期設定</span><span class="sxs-lookup"><span data-stu-id="2bdb7-107">Excel initialization settings</span></span>

<span data-ttu-id="2bdb7-108">**アクセス接続エンジン\\エンジン\\Excel**フォルダーには、Microsoft Excel ワークシートへの外部アクセスの使用、Aceexcl.dll のドライバーの初期設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="2bdb7-109">通常、このキーのエントリの設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="2bdb7-110">Microsoft Access データベース エンジンで使用される、Excel キーのエントリを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bdb7-111">エントリ</span><span class="sxs-lookup"><span data-stu-id="2bdb7-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="2bdb7-112">説明</span><span class="sxs-lookup"><span data-stu-id="2bdb7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-113">win32</span><span class="sxs-lookup"><span data-stu-id="2bdb7-113">win32</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-p103">Msexcl40.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="2bdb7-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-118">データ型を調べる行の数です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="2bdb7-119">検出されたデータの種類の最大数を指定したデータ型が決定されます。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="2bdb7-120">データ型は次の順序で決定は、同順がある場合は、: 数値、通貨、日付、文字列、ブール値です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="2bdb7-121">列のデータ型に一致しないデータが検出された場合は<strong>Null</strong>値として返されます。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="2bdb7-122">インポート時に [列のデータ型が混在している場合列全体は、ImportMixedTypes の設定に従ってキャストされます。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="2bdb7-123">チェックする行の既定数は、8 です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="2bdb7-124">値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="2bdb7-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-p105">MajorityType または Text のどちらかを設定できます。MajorityType を設定した場合、データ型が混在している列は、インポート時に最も数の多いデータ型にキャストされます。Text を設定した場合、データ型が混在している列は、インポート時にテキスト型 (Text) にキャストされます。既定値は Text です。値の型は REG_SZ 型です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="2bdb7-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-p106">Microsoft Jet 3.5 または 4.0 で、新しいデータを追加する前にワークシートの末尾に付加される空行の数です。たとえば、AppendBlankRows を 4 に設定すると、Microsoft Jet データベース エンジンはワークシートの末尾に 4 つの空行を付加してから、その後にデータのある行を付加します。このエントリには、0 ～ 16 の範囲の整数値を設定します。既定値は 01 (1 行の付加) です。値の型は REG_DWORD 型です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-136">消えて</span><span class="sxs-lookup"><span data-stu-id="2bdb7-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-p107">テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。値 00 では、1 行目に列名が含まれません。この場合、列名は F1、F2、F3、というように表示されます。既定値は 01 です。値の型は REG_BINARY 型です。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="2bdb7-142">**アクセス接続エンジン\\エンジン\\Excel 8.0**フォルダーには、Microsoft Excel 97 に適用されますが、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bdb7-143">エントリ名</span><span class="sxs-lookup"><span data-stu-id="2bdb7-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="2bdb7-144">型</span><span class="sxs-lookup"><span data-stu-id="2bdb7-144">Type</span></span></p></th>
<th><p><span data-ttu-id="2bdb7-145">値</span><span class="sxs-lookup"><span data-stu-id="2bdb7-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-146">Engine</span><span class="sxs-lookup"><span data-stu-id="2bdb7-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2bdb7-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-148">Excel</span><span class="sxs-lookup"><span data-stu-id="2bdb7-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="2bdb7-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2bdb7-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="2bdb7-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="2bdb7-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bdb7-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-154">01</span><span class="sxs-lookup"><span data-stu-id="2bdb7-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="2bdb7-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bdb7-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-157">00</span><span class="sxs-lookup"><span data-stu-id="2bdb7-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="2bdb7-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2bdb7-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-160">1</span><span class="sxs-lookup"><span data-stu-id="2bdb7-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="2bdb7-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bdb7-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-163">00</span><span class="sxs-lookup"><span data-stu-id="2bdb7-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="2bdb7-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bdb7-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-166">01</span><span class="sxs-lookup"><span data-stu-id="2bdb7-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bdb7-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="2bdb7-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2bdb7-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-p108">カレント データベースから Microsoft Excel 97 ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bdb7-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="2bdb7-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2bdb7-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2bdb7-173">01</span><span class="sxs-lookup"><span data-stu-id="2bdb7-173">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="2bdb7-174">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-174">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bdb7-175">関連項目</span><span class="sxs-lookup"><span data-stu-id="2bdb7-175">See also</span></span>

- [<span data-ttu-id="2bdb7-176">Excel ドライバーで TypeGuessRows 設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="2bdb7-176">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
